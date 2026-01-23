# TIPOS DE DATOS Y ALGORITMOS APLICADOS I  
---

## 4.1 Números y secuencias

### Teoría

Los **números** son uno de los tipos de datos fundamentales en programación y algoritmia. Se utilizan para representar cantidades, realizar cálculos y modelar fenómenos reales.

**Tipos de números más comunes:**
- **Enteros (int):** números sin parte decimal.
- **Reales (float):** números con decimales.
- **Complejos (complex):** números con parte real e imaginaria. (numero_complejo = 3 + 4j)

Una **secuencia** es una colección ordenada de elementos numéricos, donde cada elemento ocupa una posición específica.

Ejemplos de secuencias:
- Arreglos (listas) | [10, 20, 30, 40]
- Rangos | range(inicio, fin, paso)
- Series numéricas | \[a_n = a_1 + (n - 1)d\]

### Ejercicios de Tipos de números más comunes

### Números Enteros (`int`)

### Tipo de número entero (int)

```python
a = int(input("Ingresa el primer entero: "))
b = int(input("Ingresa el segundo entero: "))

print("Suma:", a + b)
print("Resta:", a - b)
print("Producto:", a * b)
```
### Tipo de número entero (float)
```python
import math

radio = float(input("Ingresa el radio: "))
area = math.pi * radio**2

print("Área del círculo:", area)
```

### Tipo de número entero (complejos)
```python
z1 = 3 + 4j
z2 = 1 + 2j

print("Suma:", z1 + z2)
print("Resta:", z1 - z2)
```
### Arreglos (listas)

```python
# Arreglo (lista) de ejemplo
arreglo = [10, 20, 30, 40]

print("Arreglo:", arreglo)
print("Primer elemento:", arreglo[0])
print("Último elemento:", arreglo[-1])

# Operaciones básicas
arreglo.append(50)          # Agregar al final
arreglo.insert(1, 15)       # Insertar en posición 1
arreglo.remove(30)          # Eliminar por valor
arreglo[2] = 200            # Modificar por índice

print("Arreglo modificado:", arreglo)
print("Longitud:", len(arreglo))

```
### Range (range(inicio, fin, paso))

- **inicio:** número inicial (incluido)
- **fin:** número final (no incluido)
- **paso:** incremento (opcional)

```python
for i in range(1, 6):
    print(i)
```

### Complejos (complex) ###
- Su parte real
- Su parte imaginaria
- Su módulo

  z = complex(3, 4)

```python
print("Parte real:", z.real)
print("Parte imaginaria:", z.imag)
print("Módulo:", abs(z))
```

### 4.2 Conjuntos y cadenas de caracteres ###
Un **conjunto (set)** es una colección no ordenada de elementos únicos, es decir, no permite duplicados.
Una **cadena de caracteres (string)** es una secuencia de símbolos que representa texto.

### Características principales: ###

Los conjuntos permiten operaciones matemáticas como unión e intersección.
Las cadenas permiten manipulación de texto (concatenar, dividir, buscar).

### Operaciones con Conjuntos en Python ###

A continuación se muestran ejemplos básicos de las operaciones más comunes entre conjuntos: unión, intersección y diferencia, usando sintaxis de Python.

### Unión (A ∪ B) ###
Combina todos los elementos de ambos conjuntos sin duplicados.

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

union_1 = A | B
union_2 = A.union(B)

print("Unión (|):", union_1)
print("Unión (.union):", union_2)
```

### Intersección (A ∩ B) ###
Devuelve los elementos que están en ambos conjuntos.

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

inter_1 = A & B
inter_2 = A.intersection(B)

print("Intersección (&):", inter_1)
print("Intersección (.intersection):", inter_2)
```

### Diferencia (A − B) ###
Elementos que están en A pero no en B.

```python
A = {1, 2, 3, 4}
B = {3, 4, 5, 6}

dif_1 = A - B
dif_2 = A.difference(B)

print("Diferencia A - B:", dif_1)
print("Diferencia (.difference):", dif_2)
```

### Manipulación de Cadenas en Python ###
Las cadenas (str) en Python permiten operaciones como concatenar, dividir, buscar, entre muchas otras.
Aquí tienes ejemplos básicos y muy usados.

### 1. Concatenar cadenas ###

```python
texto1 = "Hola"
texto2 = "Mundo"

# Concatenación con +
resultado = texto1 + " " + texto2
print(resultado)

# Concatenación con f-strings (más moderno)
resultado2 = f"{texto1} {texto2}"
print(resultado2)
```
### 2. Dividir cadenas (split) ###
```python
frase = "manzana,pera,uva,mango"

# Divide usando coma como separador
lista_frutas = frase.split(",")

print(lista_frutas)   # ['manzana', 'pera', 'uva', 'mango']
```
### 3. Buscar dentro de una cadena ###
```python
texto = "Programar en Python es divertido."

# Buscar posición de una palabra
pos = texto.find("Python")
print("Posición de 'Python':", pos)

# Verificar si una palabra está en la cadena
existe = "Python" in texto
print("¿Está 'Python'? :",
```

### 4. Reemplazar texto (replace) ###
```python
mensaje = "Hola mundo"
nuevo = mensaje.replace("mundo", "Python")

print(nuevo)  # Hola Python
```

### 5. Cambiar mayúsculas/minúsculas ###
```python
cadena = "Python es Genial"

print(cadena.upper())     # MAYÚSCULAS
print(cadena.lower())     # minúsculas
print(cadena.title())     # Estilo Título
print(cadena.capitalize()) # Solo primera letra en mayúscula
```

### 6. Eliminar espacios (strip) ###
```python

texto = "   hola python   "

print(texto.strip())   # elimina espacios al inicio y fin
print(texto.lstrip())  # elimina espacios a la izquierda
print(texto.rstrip())  # elimina espacios a la derecha
```

### 7. Cortar subcadenas (slicing) ###
```python

texto = "ABCDEFGHIJK"

print(texto[0:4])   # ABCD
print(texto[5:])    # FGHIJK
print(texto[:3])    # ABC
print(texto[-3:])   # IJK
```

### 8. Contar ocurrencias ###
```python

frase = "banana"

print(frase.count("a"))  # 3

```

### 9. Unir cadenas (join) ###
```python

palabras = ["Hola", "mundo", "Python"]

resultado = " ".join(palabras)
print(resultado)   # Hola mundo Python

```
### Tabla Resumen de Manipulación de Cadenas en Python ###

| Operación                | Descripción                                    | Ejemplo Simplificado                           |
|--------------------------|------------------------------------------------|-------------------------------------------------|
| Concatenar               | Une dos o más cadenas                          | `"Hola" + " Mundo"`                            |
| Concatenar (f-string)    | Inserta variables dentro de una cadena         | `f"{nombre} {apellido}"`                       |
| Dividir (split)          | Separa la cadena según un separador            | `"a,b,c".split(",")`                           |
| Buscar (find)            | Devuelve la posición de una subcadena          | `"Hola".find("la")`                             |
| Buscar con operador `in` | Verifica si un texto existe dentro de otro     | `"Py" in "Python"`                              |
| Reemplazar (replace)     | Cambia partes del texto                        | `"Hola mundo".replace("mundo", "Python")`      |
| Mayúsculas (upper)       | Convierte toda la cadena a mayúsculas          | `"hola".upper()`                                |
| Minúsculas (lower)       | Convierte toda la cadena a minúsculas          | `"HOLA".lower()`                                |
| Estilo título (title)    | Primer letra de cada palabra en mayúsculas     | `"hola mundo".title()`                          |
| Capitalizar (capitalize) | Primera letra en mayúscula únicamente          | `"python".capitalize()`                         |
| Quitar espacios (strip)  | Elimina espacios al inicio y al final          | `"  hola  ".strip()`                            |
| Quitar izq. (lstrip)     | Elimina espacios a la izquierda                | `"  hola".lstrip()`                             |
| Quitar der. (rstrip)     | Elimina espacios a la derecha                  | `"hola  ".rstrip()`                             |
| Slicing (subcadenas)     | Extraer partes de una cadena                   | `"Python"[0:3]`                                 |
| Contar ocurrencias       | Cuenta cuántas veces aparece un texto          | `"banana".count("a")`                           |
| Unir cadenas (join)      | Une elementos de una lista con un separador    | `" ".join(["Hola","mundo"])`                   |


### 4.3 Diccionarios y booleanos ###
Un **diccionario** es una estructura de datos que almacena información en pares clave–valor.
Un ***booleano** representa valores lógicos:

**- True**
**- False**

Se utilizan principalmente en:
- Condiciones
- Control de flujo
- Validaciones

### 1. Ejemplo de Diccionario (clave–valor) ###

```python
# Diccionario con información de una persona
persona = {
    "nombre": "Blanca",
    "edad": 30,
    "ciudad": "Aguascalientes"
}

# Acceder a elementos
print(persona["nombre"])
print(persona["ciudad"])

# Agregar un nuevo valor
persona["ocupacion"] = "Desarrolladora"

print(persona)
```
### 2. Ejemplo de Booleanos ###

```python
es_mayor = True
es_menor = False

print(es_mayor)   # True
print(es_menor)   # False
```

### 3. Booleanos en condiciones ###

```python
edad = 20

if edad >= 18:
    print("Eres mayor de edad.")
else:
    print("Eres menor de edad.")
```

### 4. Booleanos en control de flujo ###

```python
activo = True

while activo:
    print("El sistema está activo.")
    activo = False  # Finaliza el ciclo cambiando el booleano
```

### 5. Booleanos en validaciones ###

```python
usuario = "admin"
password = "1234"

es_valido = (usuario == "admin") and (password == "1234")

if es_valido:
    print("Acceso permitido.")
else:
    print("Acceso denegado.")
```

### Tabla Resumen: Diccionarios y Booleanos en Python ###


| Concepto                      | Descripción                                                                 | Sintaxis común                         | Ejemplo breve                           |
|------------------------------|-----------------------------------------------------------------------------|----------------------------------------|-------------------------------------------|
| **Diccionario**              | Estructura clave–valor, mutable y ordenada desde Python 3.7                 | `{clave: valor}`                       | `{"nombre": "Blanca", "edad": 30}`        |
| Acceso a valor               | Obtener un valor usando su clave                                            | `dic["clave"]` / `dic.get("clave")`    | `persona["nombre"]`                       |
| Insertar / actualizar        | Agregar o cambiar un valor del diccionario                                  | `dic["clave"] = valor`                 | `persona["ciudad"] = "AGS"`               |
| Eliminar                     | Remover un par clave–valor                                                  | `del dic["clave"]` / `pop()`           | `del persona["edad"]`                     |
| Recorrer claves/valores      | Iterar sobre un diccionario                                                 | `dic.items()`                          | `for k, v in persona.items()`             |
| **Booleano**                 | Valor lógico que representa verdadero o falso                               | `True`, `False`                        | `activo = True`                           |
| Operadores lógicos           | Combinan condiciones                                                        | `and`, `or`, `not`                     | `(a > 0) and es_admin`                    |
| Comparaciones                | Evalúan expresiones que devuelven booleanos                                 | `==`, `!=`, `>`, `<`, `>=`, `<=`       | `edad >= 18`                              |
| Condiciones (`if/elif`)      | Control de ejecución basado en booleanos                                    | `if cond:`                             | `if es_valido: "OK"`                      |
| Control de flujo (`while`)   | Repite mientras la condición sea verdadera                                  | `while cond:`                          | `while activo:`                           |
| Validaciones compuestas      | Reglas con múltiples condiciones                                            | `and` / `or`                           | `user=="admin" and pwd_correcta`          |
| Existencia en diccionario    | Comprobar si una clave está presente                                        | `"clave" in dic`                       | `"edad" in persona`                       |
| Valores por defecto          | Evitar error cuando falta una clave                                         | `dic.get("clave", defecto)`            | `persona.get("edad", "N/D")`              |
| Limpiar diccionario          | Vaciar todas las entradas                                                   | `dic.clear()`                          | `persona.clear()`                         |


### 4.4 Datos temporales ###
Los datos temporales permiten trabajar con fechas y horas, siendo fundamentales para:

- Registros
- Eventos
- Control de tiempos

### Incluyen: ###

- Fecha (date)
- Hora (time)
- Fecha y hora (datetime)

### 1) Fecha (date) ###

```python
from datetime import date

# Fecha actual
hoy = date.today()
print("Hoy:", hoy)  # Ej: 2026-01-22

# Crear una fecha específica: año, mes, día
cumple = date(1990, 7, 15)
print("Cumpleaños:", cumple)  # 1990-07-15

# Componentes individuales
print("Año:", hoy.year)
print("Mes:", hoy.month)
print("Día:", hoy.day)

# Formatear fecha (a texto)
print("Formateado:", hoy.strftime("%d/%m/%Y"))  # Ej: 22/01/2026

# Parsear texto a fecha
from datetime import datetime
texto = "31-12-2025"
fecha_parseada = datetime.strptime(texto, "%d-%m-%Y").date()
print("Fecha parseada:", fecha_parseada)  # 2025-12-31
```

### 2) Hora (time) ###
```python
from datetime import time

# Crear una hora: hora, minuto, segundo, microsegundo (opcional)
hora_simple = time(14, 30)
hora_completa = time(14, 30, 45, 123456)

print("Hora simple:", hora_simple)       # 14:30:00
print("Hora completa:", hora_completa)   # 14:30:45.123456

# Componentes individuales
print("Hora:", hora_completa.hour)
print("Minuto:", hora_completa.minute)
print("Segundo:", hora_completa.second)
print("Microsegundo:", hora_completa.microsecond)

# Formatear hora
print("Formateada:", hora_completa.strftime("%H:%M:%S"))  # 14:30:45
```

###  3) Fecha y hora (datetime) ###
```python
from datetime import datetime, timedelta, timezone

# Fecha y hora actual (naive, sin zona horaria)
ahora = datetime.now()
print("Ahora (local):", ahora)

# Fecha y hora actual en UTC (con tzinfo)
ahora_utc = datetime.now(timezone.utc)
print("Ahora (UTC):", ahora_utc)

# Crear un datetime específico
evento = datetime(2026, 2, 1, 9, 45, 0)
print("Evento:", evento)  # 2026-02-01 09:45:00

# Formatear datetime
print("Formato legible:", evento.strftime("%d/%m/%Y %I:%M %p"))  # 01/02/2026 09:45 AM

# Parsear texto a datetime
texto_dt = "2026-03-10 18:20:00"
dt_parseado = datetime.strptime(texto_dt, "%Y-%m-%d %H:%M:%S")
print("Datetime parseado:", dt_parseado)

# Aritmética con timedelta (sumas/restas)
inicio = datetime(2026, 1, 1, 8, 0, 0)
duracion = timedelta(hours=2, minutes=30)
fin = inicio + duracion
print("Inicio:", inicio)
print("Duración:", duracion)
print("Fin:", fin)  # 2026-01-01 10:30:00

# Diferencia entre dos datetimes (duración)
delta = fin - inicio
print("Delta en segundos:", delta.total_seconds())  # 9000.0
``
```
### 4) Zonas horarias (básico con timezone) ###
```python
from datetime import datetime, timezone, timedelta

# Crear un datetime consciente de zona horaria (ej. UTC-6)
tz_utc_minus_6 = timezone(timedelta(hours=-6))
ahora_local = datetime.now(tz_utc_minus_6)
print("Ahora UTC-6:", ahora_local)

# Convertir entre zonas (UTC ↔ UTC-6)
ahora_utc = ahora_local.astimezone(timezone.utc)
print("Convertido a UTC:", ahora_utc)
```

### 5) Extra: zoneinfo (zonas reales con horario de verano) ###
```python
from datetime import datetime
from zoneinfo import ZoneInfo  # Python 3.9+

mx = ZoneInfo("America/Mexico_City")
ny = ZoneInfo("America/New_York")

ahora_mx = datetime.now(mx)
print("CDMX:", ahora_mx)

# Convertir a otra zona
ahora_ny = ahora_mx.astimezone(ny)
print("Nueva York:", ahora_ny)
```


