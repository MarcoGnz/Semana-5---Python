# Curso Básico de Python

## 1. Introducción a Python
## Objetivo
Aplicar una instalacion correcta del lenguaje Python a traves de 5 sencillos pasos pasos. <br>
## *¿Qué es Python?*
Python es un lenguaje de programación interpretado, de alto nivel y propósito general. Fue creado por Guido van Rossum y lanzado por primera vez en 1991. Python es conocido por su sintaxis simple y fácil de leer, lo que lo hace ideal para principiantes, pero también es poderoso y ampliamente utilizado en la industria.

## Instalación de Python
*En Windows*
1. Ve a la página oficial de descargas de Python. (https://www.python.org/downloads/)
2. Descarga el instalador de Python adecuado para tu sistema operativo (por lo general, el de Windows x86-64).
3. Ejecuta el instalador y asegúrate de seleccionar la opción "Add Python to PATH" antes de hacer clic en "Install Now".

*En macOS*
1. Abre la Terminal.
2. Instala Homebrew (si no lo tienes ya) con el siguiente comando:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
3. Instala Python usando Homebrew:
```
brew install python
```
*En Linux*
1. Abre la terminal.
2. Usa el administrador de paquetes de tu distribución para instalar Python. Por ejemplo, en Ubuntu:
```
sudo apt update
sudo apt install python3
```

## Ejecución de Python
*Ejecutar scripts de Python*

Guarda tu código en un archivo con la extensión .py, por ejemplo, mi_programa.py. Luego, puedes ejecutar tu script desde la terminal o línea de comandos:
```
python mi_programa.py
```
*Uso del intérprete interactivo*
Puedes abrir una sesión interactiva de Python simplemente escribiendo python (o python3 en algunos sistemas) en tu terminal. Esto te permitirá escribir y ejecutar código Python línea por línea.

## 2. Uso de Variables
## Objetivo
Diferenciar entre distintos tipos de datos a traves de contenido teórico y ejercicios prácticos.

## 3. Uso de Variables
## Objetivo
Determinar el uso correcto de sentencias de control mediante situaciones de la vida real aplicados a código

## 4. Ciclos en Python
## Objetivo
Identificar la sintaxis y usos de los ciclos en el lenguaje Python mediante ejercicios prácticos

## 5. Funciones en Python
## Objetivo
Determinar el uso y creación de funciones en Python, incluyendo parámetros, argumentos y el concepto de retorno de valores, a través de ejemplos prácticos y teóricos.

# Ejercicios
## 1. Uso de Variables
Las variables son contenedores para almacenar valores. Puedes crear variables en Python simplemente asignándoles un valor con el operador =.
```python
# Crear variables
nombre = "Juan"
edad = 25
numero = 42

# Operaciones con variables
suma = edad + numero
print(f"La suma de {edad} y {numero} es {suma}")

```
## 2. Determinar si es Mayor de Edad
Solicita la edad del usuario y utiliza un comparador para verificar si es mayor de edad.
```python
edad = int(input("Ingresa tu edad: "))
if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")

```
## 3. Calcular la Estación del Mes
Solicita al usuario que ingrese un número de mes (1 a 12) y determina la estación del año correspondiente.
```python
mes = int(input("Ingresa el número del mes (1-12): "))

if mes in [12, 1, 2]:
    print("Es invierno.")
elif mes in [3, 4, 5]:
    print("Es primavera.")
elif mes in [6, 7, 8]:
    print("Es verano.")
elif mes in [9, 10, 11]:
    print("Es otoño.")
else:
    print("Mes no válido.")

```
## 4. Lanzamiento de Cohete
Implementa un ciclo while que cuente desde 10 hasta 1 y muestra un mensaje de lanzamiento.
```python
cuenta_regresiva = 10
while cuenta_regresiva > 0:
    print(cuenta_regresiva)
    cuenta_regresiva -= 1
print("¡Lanzamiento!")

```
## 5. Calculadora Python
Crea funciones para realizar operaciones matemáticas básicas y utiliza sentencias if para seleccionar la operación deseada.
```python
def suma(a, b):
    return a + b

def resta(a, b):
    return a - b

def multiplicacion(a, b):
    return a * b

def division(a, b):
    if b == 0:
        return "Error: División por cero."
    return a / b

operacion = input("Elige una operación (suma, resta, multiplicacion, division): ").lower()
num1 = float(input("Ingresa el primer número: "))
num2 = float(input("Ingresa el segundo número: "))

if operacion == "suma":
    print(f"El resultado es: {suma(num1, num2)}")
elif operacion == "resta":
    print(f"El resultado es: {resta(num1, num2)}")
elif operacion == "multiplicacion":
    print(f"El resultado es: {multiplicacion(num1, num2)}")
elif operacion == "division":
    print(f"El resultado es: {division(num1, num2)}")
else:
    print("Operación no válida.")

```
# Tareas
## 1. Gramática Básica de Python
Familiarízate con la sintaxis básica de Python:

- **Indentación**: Python usa la indentación para definir bloques de código.
- **Comentarios**: Los comentarios se añaden con #.
- **Variables y tipos de datos**: Python tiene varios tipos de datos integrados, como enteros (int), flotantes (float), cadenas (str), listas (list), etc.
```python
# Este es un comentario
x = 10  # Variable entera
y = 2.5  # Variable flotante
nombre = "Ana"  # Variable de cadena

print(x, y, nombre)  # Imprime las variables
```
## 2. Factorización de Python
Divide tu código en funciones reutilizables para mejorar la modularidad y organización.
```python
def saludar(nombre):
    return f"Hola, {nombre}!"

nombre_usuario = input("Ingresa tu nombre: ")
print(saludar(nombre_usuario))
```
## 3. Refactorización de Python
Revisa tu código existente buscando oportunidades para mejorarlo en términos de simplicidad, eficiencia y legibilidad.

**Ejemplo**
Antes de refactorización:
```python
x = 10
y = 20
z = 30
promedio = (x + y + z) / 3
print("El promedio es", promedio)
```
Después de refactorización:
```python
def calcular_promedio(*numeros):
    return sum(numeros) / len(numeros)

print(f"El promedio es {calcular_promedio(10, 20, 30)}")
```
# Exámenes
## 1. Serie de Introducción a los Algoritmos
Estudia conceptos básicos como bucles, condicionales y estructuras de datos.
**Ejemplo de bucle**
```python
for i in range(5):
    print(i)
```
**Ejemplo de condicional**
```python
numero = 10
if numero > 5:
    print("El número es mayor que 5.")
else:
    print("El número es 5 o menor.")
```
## 2. Visión General de Python y Serie de Funciones
Profundiza en características clave como listas, diccionarios y funciones.

**Ejemplo con listas**
```python
numeros = [1, 2, 3, 4, 5]
for numero in numeros:
    print(numero)
```
**Ejemplo con diccionarios**
```python
persona = {"nombre": "Ana", "edad": 25, "ciudad": "Madrid"}
print(persona["nombre"])
```
**Ejemplo de función**
```python
def sumar(a, b):
    return a + b

print(sumar(5, 3))
```
