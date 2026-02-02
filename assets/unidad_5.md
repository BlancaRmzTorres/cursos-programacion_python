## Unidad 5. TIPOS DE DATOS Y ALGORITMOS APLICADOS II

### 5.1 Uso avanzado de listas, conjuntos, cadenas y diccionarios

### Fundamentación teórica

En esta unidad se asume que el estudiante ya domina la creación y manipulación básica de **listas**, **conjuntos**, **cadenas** y **diccionarios**. El objetivo ahora es emplear estas estructuras de datos de manera avanzada, combinándolas para resolver problemas algorítmicos más complejos.

Desde el punto de vista algorítmico, estas estructuras permiten:

- Optimizar recorridos y búsquedas  
- Reducir complejidad computacional  
- Representar datos del mundo real de forma estructurada  
- Aplicar filtros, transformaciones y validaciones  

El uso avanzado implica **pensar en términos de datos**, no solo en instrucciones.

### Ejemplo 1: Filtrado avanzado con listas y diccionarios

```python
estudiantes = [
    {"nombre": "Ana", "promedio": 85},
    {"nombre": "Luis", "promedio": 68},
    {"nombre": "María", "promedio": 92}
]

aprobados = [
    e["nombre"]
    for e in estudiantes
    if e["promedio"] >= 70
]

print(aprobados)
```
#### 🧮 **Salida** ####

- ['Ana', 'María']

### Ejemplo 2: Eliminación eficiente de duplicados usando conjuntos
```python
correos = ["a@mail.com", "b@mail.com", "a@mail.com", "c@mail.com"]
correos_unicos = list(set(correos))
print(correos_unicos)
```
#### 🧮 **Salida** ####
- ['c@mail.com', 'a@mail.com', 'b@mail.com']

### 5.2 Operaciones y métodos específicos
Los métodos propios de cada tipo de dato permiten realizar operaciones optimizadas y seguras. Su correcto uso evita estructuras de control innecesarias y mejora la legibilidad del código.

A nivel universitario, el dominio de métodos implica:

- Uso de funciones internas optimizadas
- Encadenamiento de métodos
- Sustitución de ciclos manuales
- Reducción de errores lógicos

### Ejemplo 1: Ordenamiento avanzado con criterio personalizado

```python
productos = [
{"nombre": "Laptop", "precio": 15000},
{"nombre": "Mouse", "precio": 300},
{"nombre": "Monitor", "precio": 4000}
]

productos.sort(key=lambda p: p["precio"], reverse=True)
print(productos)
```
#### 🧮 **Salida** ####
- [{'nombre': 'Laptop', 'precio': 15000}, {'nombre': 'Monitor', 'precio': 4000}, {'nombre': 'Mouse', 'precio': 300}]

### Ejemplo 2: Uso seguro de diccionarios con get()

```python
config = {"tema": "oscuro", "idioma": "es"}

idioma = config.get("idioma", "no definido")
region = config.get("region", "MX")
print(idioma, region)
```

#### 🧮 **Salida** ####
- es MX

### 5.3 Gestión de fechas y horarios

La gestión temporal es esencial en sistemas informáticos reales como plataformas educativas, sistemas de control, auditorías y análisis longitudinales.

El manejo avanzado de fechas implica:

- Comparación de fechas
- Validación de periodos
- Cálculo de duraciones
- Control de eventos y vencimientos

Python proporciona el módulo datetime, que permite tratar el tiempo como una entidad manipulable y comparable.

### Ejemplo 1: Validación de fechas de entrega

```python
from datetime import datetime
fecha_entrega = datetime(2026, 2, 1)
hoy = datetime.now()

if hoy <= fecha_entrega:
    print("Entrega en tiempo")
else:
    print("Entrega fuera de tiempo")
```

#### 🧮 **Salida** ####
- Entrega fuera de tiempo

### Ejemplo 2: Cálculo de duración entre eventos

```python
from datetime import datetime

inicio = datetime(2026, 1, 1, 8, 0)
fin = datetime(2026, 1, 1, 12, 30)

duracion = fin - inicio
print("Horas:", duracion.total_seconds() / 3600)
```
#### 🧮 **Salida** ####
- Horas: 4.5

### 5.4 Evaluación booleana y operaciones de conjunto

La lógica booleana es la base de la toma de decisiones en programación. En esta etapa se emplea de forma compuesta para construir reglas de negocio, validaciones complejas y filtros de datos.

Las operaciones de conjunto permiten evaluar relaciones entre colecciones completas, lo cual es más eficiente que evaluar elemento por elemento.

### Ejemplo 1: Validación lógica compuesta

```python
usuario = "admin"
password = "1234"
activo = True

acceso = (usuario == "admin") and (password == "1234") and activo
print("Acceso permitido" if acceso else "Acceso denegado")
```
#### 🧮 **Salida** ####
- Acceso permitido

### Ejemplo 2: Operaciones de conjunto aplicadas a reglas
```python
usuarios_registrados = {"Ana", "Luis", "María"}
usuarios_con_pago = {"Ana", "María"}

usuarios_validos = usuarios_registrados & usuarios_con_pago
print(usuarios_validos)
```
#### 🧮 **Salida** ####
- {'Ana', 'María'}




