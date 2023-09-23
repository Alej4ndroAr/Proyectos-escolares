# Apuntes 1er parcial
---
###### Andrade Romero Jesus Alejandro
-----------------------
## La programacion funcional
La programación funcional es un paradigma de programación que se basa en el concepto de funciones matemáticas y se enfoca en el tratamiento de datos como valores inmutables y en la aplicación de funciones para transformar esos datos.
##### Caracteristicas
-Enfoque Principal: 
Se centra en el uso de funciones como elementos fundamentales.
-Funciones Pura: 
Las funciones son puras, lo que significa que producen el mismo resultado para los mismos argumentos y no tienen efectos secundarios.
-Inmutabilidad: 
Se promueve la inmutabilidad de los datos siempre que sea posible, evitando la modificación de variables y promoviendo la creación de nuevos valores.
-Recursión: 
La recursión se utiliza en lugar de bucles para controlar el flujo del programa.
-----
#### Comparación de la programacion funcional con otros paradigmas de programacion:
Para esto utilizamos como ejemplo la elaboracion de una calculadora, la cual fue diferente para cada paradigma.
###### `Programacion Funcional:`
```python
  def suma(a, b):
 return a + b
def resta(a, b):
 return a - b
def multiplicacion(a, b):
 return a * b
def division(a, b):
 #validar el 0
 return a / b
def mi_calculadora(opcion, num1, num2):
    if opcion == '1':
        return suma(num1, num2)
    elif opcion == '2':
        return resta(num1, num2)
    elif opcion == '3':
        return multiplicacion(num1, num2)
    elif opcion == '4' and num2 != 0:
        return division(num1, num2)
    else:
        return "Opción no válida"
while True:
 print("\nMi Calculadora")
 print("1. Suma")
 print("2. Resta")
 print("3. Multiplicación")
 print("4. División")
 print("5. Salir")
 opcion = input("Selecciona una opción: ")
 if opcion == '5':
     print("¡Gracias por usar Mi Calculadora!")
     break
 elif opcion < '1' or opcion > '5':
             print("Opción no válida")
 else:
    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))
 resultado = mi_calculadora(opcion, num1, num2)
 print("Resultado:", resultado)
```
Este programa implementa una calculadora simple enfocada al paradigma `funcional` que permite al usuario realizar operaciones de "suma, resta, multiplicación y división" con dos números. También incluye una opción para salir del programa.

###### Funciones: 
Lo mas destacble de este paradiga son las `Funciones Puras` las cuales son las funciones de "suma, resta, multiplicacion, division, y mi_calculadora". Esto significa que su resultado depende únicamente de sus argumentos y no tienen efectos secundarios observables en el programa.

###### `Programacion estructurada:`
```python
while True:
 print("\nMi Calculadora")
 print("1. Suma")
 print("2. Resta")
 print("3. Multiplicación")
 print("4. División")
 print("5. Salir")
 opcion = input("Selecciona una opción: ")
 if opcion == '5':
    print("¡Hasta luego!")
    break
 elif opcion < '1' or opcion > '5':
        print("Opcion no valida")
 else:
    num1 = float(input("Ingresa el primer número: "))
    num2 = float(input("Ingresa el segundo número: "))
if opcion == '1':
    print("Resultado:", num1 + num2)
elif opcion == '2':
    print("Resultado:", num1 - num2)
elif opcion == '3':
    print("Resultado:", num1 * num2)
elif opcion == '4': 
     if num2 != 0:
        print("Resultado: ", num1 / num2)
     else:
       print("No se puede dividir entre cero")
else:
    print("¡Gracias por usar Mi Calculadora!")
```
Al igual que el programa anterior, este implementa una calculadora, pero ahora con un enfoque al paradigma `estructurado`.
###### Estructuras de control:
 En comparacion, este paradigma es que se basa en el uso de "estructuras de control" como secuencias,  `if, elif, y else` para tomar decisiones basadas en la entrada del usuario y ejecutar acciones específicas en función de esas decisiones. También utiliza un bucle `while` para mantener el programa en ejecución hasta que el usuario decida salir.

###### `Programación orientada a objetos (POO):`
```python
class MiCalculadora:
 def suma(self, a, b):
    return a + b
 def resta(self, a, b):
    return a - b
 def multiplicacion(self, a, b):
    return a * b
 def division(self, a, b):
    if b != 0:
        return a / b
    else:
        return "No se puede dividir entre cero"
calculadora = MiCalculadora()
while True:
    print("\nMi Calculadora")
    print("1. Suma")
    print("2. Resta")
    print("3. Multiplicación")
    print("4. División")
    print("5. Salir")
    opcion = input("Selecciona una opción: ")
    if opcion == '5':
        print("¡Gracias por usar Mi Calculadora!")
        break
    elif opcion < '1' or opcion > '5':
        print("Opción no válida")
    else:
        num1 = float(input("Ingresa el primer número: "))
        num2 = float(input("Ingresa el segundo número: "))
    if opcion == '1':
        print("Resultado:", calculadora.suma(num1, num2))
    elif opcion == '2':
        print("Resultado:", calculadora.resta(num1, num2))
    elif opcion == '3':
        print("Resultado:", calculadora.multiplicacion(num1, num2))
    elif opcion == '4': 
        if num2 != 0:
            print("Resultado:", calculadora.division(num1, num2))
        else:
            print("No se puede dividir entre cero")
```
Este codigo utiliza un enfoque de programación orientada a objetos (POO), lo que lo caracteriza es que los programas se organizan en "clases y objetos" que encapsulan datos y comportamientos relacionados.
###### Clases, objetos, encapsulacion, etc.:
- Clase: El código define una clase llamada `MiCalculadora`, La cual es una clase que se utiliza para crear objetos.
- Métodos de Clase: Dentro de la clase "MiCalculadora", se definen métodos como `suma, resta, multiplicacion, y division`. Estos métodos son funciones que operan en los atributos de los objetos de la clase. 
- Creación de Objetos: Se crea una instancia de la clase "MiCalculadora" mediante la línea `calculadora = MiCalculadora()`. Aquí, `calculadora` se convierte en un objeto de la clase MiCalculadora, y se pueden llamar a sus métodos para realizar operaciones matemáticas.
- Encapsulación: Los métodos de la clase MiCalculadora encapsulan la lógica de las operaciones matemáticas. Esto significa que la implementación de las operaciones está oculta dentro de la clase, y el usuario solo necesita llamar a los métodos correspondientes.
- Polimorfismo: El código muestra polimorfismo, ya que se pueden llamar a métodos con el mismo nombre (suma, resta, etc.) en diferentes objetos de la clase MiCalculadora


------------------
#### Tipos de datos:
Los tipos de datos son elementos fundamentales ya que te permiten almacenar y manipular diferentes tipos de información. 
###### `Tipos de Datos Numéricos:`

- **int**: Este tipo de dato se utiliza para representar números enteros, como -1, 0, 1, 2, etc. Los enteros en Python no tienen límites de tamaño, lo que significa que pueden ser tan grandes como la memoria lo permita.

- **float**: Los números de punto flotante se utilizan para representar números con decimales, como 3.14 o -0.001. Los números de punto flotante en Python siguen el estándar de punto flotante IEEE 754.

- **complex**: Los números complejos se utilizan para representar números complejos, que tienen una parte real y una parte imaginaria, como 3+2j.

###### `Tipo de Dato Decimal:`

- Python también tiene un tipo de dato decimal (`decimal`) que se utiliza para realizar cálculos de punto flotante con una precisión decimal fija. Es útil cuando se requiere una precisión exacta en cálculos financieros o científicos.

###### `Tipo de Dato Científico:`

- No existe un tipo de dato científico nativo en Python, pero puedes utilizar el tipo `float` para representar números en notación científica. Por ejemplo, `3.14e-10` representa 3.14 multiplicado por 10 elevado a la potencia negativa de 10.

###### `Tipo de Dato Lógico:`

- **bool**: Este tipo de dato se utiliza para representar valores booleanos, que pueden ser `True` (verdadero) o `False` (falso). Los valores booleanos se utilizan en expresiones lógicas y en el control de flujo de un programa para tomar decisiones.

###### `Tipo de Dato Cadena (String):`

- **str**: Las cadenas son secuencias de caracteres, como texto o palabras. Se utilizan para representar y manipular datos de texto. Las cadenas se pueden definir entre comillas simples (' '), comillas dobles (" "), o incluso comillas triples (''' ''' o """ """) para cadenas multilínea.
----------------------------------
#### Operadores:
###### `Operadores Aritméticos:`

- **+**: Suma
- **-**: Resta
- **\***: Multiplicación
- **/**: División
- **//**: División entera (resultado redondeado al número entero más cercano)
- **%**: Módulo (el residuo de la división)
- **\*\***: Potencia (por ejemplo, `2 ** 3` es igual a 2 elevado a la potencia de 3, es decir, 8)

Los operadores aritméticos se utilizan para realizar operaciones matemáticas en Python.

###### `Operadores Lógicos:`

- **and**: Operador lógico "y"
- **or**: Operador lógico "o"
- **not**: Operador lógico "no"

Los operadores lógicos se utilizan para combinar expresiones lógicas y evaluar condiciones en Python.

###### `Operadores Condicionales:`

- **==**: Igual a
- **!=**: No igual a
- **<**: Menor que
- **>**: Mayor que
- **<=**: Menor o igual que
- **>=**: Mayor o igual que
------------------------------------------------
#### Estructuras de datos:

###### `Listas (`list`):`

Las listas en Python son colecciones ordenadas y mutables de elementos. Puedes almacenar una variedad de tipos de datos en una lista y modificarla añadiendo, eliminando o modificando elementos. Las listas se definen utilizando corchetes `[]`.

###### `Diccionarios (`dict`):`

Los diccionarios son colecciones de pares clave-valor que se utilizan para mapear un valor (valor) a una clave (key). Son útiles cuando necesitas buscar un valor basado en una clave. Los diccionarios se definen utilizando llaves `{}`.

###### `Conjuntos (`set`):`

Los conjuntos son colecciones no ordenadas y mutables de elementos únicos. Se utilizan cuando necesitas almacenar elementos únicos y realizar operaciones de conjuntos, como unión e intersección. Los conjuntos se definen utilizando llaves `{}` o la función `set()`.

###### `Tuplas (`tuple`):`
 Las tuplas son colecciones ordenadas e inmutables de elementos. A diferencia de las listas, no se pueden modificar después de su creación. Las tuplas se definen utilizando paréntesis `()`.

-------------------------------------------------------------
#### Estructuras Condicionales:
###### `if:`

La declaración `if` se utiliza para realizar una acción si una condición es verdadera. Por ejemplo:

```python
if condicion:
    # Código a ejecutar si la condición es verdadera
```    
###### `if-else:`
La declaración if-else permite ejecutar un bloque de código si una condición es verdadera y otro bloque de código si la condición es falsa. Por ejemplo:
```python
if condicion:
    # Código a ejecutar si la condición es verdadera
else:
    # Código a ejecutar si la condición es falsa
``` 
###### `if-elif-...-else:` 
La declaración "if-elif-...-else" permite evaluar múltiples condiciones en secuencia y ejecutar el bloque de código del primer if o elif que sea verdadero. Si ninguno es verdadero, se ejecuta el bloque else.

------------------------------------------
#### Estructuras para Control de Flujo:

###### `Iterables e Iteradores:`

Los iterables son objetos que se pueden recorrer, como listas y tuplas. Los iteradores son objetos que permiten recorrer un iterable uno a uno, utilizando métodos como `next()`. Puedes crear iteradores personalizados implementando los métodos `__iter__()` y `__next__()`.

###### `Estructura for:`

El bucle `for` se utiliza para iterar sobre elementos en un iterable. Puedes recorrer listas, tuplas, diccionarios, y más utilizando un bucle `for`.

###### `Estructura while:`

El bucle `while` se utiliza para ejecutar un bloque de código repetidamente mientras una condición sea verdadera.

###### `Uso de range, break y continue:`

- `range()`: Se utiliza para generar secuencias de números.

- `break`: Se utiliza para salir de un bucle antes de que se complete.

- `continue`: Se utiliza para pasar a la siguiente iteración de un bucle sin ejecutar el resto del código en ese ciclo.
