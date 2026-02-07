# 6. APLICACIONES AVANZADAS DE PYTHON

Python no solo se utiliza para scripts básicos o análisis de datos, sino también para **desarrollo profesional**, automatización avanzada, sistemas complejos y productos comerciales. En este tema se abordan herramientas y conceptos que permiten escribir **código robusto, eficiente, portable y vendible**.

---

## 6.1 Problemáticas de codificación

Las problemáticas de codificación surgen cuando el código crece en tamaño, complejidad o debe mantenerse a largo plazo.

### Principales problemáticas

### 1. Código difícil de mantener
- Funciones demasiado largas
- Falta de modularidad
- Uso excesivo de variables globales

**Soluciones:**
- Programación modular  
- Uso de funciones pequeñas y clases  
- Aplicación de principios SOLID

#### Ejercicio

##### ❌ Código con mala práctica
```python
total = 0

def calcular():
    global total
    precios = [100, 200, 300]
    for p in precios:
        total += p
    descuento = total * 0.1
    total = total - descuento
    print("Total final:", total)

calcular()
```
##### ✅ Código mejorado
```python
def calcular_total(precios):
    return sum(precios)

def aplicar_descuento(total, tasa):
    return total * (1 - tasa)

precios = [100, 200, 300]
total = calcular_total(precios)
total_final = aplicar_descuento(total, 0.1)

print("Total final:", total_final)
```

---

### 2. Errores difíciles de detectar
- Errores lógicos
- Excepciones no controladas
- Resultados incorrectos sin fallos visibles

**Soluciones:**
- Manejo de excepciones con `try-except`
- Pruebas unitarias (`unittest`, `pytest`)
- Uso de registros de errores con `logging`

#### Ejercicio
##### ❌ Código sin manejo de errores

```python
def dividir(a, b):
    return a / b

print(dividir(10, 0))
```

##### ✅ Código con manejo de excepciones

```python
def dividir(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        return "Error: división entre cero"
```

##### ➕ Registro de errores

```python
import logging

logging.basicConfig(level=logging.ERROR)

def dividir(a, b):
    try:
        return a / b
    except ZeroDivisionError:
        logging.error("División entre cero")
        return None
```


---

### 3. Bajo rendimiento
- Bucles ineficientes
- Uso incorrecto de estructuras de datos
- Procesamiento innecesario

**Soluciones:**
- Uso de *list comprehensions*
- Librerías optimizadas como NumPy y Pandas
- Análisis de complejidad y *profiling*


#### Ejercicio
##### ❌ Código ineficiente

```python
numeros = []
for i in range(100000):
    numeros.append(i * 2)
```

##### ✅ Código optimizado

```python
numeros = [i * 2 for i in range(100000)]
```

##### ➕ Uso de NumPy

```python
import numpy as np

numeros = np.arange(100000) * 2
```


---

### 4. Problemas de compatibilidad
- Diferencias entre sistemas operativos
- Versiones distintas de Python

**Soluciones:**
- Uso de entornos virtuales (`venv`)
- Control de versiones
- Manejo adecuado de dependencias (`requirements.txt`)

#### Ejercicio
```python
python -m venv venv
pip install pandas
pip freeze > requirements.txt
```

---

## 6.2 Manipulaciones de bajo nivel

Aunque Python es un lenguaje de alto nivel, ofrece herramientas para realizar operaciones cercanas al hardware cuando se requiere mayor control.

### ¿Qué es la manipulación de bajo nivel?
Son operaciones que trabajan directamente con:
- Memoria
- Bits y bytes
- Archivos binarios
- Sistema operativo

---

### Ejemplos de manipulaciones de bajo nivel

### 1. Manejo de bits y bytes
- Operadores bit a bit (`&`, `|`, `^`, `<<`, `>>`)
- Conversión entre representaciones binarias

**Aplicaciones comunes:**
- Criptografía
- Protocolos de comunicación
- Compresión de datos

#### Ejercicio

```python
a = 5   # 0101
b = 3   # 0011

print(a & b)   # AND
print(a | b)   # OR
print(a << 1)  # Desplazamiento
```

---

### 2. Archivos binarios
- Lectura y escritura de archivos binarios
- Uso del módulo `struct` para empaquetar datos

**Aplicaciones:**
- Imágenes
- Audio
- Archivos propietarios

#### Ejercicio

```python
with open("datos.bin", "wb") as f:
    f.write(b'\x01\x02\x03')

with open("datos.bin", "rb") as f:
    print(f.read())
```

---

### 3. Gestión de memoria y rendimiento
- Uso de `memoryview`
- Optimización de estructuras de datos
- Integración con código en C mediante extensiones

#### Ejercicio

```python
datos = bytearray(b"Python")
vista = memoryview(datos)
vista[0] = ord('J')
print(datos)
#### 

---

### 4. Interacción con el sistema operativo
- Gestión de procesos (`subprocess`)
- Variables de entorno
- Manejo de rutas y permisos

Esto permite crear:
- Automatizadores
- Scripts administrativos
- Herramientas de sistema

#### Ejercicio

```python
import os

print(os.getcwd())
print(os.listdir())
```

---

## 6.3 Uso del calendario y husos horarios

El manejo correcto del tiempo es crítico en aplicaciones reales.

### Importancia
- Sistemas financieros
- Registros y auditorías
- Bases de datos
- Aplicaciones distribuidas

Un manejo incorrecto de fechas puede provocar **errores graves**.

---

### Conceptos clave

### 1. Fechas y horas
Python permite trabajar con:
- Fechas
- Horas
- Marcas de tiempo (*timestamps*)
- Intervalos de tiempo

#### Ejercicio

```python
from datetime import datetime

ahora = datetime.now()
print(ahora)
```

---

### 2. Usos horarios (*Time Zones*)
Un huso horario representa la diferencia horaria respecto a UTC.

**Problemas comunes:**
- Cambios de horario de verano
- Usuarios en distintos países
- Conversión incorrecta de fechas

---

### 3. Fechas *naive* y *aware*
- **Naive**: No contiene información de zona horaria
- **Aware**: Incluye zona horaria explícita

> En aplicaciones reales se recomienda trabajar siempre con fechas *aware*.

#### Ejercicio

```python
from datetime import datetime
from zoneinfo import ZoneInfo

fecha = datetime.now(ZoneInfo("America/Mexico_City"))
print(fecha)
```

---

### 4. Aplicaciones prácticas
- Programación de tareas
- Generación de reportes
- Sistemas internacionales
- Auditorías y registros históricos

---

## 6.4 Características avanzadas de Python para el desarrollo rápido y la venta de desarrollos

Python es una herramienta ideal para crear soluciones **rápidas, escalables y comercializables**.

---

### 1. Desarrollo rápido (*Rapid Development*)
Python permite:
- Escribir menos código
- Prototipar rápidamente
- Validar ideas en poco tiempo

**Herramientas clave:**
- Frameworks web como Flask y Django
- Librerías reutilizables
- Automatización mediante scripts

#### Ejercicio

```python
from flask import Flask

app = Flask(__name__)

@app.route("/")
def inicio():
    return "Hola, aplicación en Python"

app.run()
```

---

### 2. Programación orientada a objetos avanzada
- Clases abstractas
- Herencia
- Polimorfismo
- Encapsulamiento

Permite:
- Código reutilizable
- Fácil mantenimiento
- Escalabilidad del proyecto

#### Ejercicio

```python
from abc import ABC, abstractmethod

class Pago(ABC):
    @abstractmethod
    def procesar(self):
        pass
```

---

### 3. Programación funcional
- Funciones lambda
- `map`, `filter`, `reduce`
- Funciones como objetos

Útil para:
- Procesamiento de datos
- Código más expresivo y conciso

#### Ejercicio

```python
numeros = [1, 2, 3, 4]
cuadrados = list(map(lambda x: x**2, numeros))
```

---

### 4. Empaquetado y distribución
Python permite:
- Crear librerías propias
- Generar ejecutables
- Distribuir aplicaciones

Fundamental para:
- Venta de software
- Entrega a clientes
- Uso empresarial

#### Ejercicio

```python
pip install setuptools wheel
```

---

### 5. Integración con otras tecnologías
Python se integra fácilmente con:
- Bases de datos
- APIs
- Sistemas web
- Lenguajes como C, Java y JavaScript

---

## Conclusión

Las aplicaciones avanzadas de Python permiten evolucionar de:
**scripts académicos**  
a  
**soluciones profesionales y comerciales**.

Dominar estos temas permite:
- Escribir código eficiente y mantenible
- Crear sistemas reales
- Desarrollar productos vendibles
- Fortalecer el perfil profesional

---

