PID = Proporcionální, Integrační, Derivační
PID regulace je spojitá regulace.
# Regulátor s konstantním zesílením (P-regulátor)

![Regulátor s konstantním zesílením](RegulatorP.png)

## Popis
- Na vstupu regulátoru je **regulační odchylka** (chyba = rozdíl mezi požadovanou a aktuální hodnotou).  
- Výstup regulátoru je přímo úměrný odchylce:  
  
  $$u(t) = K_{p}  \cdot e(t)$$
  
  kde:
  - $u(t)$ = výstup regulátoru  
  - $e(t)$ = regulační odchylka  
  - $K_{p}$ = konstantní zesílení regulátoru  

## Vlastnosti
- Jedná se o **nejjednodušší typ regulátoru**.  
- Regulátor **zesiluje chybu**, ale nijak neakumuluje ani nepamatuje minulost.  
- Při **konstantním rušivém působení** (např. odporová síla, tření) se výsledná hodnota **ustálí s trvalou regulační odchylkou** (chyba ≠ 0).  
- Regulátor pouze **zamezuje dalšímu poklesu** a udržuje systém poblíž požadované hodnoty, ale ne na ní přesně.  

![image](regulator_1_odezva.png)

## Výhody
- Jednoduchost, snadná realizace.  
- Rychlá reakce na změny.  

## Nevýhody
- **Statická chyba** – systém nikdy přesně nedosáhne požadované hodnoty, pokud působí trvalá porucha.  
- Není vhodný pro přesné ustálení.  

## Klasifikace
- Řadí se mezi **statické regulátory**.  
- Samotný regulátor s konstantním zesílením nemění řád soustavy – výsledný řád systému závisí na řízené soustavě (může být 1. nebo 2. řádu podle modelu řízené části).  

## Použití
- Vhodný tam, kde **nevadí malá trvalá chyba** (např. jednoduché zesílení signálu, základní stabilizace).  
- Často se používá jako **součást složitějších regulátorů** (např. P-regulátor v PID regulaci).  


---


# Integrační regulátor (I-Regulátor)

1. Diferenciální rovnice
	- Integrační regulátor vytváří výstup, který závisí na integrálu chyby. Výstup se neustále zvyšuje nebo snižuje v závislosti na tom, zda je chyba kladná nebo záporná. 
	- Integrační složka pomáhá eliminovat zbytkovou chybu v ustáleném stavu.
	$$ u(t) = K_{1} \int_{0}^{t} e(\tau) \, \mathrm{d}\tau $$
	- $K_1$ = integrační zisk (zesílení)
	- $\int_{0}^{t} e(\tau) \, \mathrm{d}\tau$ = integrál chyby v čase
2. Přenosová funkce Integračního regulátoru
	- Přenosová funkce = poměr výstupu systému ke vstupu systému (obojí v Laplacově transformaci)
	$$G(s) = \frac{K_{1}}{s}$$

	- $s$ = komplexní frekvence (proměnná přenosové funkce)

### PID regulace řečí pythonu:

```

# Inevitable import

import matplotlib.pyplot as plt # creating graphs

# If doesn't work: Try: Open command line (type cmd),

# run: pip install matplotlib, if doesn't work too, then gg

  

h0 = 1.4 # Initial height m

v0 = 0 # Initial velocity m/s

h_wanted = 1 # Target height m

m = 1 # mass in kg

g = 9.81 # gravity acceleration m/s^-2

fg = m*g # gravity force N

dt = 0.001 # time step s

final_time = 60 # s

state = [h0, 0, 0] # state vector of the system

  

error = [h_wanted - state[0]] # Initial error (target - actual)

integral_sum = 0 # variable to store integral sum (adding, adding, adding...)

  

def pid(error):

    global dt

    global integral_sum

  

    # Those are constants that we are gonna optimize

    Kp = 10

    Kd = 10

    Ki = 10

  

    # P

    proportional = Kp * error[-1] + Kd * dif + Ki * integral_sum

  

    # I

    integral_sum += error[-1]*dt

  

    # D

    dif = (error[-1]- error[-2])/dt

  

    # = PID regulátor (proportional - integral_sum - derivative)

    return proportional

  

def model(state, m, fg, fq, dt):

    # Some physics here:

    global h_wanted

    a = (fq+fg)/m

    state[1] += a * dt

    dh = state[1] * dt

  

    state[0] += dh

    state[2] += dt

  

    return state

  

# Just define the arrays for processing

height = []

velocity = []

time = []

  

# state = [height, velocity, time]... and describes the state of the system (system = thrown object)

  

# Run the physics engine (= let the time start ticking)

for time_step in range(final_time*1000):

    error.append(h_wanted - state[0]) # Add current error to memory of all previous errors

    fq = pid(error) # Regulator output

  

    # Memorize the current state

    height.append(state[0])

    velocity.append(state[1])

    time.append(state[2])

  

    state = model(state, m, fg, fq, dt) # Calculate the new state through model

  

# Plot result

plt.plot(time, height) # x, y

plt.grid(True) # just design

plt.xlabel("time (s)")

plt.ylabel("height (m)")

plt.title("Flight of a thrown object regulation")

plt.show() # This line does the thing

  

# ps: comments got me longer than the code itself (just kidding)


```