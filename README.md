# Reto 6

Bienvenidos, a continuación les voy a mostrar como se resuelve el reto 6.
La verdad fue un poco tedioso para mi por lo largo que era pero se logró.

# 1) La esfera y el cono
![image](https://user-images.githubusercontent.com/124614177/227400957-b85082d2-7e75-4005-801d-132e9c96b75a.png)

- Una función matemática para calcular el volumen y el área superficial.

- Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r1, r2 y h.

- Revise como utilizar el valor de pi usando import math y math.pi

```
from cmath import pi
import math
math.pi

r1 = float(input("ingrese el radio de la esfera: "))
r2 = float(input("ingrese el radio del cono: "))
h = float(input("ingrese la altura del cono: "))


def volumen():
    vol_esfera = (3/4)*pi*(r1**3)
    vol_cono = (1/3)*h*pi*(r2**2)
    vol_total = vol_esfera + vol_cono
    print(vol_total)

def area():
    generatriz = ((r2**2)+(h**2))**0.5
    area_esfera = 4*pi*(r1**2)
    area_cono = (pi*r2*generatriz) + (pi*(r2**2))
    area_total = area_esfera + area_cono
    print(area_total)

print("el volumen total es ",volumen)
print("el area total es :",area)
```
# 2) Carrito 😆

![image](https://user-images.githubusercontent.com/124614177/227402989-dd9cc582-fbef-428b-bbbd-c2c6afa4161d.png)


Dado la figura de la imagen, desarrolle:

- Una función matemática para calcular el área y el perimetro.

- Cree dos funciones en python para calcular los valores antes establecidos, al ingresar por teclado r, a y b.

- Revise como utilizar el valor de pi usando import math y math.pi

```
from cmath import pi
import math
math.pi

a = float(input("ingrese la medida del lado más corto del rectangulo: "))
b = float(input("ingrese la medida del lado más largo del rectangulo: "))
r = float(input("ingrese el radio de los circulos: "))

def area():
    area_rec = b*a
    area_circulo = pi*(r**2)
    area_total = area_rec+(2*area_circulo)
    print(area_total)

def perimetro():
    per_rec = (2*a)+(2*b)
    per_circulo = pi*(2*r)
    per_total = per_rec+(2*per_circulo)

print("el area total es: ",area)
print("el perimetro total es: ",perimetro)
```
# 3) La carniceria 🍗

Diseñe una función que calcule la cantidad de carne de aves en kilos si se tienen N gallinas, M gallos y K pollitos cada uno pesando 6 kilos, 7 kilos y 1 kilo respectivamente.

```
N = int(input("ingrese la cantidad de gallinas que hay: "))
M = int(input("ingrese la cantidad de gallos que hay: "))
K = int(input("ingrese la cantidad de pollitos que hay: "))

def carne():
    N_total = 6*N
    M_total = 7*N
    K_total = 1*N
    carne_total = N_total+M_total+K_total
    print(carne_total)

print("la cantidad de carne de aves que hay en total es ",carne," kg")
```
# 4) La compra

Mi mamá me manda a comprar P panes a 300 cada uno, M bolsas de leche a 3300 cada una y H huevos a 350 cada uno. Hacer un programa que me diga las vueltas (o lo que quedo debiendo) cuando me da un billete de B pesos.
```
B = int(input("¿Cuánto dinero te dió tu mamá para la compra?: "))
P = int(input("¿Cuántos panes tienes que comprar?: "))
M = int(input("¿Cuántas bolsas de leche tienes que comprar?: "))
H =  int(input("¿Cuántos huevos tienes que comprar?: "))

panes = P*300
leche = M*3300
huevos = H*350

cuenta = panes+leche+huevos

if cuenta <= B:
    vueltas = B-cuenta
    print("tu compra costó $",cuenta," por lo tanto tus vuelas son $",vueltas)
else:
    debo = abs(B-cuenta)
    print("no te alcanzó la plata, ahora le debes $",debo," al tipo de la tienda")
```
# 5) El gota a gota 😥

Haga un programa que utilice una función para calcular el valor de un préstamo C usando interés compuesto del i por n meses.
```
Ci = int(input("ingrese el capital inicial en pesos: "))
i = int(input("ingrese la tasa de interés (%): "))
n = int(input("ingrese el periodo de ahorro en meses: "))

def interes():
    Cf = Ci*((1+(i/100)**n))
    print("El capital final teniendo en cuenta la información dada es ",Cf)

interes()
```
# 6) COVID-19

El número de contagiados de Covid-19 en el país de NuncaLandia se duplica cada día. Hacer un programa que diga el número total de personas que se han contagiado cuando pasen D días a partir de hoy, si el número de contagiados actuales es C.
```
C = int(input("cuántos son los contagiados actuales de COVID-19?: "))
D = int(input("ingrese el número de días para el pronosticar los casos para ese tiempo: "))
contagios = C**D
print("los contagios para el dia ",D," son ",contagios)
```
# 7) El código que me sacó canas

Escriba un programa que pida 5 números reales y calcule las siguientes operaciones usando una función para cada una:

- El promedio
- La mediana
- El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)
- Ordenar los números de forma ascendente
- Ordenar los números de forma descendente
- La potencia del mayor número elevado al menor número
- La raíz cúbica del menor número

```
n1 = int(input("ingrese un número: "))
n2 = int(input("ingrese un número: "))
n3 = int(input("ingrese un número: "))
n4 = int(input("ingrese un número: "))
n5 = int(input("ingrese un número: "))


#El promedio


prom = (n1+n2+n3+n4+n5)/5
print("1) el promedio de los números dados es: ",prom)


#La mediana




if n1<n2 and n1<n3 and n1<n4 and n1<n5: #n1
    if n2<n3 and n2<n4 and n2<n5: #n1 n2
        if n3<n4 and n3<n5: #n1 n2 n3
            if n4<n5: #n1 n2 n3 n4
                m1,m2,m3,m4,m5 =n1,n2,n3,n4,n5 #n1 n2 n3 n4 n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n1 n2 n3 n5
                m1,m2,m3,m4,m5 =n1,n2,n3,n5,n4 #n1 n2 n3 n5 n4
                print(m1,m2,m3,m4,m5)
        elif n4<n3 and n4<n5: #n1 n2 n4
            if n3<n5: #n1 n2 n4 n3 n5
                m1,m2,m3,m4,m5 =n1,n2,n4,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n1 n2 n4 n5 n3
                m1,m2,m3,m4,m5 =n1,n2,n4,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n5<n3 and n5<n4: #n1 n2 n5
            if n3<n4: #n1 n2 n5 n3 n4
                m1,m2,m3,m4,m5 =n1,n2,n5,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n1 n2 n5 n4 n3
                m1,m2,m3,m4,m5 =n1,n2,n5,n4,n3
                print(m1,m2,m3,m4,m5)
    elif n3<n2 and n3<n4 and n3<n5: #n1 n3
        if n2<n4 and n2<n5: #n1 n3 n2
            if n4<n5: #n1 n3 n2 n4 n5
                m1,m2,m3,m4,m5 =n1,n3,n2,n4,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n1 n3 n2 n5 n4
                m1,m2,m3,m4,m5 =n1,n3,n2,n5,n4
                print(m1,m2,m3,m4,m5)
        elif n4<n2 and n4<n5: #n1 n3 n4
            if n2<n5: #n1 n3 n4 n2 n5
                m1,m2,m3,m4,m5 =n1,n3,n4,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n1 n3 n4 n5 n2
                m1,m2,m3,m4,m5 =n1,n3,n4,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n5<n2 and n5<n4: #n1 n3 n5
            if n2<n4: #n1 n3 n5 n2 n4
                m1,m2,m3,m4,m5 =n1,n3,n5,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n1 n3 n5 n4 n2
                m1,m2,m3,m4,m5 =n1,n3,n5,n4,n2
                print(m1,m2,m3,m4,m5)
    elif n4<n2 and n4<n3 and n4<n5: #n1 n4
        if n2<n3 and n2<n5: #n1 n4 n2
            if n3<n5: #n1 n4 n2 n3 n5
                m1,m2,m3,m4,m5 =n1,n4,n2,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n1 n4 n2 n5 n3
                m1,m2,m3,m4,m5 =n1,n4,n2,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n2 and n3<n5: #n1 n4 n3
            if n2<n5:#n1 n4 n3 n2 n5
                m1,m2,m3,m4,m5 =n1,n4,n3,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n1 n4 n3 n5 n2
                m1,m2,m3,m4,m5 =n1,n4,n3,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n5<n2 and n5<n3: #n1 n4 n5
            if n2<n3: #n1 n4 n5 n2 n3
                m1,m2,m3,m4,m5 =n1,n4,n5,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2: #n1 n4 n5 n3 n2
                m1,m2,m3,m4,m5 =n1,n4,n5,n3,n2
                print(m1,m2,m3,m4,m5)
    elif n5<n2 and n5<n3 and n5<n4: #n1 n5
        if n2<n3 and n2<n4: #n1 n5 n2
            if n3<n4: #n1 n5 n2 n3 n4
                m1,m2,m3,m4,m5 =n1,n5,n2,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n1 n5 n2 n4 n3
                m1,m2,m3,m4,m5 =n1,n5,n2,n4,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n2 and n3<n4: #n1 n5 n3
            if n2<n4:#n1 n5 n3 n2 n4
                m1,m2,m3,m4,m5 =n1,n5,n3,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n1 n5 n3 n4 n2
                m1,m2,m3,m4,m5 =n1,n5,n3,n4,n2
                print(m1,m2,m3,m4,m5)
        elif n4<n2 and n4<n3: #n1 n5 n4
            if n2<n3:#n1 n5 n4 n2 n3
                m1,m2,m3,m4,m5 =n1,n5,n4,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2:#n1 n5 n4 n3 n2
                m1,m2,m3,m4,m5 =n1,n5,n4,n3,n2
                print(m1,m2,m3,m4,m5)
elif n2<n1 and n2<n3 and n2<n4 and n2<n5: #n2
    if n1<n3 and n1<n4 and n1<n5: #n2 n1
        if n3<n4 and n3<n5: #n2 n1 n3
            if n4<n5: #n2 n1 n3 n4 n5
                m1,m2,m3,m4,m5 =n2,n1,n3,n4,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n2 n1 n3 n5 n4
                m1,m2,m3,m4,m5 =n2,n1,n3,n5,n4
                print(m1,m2,m3,m4,m5)
        elif n4<n3 and n4<n5: #n2 n1 n4
            if n3<n5: #n2 n1 n4 n3 n5
                m1,m2,m3,m4,m5 =n2,n1,n4,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n2 n1 n4 n5 n3
                m1,m2,m3,m4,m5 =n2,n1,n4,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n5<n3 and n5<n4: #n2 n1 n5
            if n3<n4: #n2 n1 5n n3 n4
                m1,m2,m3,m4,m5 =n2,n1,n5,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n2 n1 n5 n4 n3
                m1,m2,m3,m4,m5 =n2,n1,n5,n4,n3
                print(m1,m2,m3,m4,m5)
    elif n3<n1 and n3<n4 and n3<n5: #n2 n3
        if n1<n4 and n1<n5: #n2 n3 n1
            if n4<n5: #n2 n3 n1 n4 n5
                m1,m2,m3,m4,m5 =n2,n3,n1,n4,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n2 n3 n1 n5 n4
                m1,m2,m3,m4,m5 =n2,n3,n1,n5,n4
                print(m1,m2,m3,m4,m5)
        elif n4<n1 and n4<n5: #n2 n3 n4
            if n1<n5: #n2 n3 n4 n1 n5
                m1,m2,m3,m4,m5 =n2,n3,n4,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n2 n3 n4 n5 n1
                m1,m2,m3,m4,m5 =n2,n3,n4,n5,n1
                print(m1,m2,m3,m4,m5)
        elif n5<n1 and n5<n4: #n2 n3 n5
            if n1<n4: #n2 n3 n5 n1 n4
                m1,m2,m3,m4,m5 =n2,n3,n5,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n2 n3 n5 n4 n1
                m1,m2,m3,m4,m5 =n2,n3,n5,n4,n1
                print(m1,m2,m3,m4,m5)
    elif n4<n1 and n4<n3 and n4<n5: #n2 n4
        if n1<n3 and n1<n5:#n2 n4 n1
            if n3<n5: #n2 n4 n1 n3 n5
                m1,m2,m3,m4,m5 =n2,n4,n1,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n2 n4 n1 n5 n3
                m1,m2,m3,m4,m5 =n2,n4,n1,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n5: #n2 n4 n3
            if n1<n5: #n2 n4 n3 n1 n5
                m1,m2,m3,m4,m5 =n2,n4,n3,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n2 n4 n3 n5 n1
                m1,m2,m3,m4,m5 =n2,n4,n3,n5,n1
                print(m1,m2,m3,m4,m5)
        elif n5<n1 and n5<n3: #n2 n4 n5
            if n1<n3:#n2 n4 n5 n1 n3
                m1,m2,m3,m4,m5 =n2,n4,n5,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n2 n4 n5 n3 n1
                m1,m2,m3,m4,m5 =n2,n4,n5,n3,n1
                print(m1,m2,m3,m4,m5)
    elif n5<n1 and n5<n3 and n5<n4: #n2 n5
        if n1<n3 and n1<n4: #n2 n5 n1
            if n3<n4: #n2 n5 n1 n3 n4
                m1,m2,m3,m4,m5 =n2,n5,n1,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n2 n5 n1 n4 n3
                m1,m2,m3,m4,m5 =n2,n5,n1,n4,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n4: #n2 n5 n3
            if n1<n4: #n2 n5 n3 n1 n4
                m1,m2,m3,m4,m5 =n2,n5,n3,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n2 n5 n3 n4 n1
                m1,m2,m3,m4,m5 =n2,n5,n3,n4,n1
                print(m1,m2,m3,m4,m5)
        elif n4<n1 and n4<n3: #n2 n5 n4
            if n1<n3: #n2 n5 n4 n1 n3
                m1,m2,m3,m4,m5 =n2,n5,n4,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n2 n5 n4 n3 n1
                m1,m2,m3,m4,m5 =n2,n5,n4,n3,n1
                print(m1,m2,m3,m4,m5)
elif n3<n1 and n3<n2 and n3<n4 and n3<n5:#n3
    if n1<n2 and n1<n4 and n1<n5: #n3 n1
        if n2<n4 and n2<n5: #n3 n1 n2
            if n4<n5: #n3 n1 n2 n4 n5
                m1,m2,m3,m4,m5 =n3,n1,n2,n4,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n3 n1 n2 n5 n4
                m1,m2,m3,m4,m5 =n3,n1,n2,n5,n4
                print(m1,m2,m3,m4,m5)
        elif n4<n2 and n4<n5: #n3 n1 n4
            if n2<n5: #n3 n1 n4 n2 n5
                m1,m2,m3,m4,m5 =n3,n1,n4,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n3 n1 n4 n5 n2
                m1,m2,m3,m4,m5 =n3,n1,n4,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n5<n2 and n5<n4: #n3 n1 n5
            if n2<n4: #n3 n1 n5 n2 n4
                m1,m2,m3,m4,m5 =n3,n1,n5,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n3 n1 n5 n4 n2
                m1,m2,m3,m4,m5 =n3,n1,n5,n4,n2
                print(m1,m2,m3,m4,m5)
    elif n2<n1 and n2<n4 and n2<n5: #n3 n2
        if n1<n4 and n1<n5: #n3 n2 n1
            if n4<n5: #n3 n2 n1 n4 n5
                m1,m2,m3,m4,m5 =n3,n2,n1,n4,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n3 n2 n1 n5 n4
                m1,m2,m3,m4,m5 =n3,n2,n1,n5,n4
                print(m1,m2,m3,m4,m5)
        if n4<n1 and n4<n5: #n3 n2 n4
            if n1<n5: #n3 n2 n4 n1 n5
                m1,m2,m3,m4,m5 =n3,n2,n4,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n3 n2 n4 n5 n1
                m1,m2,m3,m4,m5 =n3,n2,n4,n5,n1
                print(m1,m2,m3,m4,m5)
        if n5<n1 and n5<n4: #n3 n2 n5
            if n1<n4: #n3 n2 n5 n1 n4
                m1,m2,m3,m4,m5 =n3,n2,n5,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n3 n2 n5 n4 n1
                m1,m2,m3,m4,m5 =n3,n2,n5,n4,n1
                print(m1,m2,m3,m4,m5)
    elif n4<n1 and n4<n2 and n4<n5: #n3 n4
        if n1<n2 and n1<n5: #n3 n4 n1
            if n2<n5: #n3 n4 n1 n2 n5
                m1,m2,m3,m4,m5 =n3,n4,n1,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n3 n4 n1 n5 n2
                m1,m2,m3,m4,m5 =n3,n4,n1,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n5: #n3 n4 n2
            if n1<n5: #n3 n4 n2 n1 n5
                m1,m2,m3,m4,m5 =n3,n4,n2,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n3 n4 n2 n5 n1
                m1,m2,m3,m4,m5 =n3,n4,n2,n5,n1
                print(m1,m2,m3,m4,m5)
        elif n5<n1 and n5<n2: #n3 n4 n5
            if n1<n2: #n3 n4 n5 n1 n2
                m1,m2,m3,m4,m5 =n3,n4,n5,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n3 n4 n5 n2 n1
                m1,m2,m3,m4,m5 =n3,n4,n5,n2,n1
                print(m1,m2,m3,m4,m5)
    elif n5<n1 and n5<n2 and n5<n4: #n3 n5
        if n1<n2 and n1<n4: #n3 n5 n1
            if n2<n4: #n3 n5 n1 n2 n4
                m1,m2,m3,m4,m5 =n3,n5,n1,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n3 n5 n1 n4 n2
                m1,m2,m3,m4,m5 =n3,n5,n1,n4,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n4: #n3 n5 n2
            if n1<n4: #n3 n5 n2 n1 n4
                m1,m2,m3,m4,m5 =n3,n5,n2,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n3 n5 n2 n4 n1
                m1,m2,m3,m4,m5 =n3,n5,n2,n4,n1
                print(m1,m2,m3,m4,m5)
        elif n4<n1 and n4<n2: #n3 n5 n4
            if n1<n2: #n3 n5 n4 n1 n2
                m1,m2,m3,m4,m5 =n3,n5,n4,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n3 n5 n4 n2 n1
                m1,m2,m3,m4,m5 =n3,n5,n4,n2,n1
                print(m1,m2,m3,m4,m5)
elif n4<n1 and n4<n2 and n4<n3 and n4<n5:#n4
    if n1<n2 and n1<n3 and n1<n5: #n4 n1
        if n2<n3 and n2<n5: #n4 n1 n2
            if n3<n5: #n4 n1 n2 n3 n5
                m1,m2,m3,m4,m5 =n4,n1,n2,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n4 n1 n2 n5 n3
                m1,m2,m3,m4,m5 =n4,n1,n2,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n2 and n3<n5: #n4 n1 n3
            if n2<n5: #n4 n1 n3 n2 n5
                m1,m2,m3,m4,m5 =n4,n1,n3,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n4 n1 n3 n5 n2
                m1,m2,m3,m4,m5 =n4,n1,n3,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n5<n2 and n5<n3: #n4 n1 n5
            if n2<n3: #n4 n1 n5 n2 n3
                m1,m2,m3,m4,m5 =n4,n1,n5,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2: #n4 n1 n5 n3 n2
                m1,m2,m3,m4,m5 =n4,n1,n5,n3,n2
                print(m1,m2,m3,m4,m5)
    elif n2<n1 and n2<n3 and n2<n5: #n4 n2
        if n1<n3 and n1<n5: #n4 n2 n1
            if n3<n5: #n4 n2 n1 n3 n5
                m1,m2,m3,m4,m5 =n4,n2,n1,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n4 n2 n1 n5 n3
                m1,m2,m3,m4,m5 =n4,n2,n1,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n5: #n4 n2 n3
            if n1<n5: #n4 n2 n3 n1 n5
                m1,m2,m3,m4,m5 =n4,n2,n3,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n4 n2 n3 n5 n1
                m1,m2,m3,m4,m5 =n4,n2,n3,n5,n1
                print(m1,m2,m3,m4,m5)
        elif n5<n1 and n5<n3: #n4 n2 n5
            if n1<n3: #n4 n2 n5 n1 n3
                m1,m2,m3,m4,m5 =n4,n2,n5,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n4 n2 n5 n3 n1
                m1,m2,m3,m4,m5 =n4,n2,n5,n3,n1
                print(m1,m2,m3,m4,m5)
    elif n3<n1 and n3<n2 and n3<n5: #n4 n3
        if n1<n2 and n1<n5: #n4 n3 n1
            if n2<n5: #n4 n3 n1 n2 n5
                m1,m2,m3,m4,m5 =n4,n3,n1,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n4 n3 n1 n5 n2
                m1,m2,m3,m4,m5 =n4,n3,n1,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n5: #n4 n3 n2
            if n1<n5: #n4 n3 n2 n1 n5
                m1,m2,m3,m4,m5 =n4,n3,n2,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n4 n3 n2 n5 n1
                m1,m2,m3,m4,m5 =n4,n3,n2,n5,n1
                print(m1,m2,m3,m4,m5)
        elif n5<n1 and n5<n2: #n4 n3 n5
            if n1<n2: #n4 n3 n5 n1 n2
                m1,m2,m3,m4,m5 =n4,n3,n5,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n4 n3 n5 n2 n1
                m1,m2,m3,m4,m5 =n4,n3,n5,n2,n1
                print(m1,m2,m3,m4,m5)
    elif n5<n1 and n5<n2 and n5<n3: #n4 n5
        if n1<n2 and n1<n3: #n4 n5 n1
            if n2<n3: #n4 n5 n1 n2 n3
                m1,m2,m3,m4,m5 =n4,n5,n1,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2: #n4 n5 n1 n3 n2
                m1,m2,m3,m4,m5 =n4,n5,n1,n3,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n3: #n4 n5 n2
            if n1<n3: #n4 n5 n2 n1 n3
                m1,m2,m3,m4,m5 =n4,n5,n2,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n4 n5 n2 n3 n1
                m1,m2,m3,m4,m5 =n4,n5,n2,n3,n1
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n2: #n4 n5 n3
            if n1<n2: #n4 n5 n3 n1 n2
                m1,m2,m3,m4,m5 =n4,n5,n3,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n4 n5 n3 n2 n1
                m1,m2,m3,m4,m5 =n4,n5,n3,n2,n1
                print(m1,m2,m3,m4,m5)
elif n5<n1 and n5<n2 and n5<n3 and n5<n4: #n5
    if n1<n2 and n1<n3 and n1<n4: #n5 n1
        if n2<n3 and n2<n4: #n5 n1 n2
            if n3<n4: #n5 n1 n2 n3 n4
                m1,m2,m3,m4,m5 =n5,n1,n2,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n5 n1 n2 n4 n3
                m1,m2,m3,m4,m5 =n5,n1,n2,n4,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n2 and n3<n4: #n5 n1 n3
            if n2<n4: #n5 n1 n3 n2 n4
                m1,m2,m3,m4,m5 =n5,n1,n3,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n5 n1 n3 n4 n2
                m1,m2,m3,m4,m5 =n5,n1,n3,n4,n2
                print(m1,m2,m3,m4,m5)
        elif n4<n2 and n4<n3: #n5 n1 n4
            if n2<n3: #n5 n1 n4 n2 n3
                m1,m2,m3,m4,m5 =n5,n1,n4,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2: #n5 n1 n4 n3 n2
                m1,m2,m3,m4,m5 =n5,n1,n4,n3,n2
                print(m1,m2,m3,m4,m5)
    elif n2<n1 and n2<n3 and n2<n4: #n5 n2
        if n1<n3 and n1<n4:#n5 n2 n1
            if n3<n4: #n5 n2 n1 n3 n4
                m1,m2,m3,m4,m5 =n5,n2,n1,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n5 n2 n1 n4 n3
                m1,m2,m3,m4,m5 =n5,n2,n1,n4,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n4: #n5 n2 n3
            if n1<n4: #n5 n2 n3 n1 n4
                m1,m2,m3,m4,m5 =n5,n2,n3,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n5 n2 n3 n4 n1
                m1,m2,m3,m4,m5 =n5,n2,n3,n4,n1
                print(m1,m2,m3,m4,m5)
        elif n4<n1 and n4<n3: #n5 n2 n4
            if n1<n3: #n5 n2 n4 n1 n3
                m1,m2,m3,m4,m5 =n5,n2,n4,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n5 n2 n4 n3 n1
                m1,m2,m3,m4,m5 =n5,n2,n4,n3,n1
                print(m1,m2,m3,m4,m5)
    elif n3<n1 and n3<n2 and n3<n4: #n5 n3
        if n1<n2 and n1<n4: #n5 n3 n1
            if n2<n4: #n5 n3 n1 n2 n4
                m1,m2,m3,m4,m5 =n5,n3,n1,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n5 n3 n1 n4 n2
                m1,m2,m3,m4,m5 =n5,n3,n1,n4,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n4: #n5 n3 n2
            if n1<n4: #n5 n3 n2 n1 n4
                m1,m2,m3,m4,m5 =n5,n3,n2,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n5 n3 n2 n4 n1
                m1,m2,m3,m4,m5 =n5,n3,n2,n4,n1
                print(m1,m2,m3,m4,m5)
        elif n4<n1 and n4<n2: #n5 n3 n4
            if n1<n2: #n5 n3 n4 n1 n2
                m1,m2,m3,m4,m5 =n5,n3,n4,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n5 n3 n4 n2 n1
                m1,m2,m3,m4,m5 =n5,n3,n4,n2,n1
                print(m1,m2,m3,m4,m5)
    elif n4<n1 and n4<n2 and n4<n3: #n5 n4
        if n1<n2 and n1<n3: #n5 n4 n1
            if n2<n3: #n5 n4 n1 n2 n3
                m1,m2,m3,m4,m5 =n5,n4,n1,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2: #n5 n4 n1 n3 n2
                m1,m2,m3,m4,m5 =n5,n4,n1,n3,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n3: #n5 n4 n2
            if n1<n3: #n5 n4 n2 n1 n3
                m1,m2,m3,m4,m5 =n5,n4,n2,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n5 n4 n2 n3 n1
                m1,m2,m3,m4,m5 =n5,n4,n2,n3,n1
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n2: #n5 n4 n3
            if n1<n2: #n5 n4 n3 n1 n2
                m1,m2,m3,m4,m5 =n5,n4,n3,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n5 n4 n3 n2 n1
                m1,m2,m3,m4,m5 =n5,n4,n3,n2,n1
                print(m1,m2,m3,m4,m5)




print("2) La mediana de los numeros dados es el número de la mitad ",m3)


#El promedio multiplicativo (multilplica todos y luego calcula la raíz de la cantidad de operandos)


prom_mul = (n1*n2*n3*n4*n5)**5
print("3) El promedio multiplicativo de los números dados es: ",prom_mul)


#Ordenar los números de forma ascendente


print("4) Los números organizados de menor a mayor se ve de la siguiente manera: ")
if n1<n2 and n1<n3 and n1<n4 and n1<n5: #n1
    if n2<n3 and n2<n4 and n2<n5: #n1 n2
        if n3<n4 and n3<n5: #n1 n2 n3
            if n4<n5: #n1 n2 n3 n4
                m1,m2,m3,m4,m5 =n1,n2,n3,n4,n5 #n1 n2 n3 n4 n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n1 n2 n3 n5
                m1,m2,m3,m4,m5 =n1,n2,n3,n5,n4 #n1 n2 n3 n5 n4
                print(m1,m2,m3,m4,m5)
        elif n4<n3 and n4<n5: #n1 n2 n4
            if n3<n5: #n1 n2 n4 n3 n5
                m1,m2,m3,m4,m5 =n1,n2,n4,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n1 n2 n4 n5 n3
                m1,m2,m3,m4,m5 =n1,n2,n4,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n5<n3 and n5<n4: #n1 n2 n5
            if n3<n4: #n1 n2 n5 n3 n4
                m1,m2,m3,m4,m5 =n1,n2,n5,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n1 n2 n5 n4 n3
                m1,m2,m3,m4,m5 =n1,n2,n5,n4,n3
                print(m1,m2,m3,m4,m5)
    elif n3<n2 and n3<n4 and n3<n5: #n1 n3
        if n2<n4 and n2<n5: #n1 n3 n2
            if n4<n5: #n1 n3 n2 n4 n5
                m1,m2,m3,m4,m5 =n1,n3,n2,n4,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n1 n3 n2 n5 n4
                m1,m2,m3,m4,m5 =n1,n3,n2,n5,n4
                print(m1,m2,m3,m4,m5)
        elif n4<n2 and n4<n5: #n1 n3 n4
            if n2<n5: #n1 n3 n4 n2 n5
                m1,m2,m3,m4,m5 =n1,n3,n4,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n1 n3 n4 n5 n2
                m1,m2,m3,m4,m5 =n1,n3,n4,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n5<n2 and n5<n4: #n1 n3 n5
            if n2<n4: #n1 n3 n5 n2 n4
                m1,m2,m3,m4,m5 =n1,n3,n5,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n1 n3 n5 n4 n2
                m1,m2,m3,m4,m5 =n1,n3,n5,n4,n2
                print(m1,m2,m3,m4,m5)
    elif n4<n2 and n4<n3 and n4<n5: #n1 n4
        if n2<n3 and n2<n5: #n1 n4 n2
            if n3<n5: #n1 n4 n2 n3 n5
                m1,m2,m3,m4,m5 =n1,n4,n2,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n1 n4 n2 n5 n3
                m1,m2,m3,m4,m5 =n1,n4,n2,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n2 and n3<n5: #n1 n4 n3
            if n2<n5:#n1 n4 n3 n2 n5
                m1,m2,m3,m4,m5 =n1,n4,n3,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n1 n4 n3 n5 n2
                m1,m2,m3,m4,m5 =n1,n4,n3,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n5<n2 and n5<n3: #n1 n4 n5
            if n2<n3: #n1 n4 n5 n2 n3
                m1,m2,m3,m4,m5 =n1,n4,n5,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2: #n1 n4 n5 n3 n2
                m1,m2,m3,m4,m5 =n1,n4,n5,n3,n2
                print(m1,m2,m3,m4,m5)
    elif n5<n2 and n5<n3 and n5<n4: #n1 n5
        if n2<n3 and n2<n4: #n1 n5 n2
            if n3<n4: #n1 n5 n2 n3 n4
                m1,m2,m3,m4,m5 =n1,n5,n2,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n1 n5 n2 n4 n3
                m1,m2,m3,m4,m5 =n1,n5,n2,n4,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n2 and n3<n4: #n1 n5 n3
            if n2<n4:#n1 n5 n3 n2 n4
                m1,m2,m3,m4,m5 =n1,n5,n3,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n1 n5 n3 n4 n2
                m1,m2,m3,m4,m5 =n1,n5,n3,n4,n2
                print(m1,m2,m3,m4,m5)
        elif n4<n2 and n4<n3: #n1 n5 n4
            if n2<n3:#n1 n5 n4 n2 n3
                m1,m2,m3,m4,m5 =n1,n5,n4,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2:#n1 n5 n4 n3 n2
                m1,m2,m3,m4,m5 =n1,n5,n4,n3,n2
                print(m1,m2,m3,m4,m5)
elif n2<n1 and n2<n3 and n2<n4 and n2<n5: #n2
    if n1<n3 and n1<n4 and n1<n5: #n2 n1
        if n3<n4 and n3<n5: #n2 n1 n3
            if n4<n5: #n2 n1 n3 n4 n5
                m1,m2,m3,m4,m5 =n2,n1,n3,n4,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n2 n1 n3 n5 n4
                m1,m2,m3,m4,m5 =n2,n1,n3,n5,n4
                print(m1,m2,m3,m4,m5)
        elif n4<n3 and n4<n5: #n2 n1 n4
            if n3<n5: #n2 n1 n4 n3 n5
                m1,m2,m3,m4,m5 =n2,n1,n4,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n2 n1 n4 n5 n3
                m1,m2,m3,m4,m5 =n2,n1,n4,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n5<n3 and n5<n4: #n2 n1 n5
            if n3<n4: #n2 n1 5n n3 n4
                m1,m2,m3,m4,m5 =n2,n1,n5,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n2 n1 n5 n4 n3
                m1,m2,m3,m4,m5 =n2,n1,n5,n4,n3
                print(m1,m2,m3,m4,m5)
    elif n3<n1 and n3<n4 and n3<n5: #n2 n3
        if n1<n4 and n1<n5: #n2 n3 n1
            if n4<n5: #n2 n3 n1 n4 n5
                m1,m2,m3,m4,m5 =n2,n3,n1,n4,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n2 n3 n1 n5 n4
                m1,m2,m3,m4,m5 =n2,n3,n1,n5,n4
                print(m1,m2,m3,m4,m5)
        elif n4<n1 and n4<n5: #n2 n3 n4
            if n1<n5: #n2 n3 n4 n1 n5
                m1,m2,m3,m4,m5 =n2,n3,n4,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n2 n3 n4 n5 n1
                m1,m2,m3,m4,m5 =n2,n3,n4,n5,n1
                print(m1,m2,m3,m4,m5)
        elif n5<n1 and n5<n4: #n2 n3 n5
            if n1<n4: #n2 n3 n5 n1 n4
                m1,m2,m3,m4,m5 =n2,n3,n5,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n2 n3 n5 n4 n1
                m1,m2,m3,m4,m5 =n2,n3,n5,n4,n1
                print(m1,m2,m3,m4,m5)
    elif n4<n1 and n4<n3 and n4<n5: #n2 n4
        if n1<n3 and n1<n5:#n2 n4 n1
            if n3<n5: #n2 n4 n1 n3 n5
                m1,m2,m3,m4,m5 =n2,n4,n1,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n2 n4 n1 n5 n3
                m1,m2,m3,m4,m5 =n2,n4,n1,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n5: #n2 n4 n3
            if n1<n5: #n2 n4 n3 n1 n5
                m1,m2,m3,m4,m5 =n2,n4,n3,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n2 n4 n3 n5 n1
                m1,m2,m3,m4,m5 =n2,n4,n3,n5,n1
                print(m1,m2,m3,m4,m5)
        elif n5<n1 and n5<n3: #n2 n4 n5
            if n1<n3:#n2 n4 n5 n1 n3
                m1,m2,m3,m4,m5 =n2,n4,n5,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n2 n4 n5 n3 n1
                m1,m2,m3,m4,m5 =n2,n4,n5,n3,n1
                print(m1,m2,m3,m4,m5)
    elif n5<n1 and n5<n3 and n5<n4: #n2 n5
        if n1<n3 and n1<n4: #n2 n5 n1
            if n3<n4: #n2 n5 n1 n3 n4
                m1,m2,m3,m4,m5 =n2,n5,n1,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n2 n5 n1 n4 n3
                m1,m2,m3,m4,m5 =n2,n5,n1,n4,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n4: #n2 n5 n3
            if n1<n4: #n2 n5 n3 n1 n4
                m1,m2,m3,m4,m5 =n2,n5,n3,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n2 n5 n3 n4 n1
                m1,m2,m3,m4,m5 =n2,n5,n3,n4,n1
                print(m1,m2,m3,m4,m5)
        elif n4<n1 and n4<n3: #n2 n5 n4
            if n1<n3: #n2 n5 n4 n1 n3
                m1,m2,m3,m4,m5 =n2,n5,n4,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n2 n5 n4 n3 n1
                m1,m2,m3,m4,m5 =n2,n5,n4,n3,n1
                print(m1,m2,m3,m4,m5)
elif n3<n1 and n3<n2 and n3<n4 and n3<n5:#n3
    if n1<n2 and n1<n4 and n1<n5: #n3 n1
        if n2<n4 and n2<n5: #n3 n1 n2
            if n4<n5: #n3 n1 n2 n4 n5
                m1,m2,m3,m4,m5 =n3,n1,n2,n4,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n3 n1 n2 n5 n4
                m1,m2,m3,m4,m5 =n3,n1,n2,n5,n4
                print(m1,m2,m3,m4,m5)
        elif n4<n2 and n4<n5: #n3 n1 n4
            if n2<n5: #n3 n1 n4 n2 n5
                m1,m2,m3,m4,m5 =n3,n1,n4,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n3 n1 n4 n5 n2
                m1,m2,m3,m4,m5 =n3,n1,n4,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n5<n2 and n5<n4: #n3 n1 n5
            if n2<n4: #n3 n1 n5 n2 n4
                m1,m2,m3,m4,m5 =n3,n1,n5,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n3 n1 n5 n4 n2
                m1,m2,m3,m4,m5 =n3,n1,n5,n4,n2
                print(m1,m2,m3,m4,m5)
    elif n2<n1 and n2<n4 and n2<n5: #n3 n2
        if n1<n4 and n1<n5: #n3 n2 n1
            if n4<n5: #n3 n2 n1 n4 n5
                m1,m2,m3,m4,m5 =n3,n2,n1,n4,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n4: #n3 n2 n1 n5 n4
                m1,m2,m3,m4,m5 =n3,n2,n1,n5,n4
                print(m1,m2,m3,m4,m5)
        if n4<n1 and n4<n5: #n3 n2 n4
            if n1<n5: #n3 n2 n4 n1 n5
                m1,m2,m3,m4,m5 =n3,n2,n4,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n3 n2 n4 n5 n1
                m1,m2,m3,m4,m5 =n3,n2,n4,n5,n1
                print(m1,m2,m3,m4,m5)
        if n5<n1 and n5<n4: #n3 n2 n5
            if n1<n4: #n3 n2 n5 n1 n4
                m1,m2,m3,m4,m5 =n3,n2,n5,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n3 n2 n5 n4 n1
                m1,m2,m3,m4,m5 =n3,n2,n5,n4,n1
                print(m1,m2,m3,m4,m5)
    elif n4<n1 and n4<n2 and n4<n5: #n3 n4
        if n1<n2 and n1<n5: #n3 n4 n1
            if n2<n5: #n3 n4 n1 n2 n5
                m1,m2,m3,m4,m5 =n3,n4,n1,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n3 n4 n1 n5 n2
                m1,m2,m3,m4,m5 =n3,n4,n1,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n5: #n3 n4 n2
            if n1<n5: #n3 n4 n2 n1 n5
                m1,m2,m3,m4,m5 =n3,n4,n2,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n3 n4 n2 n5 n1
                m1,m2,m3,m4,m5 =n3,n4,n2,n5,n1
                print(m1,m2,m3,m4,m5)
        elif n5<n1 and n5<n2: #n3 n4 n5
            if n1<n2: #n3 n4 n5 n1 n2
                m1,m2,m3,m4,m5 =n3,n4,n5,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n3 n4 n5 n2 n1
                m1,m2,m3,m4,m5 =n3,n4,n5,n2,n1
                print(m1,m2,m3,m4,m5)
    elif n5<n1 and n5<n2 and n5<n4: #n3 n5
        if n1<n2 and n1<n4: #n3 n5 n1
            if n2<n4: #n3 n5 n1 n2 n4
                m1,m2,m3,m4,m5 =n3,n5,n1,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n3 n5 n1 n4 n2
                m1,m2,m3,m4,m5 =n3,n5,n1,n4,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n4: #n3 n5 n2
            if n1<n4: #n3 n5 n2 n1 n4
                m1,m2,m3,m4,m5 =n3,n5,n2,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n3 n5 n2 n4 n1
                m1,m2,m3,m4,m5 =n3,n5,n2,n4,n1
                print(m1,m2,m3,m4,m5)
        elif n4<n1 and n4<n2: #n3 n5 n4
            if n1<n2: #n3 n5 n4 n1 n2
                m1,m2,m3,m4,m5 =n3,n5,n4,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n3 n5 n4 n2 n1
                m1,m2,m3,m4,m5 =n3,n5,n4,n2,n1
                print(m1,m2,m3,m4,m5)
elif n4<n1 and n4<n2 and n4<n3 and n4<n5:#n4
    if n1<n2 and n1<n3 and n1<n5: #n4 n1
        if n2<n3 and n2<n5: #n4 n1 n2
            if n3<n5: #n4 n1 n2 n3 n5
                m1,m2,m3,m4,m5 =n4,n1,n2,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n4 n1 n2 n5 n3
                m1,m2,m3,m4,m5 =n4,n1,n2,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n2 and n3<n5: #n4 n1 n3
            if n2<n5: #n4 n1 n3 n2 n5
                m1,m2,m3,m4,m5 =n4,n1,n3,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n4 n1 n3 n5 n2
                m1,m2,m3,m4,m5 =n4,n1,n3,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n5<n2 and n5<n3: #n4 n1 n5
            if n2<n3: #n4 n1 n5 n2 n3
                m1,m2,m3,m4,m5 =n4,n1,n5,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2: #n4 n1 n5 n3 n2
                m1,m2,m3,m4,m5 =n4,n1,n5,n3,n2
                print(m1,m2,m3,m4,m5)
    elif n2<n1 and n2<n3 and n2<n5: #n4 n2
        if n1<n3 and n1<n5: #n4 n2 n1
            if n3<n5: #n4 n2 n1 n3 n5
                m1,m2,m3,m4,m5 =n4,n2,n1,n3,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n3: #n4 n2 n1 n5 n3
                m1,m2,m3,m4,m5 =n4,n2,n1,n5,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n5: #n4 n2 n3
            if n1<n5: #n4 n2 n3 n1 n5
                m1,m2,m3,m4,m5 =n4,n2,n3,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n4 n2 n3 n5 n1
                m1,m2,m3,m4,m5 =n4,n2,n3,n5,n1
                print(m1,m2,m3,m4,m5)
        elif n5<n1 and n5<n3: #n4 n2 n5
            if n1<n3: #n4 n2 n5 n1 n3
                m1,m2,m3,m4,m5 =n4,n2,n5,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n4 n2 n5 n3 n1
                m1,m2,m3,m4,m5 =n4,n2,n5,n3,n1
                print(m1,m2,m3,m4,m5)
    elif n3<n1 and n3<n2 and n3<n5: #n4 n3
        if n1<n2 and n1<n5: #n4 n3 n1
            if n2<n5: #n4 n3 n1 n2 n5
                m1,m2,m3,m4,m5 =n4,n3,n1,n2,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n2: #n4 n3 n1 n5 n2
                m1,m2,m3,m4,m5 =n4,n3,n1,n5,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n5: #n4 n3 n2
            if n1<n5: #n4 n3 n2 n1 n5
                m1,m2,m3,m4,m5 =n4,n3,n2,n1,n5
                print(m1,m2,m3,m4,m5)
            elif n5<n1: #n4 n3 n2 n5 n1
                m1,m2,m3,m4,m5 =n4,n3,n2,n5,n1
                print(m1,m2,m3,m4,m5)
        elif n5<n1 and n5<n2: #n4 n3 n5
            if n1<n2: #n4 n3 n5 n1 n2
                m1,m2,m3,m4,m5 =n4,n3,n5,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n4 n3 n5 n2 n1
                m1,m2,m3,m4,m5 =n4,n3,n5,n2,n1
                print(m1,m2,m3,m4,m5)
    elif n5<n1 and n5<n2 and n5<n3: #n4 n5
        if n1<n2 and n1<n3: #n4 n5 n1
            if n2<n3: #n4 n5 n1 n2 n3
                m1,m2,m3,m4,m5 =n4,n5,n1,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2: #n4 n5 n1 n3 n2
                m1,m2,m3,m4,m5 =n4,n5,n1,n3,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n3: #n4 n5 n2
            if n1<n3: #n4 n5 n2 n1 n3
                m1,m2,m3,m4,m5 =n4,n5,n2,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n4 n5 n2 n3 n1
                m1,m2,m3,m4,m5 =n4,n5,n2,n3,n1
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n2: #n4 n5 n3
            if n1<n2: #n4 n5 n3 n1 n2
                m1,m2,m3,m4,m5 =n4,n5,n3,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n4 n5 n3 n2 n1
                m1,m2,m3,m4,m5 =n4,n5,n3,n2,n1
                print(m1,m2,m3,m4,m5)
elif n5<n1 and n5<n2 and n5<n3 and n5<n4: #n5
    if n1<n2 and n1<n3 and n1<n4: #n5 n1
        if n2<n3 and n2<n4: #n5 n1 n2
            if n3<n4: #n5 n1 n2 n3 n4
                m1,m2,m3,m4,m5 =n5,n1,n2,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n5 n1 n2 n4 n3
                m1,m2,m3,m4,m5 =n5,n1,n2,n4,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n2 and n3<n4: #n5 n1 n3
            if n2<n4: #n5 n1 n3 n2 n4
                m1,m2,m3,m4,m5 =n5,n1,n3,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n5 n1 n3 n4 n2
                m1,m2,m3,m4,m5 =n5,n1,n3,n4,n2
                print(m1,m2,m3,m4,m5)
        elif n4<n2 and n4<n3: #n5 n1 n4
            if n2<n3: #n5 n1 n4 n2 n3
                m1,m2,m3,m4,m5 =n5,n1,n4,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2: #n5 n1 n4 n3 n2
                m1,m2,m3,m4,m5 =n5,n1,n4,n3,n2
                print(m1,m2,m3,m4,m5)
    elif n2<n1 and n2<n3 and n2<n4: #n5 n2
        if n1<n3 and n1<n4:#n5 n2 n1
            if n3<n4: #n5 n2 n1 n3 n4
                m1,m2,m3,m4,m5 =n5,n2,n1,n3,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n3: #n5 n2 n1 n4 n3
                m1,m2,m3,m4,m5 =n5,n2,n1,n4,n3
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n4: #n5 n2 n3
            if n1<n4: #n5 n2 n3 n1 n4
                m1,m2,m3,m4,m5 =n5,n2,n3,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n5 n2 n3 n4 n1
                m1,m2,m3,m4,m5 =n5,n2,n3,n4,n1
                print(m1,m2,m3,m4,m5)
        elif n4<n1 and n4<n3: #n5 n2 n4
            if n1<n3: #n5 n2 n4 n1 n3
                m1,m2,m3,m4,m5 =n5,n2,n4,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n5 n2 n4 n3 n1
                m1,m2,m3,m4,m5 =n5,n2,n4,n3,n1
                print(m1,m2,m3,m4,m5)
    elif n3<n1 and n3<n2 and n3<n4: #n5 n3
        if n1<n2 and n1<n4: #n5 n3 n1
            if n2<n4: #n5 n3 n1 n2 n4
                m1,m2,m3,m4,m5 =n5,n3,n1,n2,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n2: #n5 n3 n1 n4 n2
                m1,m2,m3,m4,m5 =n5,n3,n1,n4,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n4: #n5 n3 n2
            if n1<n4: #n5 n3 n2 n1 n4
                m1,m2,m3,m4,m5 =n5,n3,n2,n1,n4
                print(m1,m2,m3,m4,m5)
            elif n4<n1: #n5 n3 n2 n4 n1
                m1,m2,m3,m4,m5 =n5,n3,n2,n4,n1
                print(m1,m2,m3,m4,m5)
        elif n4<n1 and n4<n2: #n5 n3 n4
            if n1<n2: #n5 n3 n4 n1 n2
                m1,m2,m3,m4,m5 =n5,n3,n4,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n5 n3 n4 n2 n1
                m1,m2,m3,m4,m5 =n5,n3,n4,n2,n1
                print(m1,m2,m3,m4,m5)
    elif n4<n1 and n4<n2 and n4<n3: #n5 n4
        if n1<n2 and n1<n3: #n5 n4 n1
            if n2<n3: #n5 n4 n1 n2 n3
                m1,m2,m3,m4,m5 =n5,n4,n1,n2,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n2: #n5 n4 n1 n3 n2
                m1,m2,m3,m4,m5 =n5,n4,n1,n3,n2
                print(m1,m2,m3,m4,m5)
        elif n2<n1 and n2<n3: #n5 n4 n2
            if n1<n3: #n5 n4 n2 n1 n3
                m1,m2,m3,m4,m5 =n5,n4,n2,n1,n3
                print(m1,m2,m3,m4,m5)
            elif n3<n1: #n5 n4 n2 n3 n1
                m1,m2,m3,m4,m5 =n5,n4,n2,n3,n1
                print(m1,m2,m3,m4,m5)
        elif n3<n1 and n3<n2: #n5 n4 n3
            if n1<n2: #n5 n4 n3 n1 n2
                m1,m2,m3,m4,m5 =n5,n4,n3,n1,n2
                print(m1,m2,m3,m4,m5)
            elif n2<n1: #n5 n4 n3 n2 n1
                m1,m2,m3,m4,m5 =n5,n4,n3,n2,n1
                print(m1,m2,m3,m4,m5)


#Ordenar los números de forma descendente
print("5) Los números organizados de mayor a menor se ve de la siguiente manera: ")
if n1<n2 and n1<n3 and n1<n4 and n1<n5: #n1
    if n2<n3 and n2<n4 and n2<n5: #n1 n2
        if n3<n4 and n3<n5: #n1 n2 n3
            if n4<n5: #n1 n2 n3 n4
                m1,m2,m3,m4,m5 =n1,n2,n3,n4,n5 #n1 n2 n3 n4 n5
                print(m5,m4,m3,m2,m1)
            elif n5<n4: #n1 n2 n3 n5
                m1,m2,m3,m4,m5 =n1,n2,n3,n5,n4 #n1 n2 n3 n5 n4
                print(m5,m4,m3,m2,m1)
        elif n4<n3 and n4<n5: #n1 n2 n4
            if n3<n5: #n1 n2 n4 n3 n5
                m1,m2,m3,m4,m5 =n1,n2,n4,n3,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n3: #n1 n2 n4 n5 n3
                m1,m2,m3,m4,m5 =n1,n2,n4,n5,n3
                print(m5,m4,m3,m2,m1)
        elif n5<n3 and n5<n4: #n1 n2 n5
            if n3<n4: #n1 n2 n5 n3 n4
                m1,m2,m3,m4,m5 =n1,n2,n5,n3,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n3: #n1 n2 n5 n4 n3
                m1,m2,m3,m4,m5 =n1,n2,n5,n4,n3
                print(m5,m4,m3,m2,m1)
    elif n3<n2 and n3<n4 and n3<n5: #n1 n3
        if n2<n4 and n2<n5: #n1 n3 n2
            if n4<n5: #n1 n3 n2 n4 n5
                m1,m2,m3,m4,m5 =n1,n3,n2,n4,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n4: #n1 n3 n2 n5 n4
                m1,m2,m3,m4,m5 =n1,n3,n2,n5,n4
                print(m5,m4,m3,m2,m1)
        elif n4<n2 and n4<n5: #n1 n3 n4
            if n2<n5: #n1 n3 n4 n2 n5
                m1,m2,m3,m4,m5 =n1,n3,n4,n2,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n2: #n1 n3 n4 n5 n2
                m1,m2,m3,m4,m5 =n1,n3,n4,n5,n2
                print(m5,m4,m3,m2,m1)
        elif n5<n2 and n5<n4: #n1 n3 n5
            if n2<n4: #n1 n3 n5 n2 n4
                m1,m2,m3,m4,m5 =n1,n3,n5,n2,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n2: #n1 n3 n5 n4 n2
                m1,m2,m3,m4,m5 =n1,n3,n5,n4,n2
                print(m5,m4,m3,m2,m1)
    elif n4<n2 and n4<n3 and n4<n5: #n1 n4
        if n2<n3 and n2<n5: #n1 n4 n2
            if n3<n5: #n1 n4 n2 n3 n5
                m1,m2,m3,m4,m5 =n1,n4,n2,n3,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n3: #n1 n4 n2 n5 n3
                m1,m2,m3,m4,m5 =n1,n4,n2,n5,n3
                print(m5,m4,m3,m2,m1)
        elif n3<n2 and n3<n5: #n1 n4 n3
            if n2<n5:#n1 n4 n3 n2 n5
                m1,m2,m3,m4,m5 =n1,n4,n3,n2,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n2: #n1 n4 n3 n5 n2
                m1,m2,m3,m4,m5 =n1,n4,n3,n5,n2
                print(m5,m4,m3,m2,m1)
        elif n5<n2 and n5<n3: #n1 n4 n5
            if n2<n3: #n1 n4 n5 n2 n3
                m1,m2,m3,m4,m5 =n1,n4,n5,n2,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n2: #n1 n4 n5 n3 n2
                m1,m2,m3,m4,m5 =n1,n4,n5,n3,n2
                print(m5,m4,m3,m2,m1)
    elif n5<n2 and n5<n3 and n5<n4: #n1 n5
        if n2<n3 and n2<n4: #n1 n5 n2
            if n3<n4: #n1 n5 n2 n3 n4
                m1,m2,m3,m4,m5 =n1,n5,n2,n3,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n3: #n1 n5 n2 n4 n3
                m1,m2,m3,m4,m5 =n1,n5,n2,n4,n3
                print(m5,m4,m3,m2,m1)
        elif n3<n2 and n3<n4: #n1 n5 n3
            if n2<n4:#n1 n5 n3 n2 n4
                m1,m2,m3,m4,m5 =n1,n5,n3,n2,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n2: #n1 n5 n3 n4 n2
                m1,m2,m3,m4,m5 =n1,n5,n3,n4,n2
                print(m5,m4,m3,m2,m1)
        elif n4<n2 and n4<n3: #n1 n5 n4
            if n2<n3:#n1 n5 n4 n2 n3
                m1,m2,m3,m4,m5 =n1,n5,n4,n2,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n2:#n1 n5 n4 n3 n2
                m1,m2,m3,m4,m5 =n1,n5,n4,n3,n2
                print(m5,m4,m3,m2,m1)
elif n2<n1 and n2<n3 and n2<n4 and n2<n5: #n2
    if n1<n3 and n1<n4 and n1<n5: #n2 n1
        if n3<n4 and n3<n5: #n2 n1 n3
            if n4<n5: #n2 n1 n3 n4 n5
                m1,m2,m3,m4,m5 =n2,n1,n3,n4,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n4: #n2 n1 n3 n5 n4
                m1,m2,m3,m4,m5 =n2,n1,n3,n5,n4
                print(m5,m4,m3,m2,m1)
        elif n4<n3 and n4<n5: #n2 n1 n4
            if n3<n5: #n2 n1 n4 n3 n5
                m1,m2,m3,m4,m5 =n2,n1,n4,n3,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n3: #n2 n1 n4 n5 n3
                m1,m2,m3,m4,m5 =n2,n1,n4,n5,n3
                print(m5,m4,m3,m2,m1)
        elif n5<n3 and n5<n4: #n2 n1 n5
            if n3<n4: #n2 n1 5n n3 n4
                m1,m2,m3,m4,m5 =n2,n1,n5,n3,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n3: #n2 n1 n5 n4 n3
                m1,m2,m3,m4,m5 =n2,n1,n5,n4,n3
                print(m5,m4,m3,m2,m1)
    elif n3<n1 and n3<n4 and n3<n5: #n2 n3
        if n1<n4 and n1<n5: #n2 n3 n1
            if n4<n5: #n2 n3 n1 n4 n5
                m1,m2,m3,m4,m5 =n2,n3,n1,n4,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n4: #n2 n3 n1 n5 n4
                m1,m2,m3,m4,m5 =n2,n3,n1,n5,n4
                print(m5,m4,m3,m2,m1)
        elif n4<n1 and n4<n5: #n2 n3 n4
            if n1<n5: #n2 n3 n4 n1 n5
                m1,m2,m3,m4,m5 =n2,n3,n4,n1,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n1: #n2 n3 n4 n5 n1
                m1,m2,m3,m4,m5 =n2,n3,n4,n5,n1
                print(m5,m4,m3,m2,m1)
        elif n5<n1 and n5<n4: #n2 n3 n5
            if n1<n4: #n2 n3 n5 n1 n4
                m1,m2,m3,m4,m5 =n2,n3,n5,n1,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n1: #n2 n3 n5 n4 n1
                m1,m2,m3,m4,m5 =n2,n3,n5,n4,n1
                print(m5,m4,m3,m2,m1)
    elif n4<n1 and n4<n3 and n4<n5: #n2 n4
        if n1<n3 and n1<n5:#n2 n4 n1
            if n3<n5: #n2 n4 n1 n3 n5
                m1,m2,m3,m4,m5 =n2,n4,n1,n3,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n3: #n2 n4 n1 n5 n3
                m1,m2,m3,m4,m5 =n2,n4,n1,n5,n3
                print(m5,m4,m3,m2,m1)
        elif n3<n1 and n3<n5: #n2 n4 n3
            if n1<n5: #n2 n4 n3 n1 n5
                m1,m2,m3,m4,m5 =n2,n4,n3,n1,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n1: #n2 n4 n3 n5 n1
                m1,m2,m3,m4,m5 =n2,n4,n3,n5,n1
                print(m5,m4,m3,m2,m1)
        elif n5<n1 and n5<n3: #n2 n4 n5
            if n1<n3:#n2 n4 n5 n1 n3
                m1,m2,m3,m4,m5 =n2,n4,n5,n1,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n1: #n2 n4 n5 n3 n1
                m1,m2,m3,m4,m5 =n2,n4,n5,n3,n1
                print(m5,m4,m3,m2,m1)
    elif n5<n1 and n5<n3 and n5<n4: #n2 n5
        if n1<n3 and n1<n4: #n2 n5 n1
            if n3<n4: #n2 n5 n1 n3 n4
                m1,m2,m3,m4,m5 =n2,n5,n1,n3,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n3: #n2 n5 n1 n4 n3
                m1,m2,m3,m4,m5 =n2,n5,n1,n4,n3
                print(m5,m4,m3,m2,m1)
        elif n3<n1 and n3<n4: #n2 n5 n3
            if n1<n4: #n2 n5 n3 n1 n4
                m1,m2,m3,m4,m5 =n2,n5,n3,n1,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n1: #n2 n5 n3 n4 n1
                m1,m2,m3,m4,m5 =n2,n5,n3,n4,n1
                print(m5,m4,m3,m2,m1)
        elif n4<n1 and n4<n3: #n2 n5 n4
            if n1<n3: #n2 n5 n4 n1 n3
                m1,m2,m3,m4,m5 =n2,n5,n4,n1,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n1: #n2 n5 n4 n3 n1
                m1,m2,m3,m4,m5 =n2,n5,n4,n3,n1
                print(m5,m4,m3,m2,m1)
elif n3<n1 and n3<n2 and n3<n4 and n3<n5:#n3
    if n1<n2 and n1<n4 and n1<n5: #n3 n1
        if n2<n4 and n2<n5: #n3 n1 n2
            if n4<n5: #n3 n1 n2 n4 n5
                m1,m2,m3,m4,m5 =n3,n1,n2,n4,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n4: #n3 n1 n2 n5 n4
                m1,m2,m3,m4,m5 =n3,n1,n2,n5,n4
                print(m5,m4,m3,m2,m1)
        elif n4<n2 and n4<n5: #n3 n1 n4
            if n2<n5: #n3 n1 n4 n2 n5
                m1,m2,m3,m4,m5 =n3,n1,n4,n2,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n2: #n3 n1 n4 n5 n2
                m1,m2,m3,m4,m5 =n3,n1,n4,n5,n2
                print(m5,m4,m3,m2,m1)
        elif n5<n2 and n5<n4: #n3 n1 n5
            if n2<n4: #n3 n1 n5 n2 n4
                m1,m2,m3,m4,m5 =n3,n1,n5,n2,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n2: #n3 n1 n5 n4 n2
                m1,m2,m3,m4,m5 =n3,n1,n5,n4,n2
                print(m5,m4,m3,m2,m1)
    elif n2<n1 and n2<n4 and n2<n5: #n3 n2
        if n1<n4 and n1<n5: #n3 n2 n1
            if n4<n5: #n3 n2 n1 n4 n5
                m1,m2,m3,m4,m5 =n3,n2,n1,n4,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n4: #n3 n2 n1 n5 n4
                m1,m2,m3,m4,m5 =n3,n2,n1,n5,n4
                print(m5,m4,m3,m2,m1)
        if n4<n1 and n4<n5: #n3 n2 n4
            if n1<n5: #n3 n2 n4 n1 n5
                m1,m2,m3,m4,m5 =n3,n2,n4,n1,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n1: #n3 n2 n4 n5 n1
                m1,m2,m3,m4,m5 =n3,n2,n4,n5,n1
                print(m5,m4,m3,m2,m1)
        if n5<n1 and n5<n4: #n3 n2 n5
            if n1<n4: #n3 n2 n5 n1 n4
                m1,m2,m3,m4,m5 =n3,n2,n5,n1,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n1: #n3 n2 n5 n4 n1
                m1,m2,m3,m4,m5 =n3,n2,n5,n4,n1
                print(m5,m4,m3,m2,m1)
    elif n4<n1 and n4<n2 and n4<n5: #n3 n4
        if n1<n2 and n1<n5: #n3 n4 n1
            if n2<n5: #n3 n4 n1 n2 n5
                m1,m2,m3,m4,m5 =n3,n4,n1,n2,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n2: #n3 n4 n1 n5 n2
                m1,m2,m3,m4,m5 =n3,n4,n1,n5,n2
                print(m5,m4,m3,m2,m1)
        elif n2<n1 and n2<n5: #n3 n4 n2
            if n1<n5: #n3 n4 n2 n1 n5
                m1,m2,m3,m4,m5 =n3,n4,n2,n1,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n1: #n3 n4 n2 n5 n1
                m1,m2,m3,m4,m5 =n3,n4,n2,n5,n1
                print(m5,m4,m3,m2,m1)
        elif n5<n1 and n5<n2: #n3 n4 n5
            if n1<n2: #n3 n4 n5 n1 n2
                m1,m2,m3,m4,m5 =n3,n4,n5,n1,n2
                print(m5,m4,m3,m2,m1)
            elif n2<n1: #n3 n4 n5 n2 n1
                m1,m2,m3,m4,m5 =n3,n4,n5,n2,n1
                print(m5,m4,m3,m2,m1)
    elif n5<n1 and n5<n2 and n5<n4: #n3 n5
        if n1<n2 and n1<n4: #n3 n5 n1
            if n2<n4: #n3 n5 n1 n2 n4
                m1,m2,m3,m4,m5 =n3,n5,n1,n2,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n2: #n3 n5 n1 n4 n2
                m1,m2,m3,m4,m5 =n3,n5,n1,n4,n2
                print(m5,m4,m3,m2,m1)
        elif n2<n1 and n2<n4: #n3 n5 n2
            if n1<n4: #n3 n5 n2 n1 n4
                m1,m2,m3,m4,m5 =n3,n5,n2,n1,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n1: #n3 n5 n2 n4 n1
                m1,m2,m3,m4,m5 =n3,n5,n2,n4,n1
                print(m5,m4,m3,m2,m1)
        elif n4<n1 and n4<n2: #n3 n5 n4
            if n1<n2: #n3 n5 n4 n1 n2
                m1,m2,m3,m4,m5 =n3,n5,n4,n1,n2
                print(m5,m4,m3,m2,m1)
            elif n2<n1: #n3 n5 n4 n2 n1
                m1,m2,m3,m4,m5 =n3,n5,n4,n2,n1
                print(m5,m4,m3,m2,m1)
elif n4<n1 and n4<n2 and n4<n3 and n4<n5:#n4
    if n1<n2 and n1<n3 and n1<n5: #n4 n1
        if n2<n3 and n2<n5: #n4 n1 n2
            if n3<n5: #n4 n1 n2 n3 n5
                m1,m2,m3,m4,m5 =n4,n1,n2,n3,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n3: #n4 n1 n2 n5 n3
                m1,m2,m3,m4,m5 =n4,n1,n2,n5,n3
                print(m5,m4,m3,m2,m1)
        elif n3<n2 and n3<n5: #n4 n1 n3
            if n2<n5: #n4 n1 n3 n2 n5
                m1,m2,m3,m4,m5 =n4,n1,n3,n2,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n2: #n4 n1 n3 n5 n2
                m1,m2,m3,m4,m5 =n4,n1,n3,n5,n2
                print(m5,m4,m3,m2,m1)
        elif n5<n2 and n5<n3: #n4 n1 n5
            if n2<n3: #n4 n1 n5 n2 n3
                m1,m2,m3,m4,m5 =n4,n1,n5,n2,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n2: #n4 n1 n5 n3 n2
                m1,m2,m3,m4,m5 =n4,n1,n5,n3,n2
                print(m5,m4,m3,m2,m1)
    elif n2<n1 and n2<n3 and n2<n5: #n4 n2
        if n1<n3 and n1<n5: #n4 n2 n1
            if n3<n5: #n4 n2 n1 n3 n5
                m1,m2,m3,m4,m5 =n4,n2,n1,n3,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n3: #n4 n2 n1 n5 n3
                m1,m2,m3,m4,m5 =n4,n2,n1,n5,n3
                print(m5,m4,m3,m2,m1)
        elif n3<n1 and n3<n5: #n4 n2 n3
            if n1<n5: #n4 n2 n3 n1 n5
                m1,m2,m3,m4,m5 =n4,n2,n3,n1,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n1: #n4 n2 n3 n5 n1
                m1,m2,m3,m4,m5 =n4,n2,n3,n5,n1
                print(m5,m4,m3,m2,m1)
        elif n5<n1 and n5<n3: #n4 n2 n5
            if n1<n3: #n4 n2 n5 n1 n3
                m1,m2,m3,m4,m5 =n4,n2,n5,n1,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n1: #n4 n2 n5 n3 n1
                m1,m2,m3,m4,m5 =n4,n2,n5,n3,n1
                print(m5,m4,m3,m2,m1)
    elif n3<n1 and n3<n2 and n3<n5: #n4 n3
        if n1<n2 and n1<n5: #n4 n3 n1
            if n2<n5: #n4 n3 n1 n2 n5
                m1,m2,m3,m4,m5 =n4,n3,n1,n2,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n2: #n4 n3 n1 n5 n2
                m1,m2,m3,m4,m5 =n4,n3,n1,n5,n2
                print(m5,m4,m3,m2,m1)
        elif n2<n1 and n2<n5: #n4 n3 n2
            if n1<n5: #n4 n3 n2 n1 n5
                m1,m2,m3,m4,m5 =n4,n3,n2,n1,n5
                print(m5,m4,m3,m2,m1)
            elif n5<n1: #n4 n3 n2 n5 n1
                m1,m2,m3,m4,m5 =n4,n3,n2,n5,n1
                print(m5,m4,m3,m2,m1)
        elif n5<n1 and n5<n2: #n4 n3 n5
            if n1<n2: #n4 n3 n5 n1 n2
                m1,m2,m3,m4,m5 =n4,n3,n5,n1,n2
                print(m5,m4,m3,m2,m1)
            elif n2<n1: #n4 n3 n5 n2 n1
                m1,m2,m3,m4,m5 =n4,n3,n5,n2,n1
                print(m5,m4,m3,m2,m1)
    elif n5<n1 and n5<n2 and n5<n3: #n4 n5
        if n1<n2 and n1<n3: #n4 n5 n1
            if n2<n3: #n4 n5 n1 n2 n3
                m1,m2,m3,m4,m5 =n4,n5,n1,n2,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n2: #n4 n5 n1 n3 n2
                m1,m2,m3,m4,m5 =n4,n5,n1,n3,n2
                print(m5,m4,m3,m2,m1)
        elif n2<n1 and n2<n3: #n4 n5 n2
            if n1<n3: #n4 n5 n2 n1 n3
                m1,m2,m3,m4,m5 =n4,n5,n2,n1,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n1: #n4 n5 n2 n3 n1
                m1,m2,m3,m4,m5 =n4,n5,n2,n3,n1
                print(m5,m4,m3,m2,m1)
        elif n3<n1 and n3<n2: #n4 n5 n3
            if n1<n2: #n4 n5 n3 n1 n2
                m1,m2,m3,m4,m5 =n4,n5,n3,n1,n2
                print(m5,m4,m3,m2,m1)
            elif n2<n1: #n4 n5 n3 n2 n1
                m1,m2,m3,m4,m5 =n4,n5,n3,n2,n1
                print(m5,m4,m3,m2,m1)
elif n5<n1 and n5<n2 and n5<n3 and n5<n4: #n5
    if n1<n2 and n1<n3 and n1<n4: #n5 n1
        if n2<n3 and n2<n4: #n5 n1 n2
            if n3<n4: #n5 n1 n2 n3 n4
                m1,m2,m3,m4,m5 =n5,n1,n2,n3,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n3: #n5 n1 n2 n4 n3
                m1,m2,m3,m4,m5 =n5,n1,n2,n4,n3
                print(m5,m4,m3,m2,m1)
        elif n3<n2 and n3<n4: #n5 n1 n3
            if n2<n4: #n5 n1 n3 n2 n4
                m1,m2,m3,m4,m5 =n5,n1,n3,n2,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n2: #n5 n1 n3 n4 n2
                m1,m2,m3,m4,m5 =n5,n1,n3,n4,n2
                print(m5,m4,m3,m2,m1)
        elif n4<n2 and n4<n3: #n5 n1 n4
            if n2<n3: #n5 n1 n4 n2 n3
                m1,m2,m3,m4,m5 =n5,n1,n4,n2,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n2: #n5 n1 n4 n3 n2
                m1,m2,m3,m4,m5 =n5,n1,n4,n3,n2
                print(m5,m4,m3,m2,m1)
    elif n2<n1 and n2<n3 and n2<n4: #n5 n2
        if n1<n3 and n1<n4:#n5 n2 n1
            if n3<n4: #n5 n2 n1 n3 n4
                m1,m2,m3,m4,m5 =n5,n2,n1,n3,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n3: #n5 n2 n1 n4 n3
                m1,m2,m3,m4,m5 =n5,n2,n1,n4,n3
                print(m5,m4,m3,m2,m1)
        elif n3<n1 and n3<n4: #n5 n2 n3
            if n1<n4: #n5 n2 n3 n1 n4
                m1,m2,m3,m4,m5 =n5,n2,n3,n1,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n1: #n5 n2 n3 n4 n1
                m1,m2,m3,m4,m5 =n5,n2,n3,n4,n1
                print(m5,m4,m3,m2,m1)
        elif n4<n1 and n4<n3: #n5 n2 n4
            if n1<n3: #n5 n2 n4 n1 n3
                m1,m2,m3,m4,m5 =n5,n2,n4,n1,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n1: #n5 n2 n4 n3 n1
                m1,m2,m3,m4,m5 =n5,n2,n4,n3,n1
                print(m5,m4,m3,m2,m1)
    elif n3<n1 and n3<n2 and n3<n4: #n5 n3
        if n1<n2 and n1<n4: #n5 n3 n1
            if n2<n4: #n5 n3 n1 n2 n4
                m1,m2,m3,m4,m5 =n5,n3,n1,n2,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n2: #n5 n3 n1 n4 n2
                m1,m2,m3,m4,m5 =n5,n3,n1,n4,n2
                print(m5,m4,m3,m2,m1)
        elif n2<n1 and n2<n4: #n5 n3 n2
            if n1<n4: #n5 n3 n2 n1 n4
                m1,m2,m3,m4,m5 =n5,n3,n2,n1,n4
                print(m5,m4,m3,m2,m1)
            elif n4<n1: #n5 n3 n2 n4 n1
                m1,m2,m3,m4,m5 =n5,n3,n2,n4,n1
                print(m5,m4,m3,m2,m1)
        elif n4<n1 and n4<n2: #n5 n3 n4
            if n1<n2: #n5 n3 n4 n1 n2
                m1,m2,m3,m4,m5 =n5,n3,n4,n1,n2
                print(m5,m4,m3,m2,m1)
            elif n2<n1: #n5 n3 n4 n2 n1
                m1,m2,m3,m4,m5 =n5,n3,n4,n2,n1
                print(m5,m4,m3,m2,m1)
    elif n4<n1 and n4<n2 and n4<n3: #n5 n4
        if n1<n2 and n1<n3: #n5 n4 n1
            if n2<n3: #n5 n4 n1 n2 n3
                m1,m2,m3,m4,m5 =n5,n4,n1,n2,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n2: #n5 n4 n1 n3 n2
                m1,m2,m3,m4,m5 =n5,n4,n1,n3,n2
                print(m5,m4,m3,m2,m1)
        elif n2<n1 and n2<n3: #n5 n4 n2
            if n1<n3: #n5 n4 n2 n1 n3
                m1,m2,m3,m4,m5 =n5,n4,n2,n1,n3
                print(m5,m4,m3,m2,m1)
            elif n3<n1: #n5 n4 n2 n3 n1
                m1,m2,m3,m4,m5 =n5,n4,n2,n3,n1
                print(m5,m4,m3,m2,m1)
        elif n3<n1 and n3<n2: #n5 n4 n3
            if n1<n2: #n5 n4 n3 n1 n2
                m1,m2,m3,m4,m5 =n5,n4,n3,n1,n2
                print(m5,m4,m3,m2,m1)
            elif n2<n1: #n5 n4 n3 n2 n1
                m1,m2,m3,m4,m5 =n5,n4,n3,n2,n1
                print(m5,m4,m3,m2,m1)






#La potencia del mayor número elevado al menor número


pot = (m5)**(m1)
print("6) La potencia del amyor numero elevado al menor numero es: ",pot)


#La raíz cúbica del menor número


raiz = (m1)**(1/3)
print("7) La raiz cúbica del menor número es: ",raiz)
```
# 8) PIP
Consultar qué es y cómo funciona pip en python.

"Pip en python es un sistema de gestión de paquetes utilizado para instalar y administrar paquetes de software escritos en Python y descargarlos a nuestra computadora con la finalidad de integrarlos a nuestros desarrollos realizado en python."

Administrador de Paquetes PIP en Python. (s. f.). Grupo Codes - training & certification. Recuperado 23 de marzo de 2023, de https://www.buscaminegocio.com/cursos-de-python/pip-en-python.html

# 9) Módulos
Hacer un listado de módulos populares para python que se puedan instalar com pip y consultar cómo instalarlos.

"Si está utilizando Python 2.7.9 (o superior) o Python 3.4 (o superior), entonces PIP viene instalado con Python por defecto."

"Las siguientes instrucciones deberían funcionar en Windows 7, Windows 8.1 y Windows 10:

Descargue el script del instalador get-pip.py. Si estás en Python 3.2, necesitarás esta versión de get-pip.py. En caso de tener Python 3.3 o 3.4 usar estas versiones de PiP correspondientemente Python 3.3 get-pip.py o Python 3.4 get-pip.py. De cualquier manera, haga clic derecho en el enlace y seleccione Guardar como y guárdelo en cualquier carpeta del pc, como su carpeta de Descargas.

Abra el símbolo del sistema y navegue hasta el archivo get-pip.py.

Ejecute el siguiente comando: python get-pip.py"

Modulos:

- camelcase       
- mysql-connector 
- pip             
- pymongo         
- setuptools

Fernandez, D. P. (2022, 7 noviembre). ¿Cómo instalar PIP para Python en Windows, Mac y Linux? 【PASO A PASO】. Tecnonucleous. https://tecnonucleous.com/2018/01/28/como-instalar-pip-para-python-en-windows-mac-y-linux/
