# 1.1. Presentación de Python

## ¿Qué es Python?
Python es un lenguaje de programación de alto nivel, versátil y de propósito general, diseñado para ser fácil de leer, escribir y mantener. Fue creado con el objetivo de priorizar la legibilidad del código, lo que lo hace ideal tanto para principiantes como para desarrolladores experimentados. Python se utiliza en una amplia gama de aplicaciones, desde el desarrollo web y la automatización de tareas hasta la inteligencia artificial, el análisis de datos, la programación científica y el desarrollo de juegos.

En el ámbito educativo, Python es ampliamente utilizado en universidades y cursos en línea (como Coursera, edX o freeCodeCamp) porque su sintaxis es similar al inglés, lo que reduce la curva de aprendizaje. 

Por ejemplo, un simple "Hola Mundo" en Python es solo 

```python
    print("Hola Mundo")
```
Comparado con lenguajes como C++, donde requeriría más sintaxis.

```include <iostream> // Para entrada y salida

int main() { // Función principal
    std::cout << "¡Hola, mundo!" << std::endl; // Imprime el mensaje
    return 0; // Indica que el programa terminó correctamente
}
```

## Aplicaciones reales incluyen:
- Desarrollo web: Sitios como Instagram, Pinterest y Spotify usan Python en su backend.
- Ciencia de datos: Herramientas como Jupyter Notebook permiten análisis interactivos.
- Automatización: Scripts para tareas repetitivas, como procesar archivos o enviar emails.
- Inteligencia artificial: Modelos de IA en empresas como Google (con TensorFlow) o OpenAI.
- Juegos y multimedia: Bibliotecas como Pygame para desarrollo de juegos simples.

## Ventajas 
- Incluyen su comunidad activa (foros como Stack Overflow tienen millones de preguntas resueltas)
- Su portabilidad (corre en Windows, macOS, Linux, etc.)
- Su integración con otros lenguajes (puedes llamar código C o Java desde Python).

## Desventajas 
- Podrían ser su velocidad de ejecución (más lento que C++ en bucles intensivos), aunque esto se mitiga con optimizaciones como Cython o el uso de bibliotecas compiladas.

En resumen, Python no es solo un lenguaje, sino un ecosistema completo que fomenta la productividad y la innovación en programación.

## Historia breve del lenguaje
La historia de Python comienza a finales de los años 80, cuando Guido van Rossum, un programador holandés trabajando en el Centrum Wiskunde & Informatica (CWI) en los Países Bajos, buscaba crear un lenguaje que superara las limitaciones de ABC, un lenguaje educativo en el que había trabajado. ABC era simple pero carecía de características para programación a gran escala. Inspirado en ABC, pero también en lenguajes como Modula-3, C, Perl y Lisp, Van Rossum inició el desarrollo de Python durante las vacaciones de Navidad de 1989. El nombre "Python" proviene de la serie de comedia británica "Monty Python's Flying Circus", reflejando el sentido del humor que Van Rossum quería infundir en el lenguaje.

La primera versión pública, Python 0.9.0, fue lanzada en febrero de 1991 a través de Usenet (un precursor de los foros modernos). Incluía características básicas como clases con herencia, manejo de excepciones, funciones y módulos. En 1994, se formó la comunidad comp.lang.python en Usenet, lo que ayudó a su difusión. Van Rossum se mudó a Estados Unidos en 1995 y trabajó en la Corporation for National Research Initiatives (CNRI), donde continuó desarrollando Python.

En la actualidad (2026), Python sigue evolucionando. La versión más reciente es Python 3.12 (lanzada en 2023), con mejoras en rendimiento (hasta 2x más rápido en algunos casos gracias al proyecto Faster CPython) y características como type hints mejorados. Python ha influido en otros lenguajes, como Swift (de Apple) y Julia. Su adopción en educación (por ejemplo, en el currículo de muchas escuelas secundarias) y en industrias como fintech (usado en bancos como JPMorgan) y espacio (NASA usa Python para misiones como Perseverance) lo han consolidado como un pilar de la programación moderna.

## Características principales

Python se distingue por una serie de características que lo hacen único y atractivo. A continuación, se explican:

## Lenguaje interpretado
Python es un lenguaje interpretado, lo que significa que el código fuente se traduce y ejecuta línea por línea por un intérprete (como CPython, el implementado en C), en lugar de compilarse a un ejecutable independiente. Esto contrasta con lenguajes compilados como C++, donde el código se convierte en binario antes de ejecutarse.

El proceso involucra: 
  - (1) El código fuente (.py) se compila a bytecode (.pyc) por el intérprete;   
  - (2) Este bytecode se ejecuta en la Máquina Virtual de Python (PVM). Ventajas incluyen desarrollo rápido (puedes probar código inmediatamente sin compilación larga), portabilidad (el bytecode es independiente de la plataforma) y facilidad de depuración (errores se detectan en runtime).
  
## Multiplataforma
Python es multiplataforma, lo que significa que el mismo código puede ejecutarse en diferentes sistemas operativos (Windows, macOS, Linux, Unix, incluso Android o iOS con herramientas como Kivy) sin modificaciones significativas. Esto se logra porque el intérprete maneja las diferencias subyacentes del SO, y las bibliotecas estándar abstraen operaciones como manejo de archivos o redes.

## Tipado dinámico
Python utiliza tipado dinámico, donde los tipos de variables se determinan en tiempo de ejecución, no en compilación. No necesitas declarar tipos explícitamente; por ejemplo, x = 5; x = "texto" es válido, cambiando de int a str dinámicamente.
Esto se basa en "duck typing": si algo se comporta como un pato, se trata como un pato (enfocado en interfaces, no en tipos estrictos). Ventajas: Código más conciso y flexible, ideal para prototipado rápido. Puedes escribir funciones genéricas que trabajen con múltiples tipos.

### Ejemplo: 

```python
def suma(a, b):
return a + b #funciona con números, strings o listas.
```
## Sintaxis legible
La sintaxis de Python es diseñada para ser legible y similar al pseudocódigo o al inglés, usando indentación (espacios o tabs) para definir bloques de código en lugar de llaves {} o palabras como "end". Esto fuerza un estilo limpio y reduce errores.

## Ejemplo: 
Un if-else es 

```python
if condicion: 
    print("Verdadero") 
else: 
    print("Falso") 
```

## Ventajas: 
Facilita la colaboración (código se lee como prosa), reduce bugs visuales y acelera el aprendizaje. El PEP 8 (Python Enhancement Proposal) define guías de estilo para consistencia.

## Desventajas: 
La indentación estricta puede frustrar a programadores de otros lenguajes, y errores de indentación son comunes en principiantes. Aplicaciones: En educación (usado en MIT, Stanford); en código abierto (proyectos como Linux Kernel usan Python para tools); y en IA, donde la legibilidad ayuda en revisiones de modelos complejos.

Otras características relacionadas: Soporte para comprehensions, decorators (@), generators (yield) y async/await para programación asíncrona, todo con sintaxis limpia.

# 1.2. Dentro de Python (gramática, sintaxis, librerías)

## Gramática básica
La gramática de Python define las reglas fundamentales para escribir código válido. Dos elementos clave son los identificadores y las palabras reservadas.
Identificadores

Los identificadores son los nombres que asignamos a variables, funciones, clases, módulos, etc. Python tiene reglas estrictas para su formación:

Reglas:
- Pueden contener letras (a-z, A-Z), dígitos (0-9) y guiones bajos (_).
- Deben comenzar con una letra o guion bajo (nunca con un dígito).
- Son sensibles a mayúsculas y minúsculas (miVariable ≠ mivariable).
- No pueden ser palabras reservadas (ver siguiente sección).

Convención PEP 8:
Es la guía oficial de estilo para escribir código Python, creada para mejorar la legibilidad y consistencia, estandarizando formato, nomenclatura y estructura, e incluye reglas sobre indentación (4 espacios), longitud de línea (máx. 79 caracteres), uso de espacios en blanco, nombres (minúsculas con guiones bajos) y organización de imports, ayudando a que el código sea más fácil de leer y mantener por otros desarrolladores. 

Recomendaciones:
- Variables y funciones: snake_case (todo minúsculas, palabras separadas por _).
- Clases: CamelCase (primera letra mayúscula en cada palabra).
- Constantes: MAYUSCULAS_CON_GUIONES.

### Ejemplos válidos:

```python
nombre = "Ana"
edad = 25
_nombre_interno = 10
mi_variable_1 = "texto"
PrecioProducto = 99.99  # aunque es válido, no sigue PEP 8 (mejor snake_case)
```

Ejemplos inválidos:

```python
1variable = 5        # comienza con número → SyntaxError
mi-variable = 10     # guion medio no permitido → SyntaxError
class = "clase"      # palabra reservada → SyntaxError
```

### Buenas prácticas:
- Usa nombres descriptivos: calcular_impuesto en vez de ci.
- Evita nombres demasiado largos, pero prioriza claridad.
- Documetar el uso de las funciones, clases, entre otras.
  
## Palabras reservadas
Son palabras que Python reserva para su propio uso (sentencias, operadores, etc.). No pueden usarse como identificadores.

Puedes ver la lista completa ejecutando:

```python
import keyword
print(keyword.kwlist)
```

['False', 'None', 'True', 'and', 'as', 'assert', 'async', 'await  'break', 'class', 'continue', 'def', 'del', 'elif', 'else',  'except', 'finally', 'for', 'from', 'global', 'if', 'import',  'in', 'is', 'lambda', 'nonlocal', 'not', 'or', 'pass', 'raise',  'return', 'try', 'while', 'with', 'yield']

Ejemplos de uso correcto:

```python
if edad >= 18:
    print("Mayor de edad")
else:
    print("Menor de edad")

for i in range(5):
    print(i)

def saludar(nombre):
    return f"Hola, {nombre}"
```

Ejemplo de error:

```python
def = 5        # SyntaxError: invalid syntax
class = "A"    # SyntaxError
```

## Sintaxis
La sintaxis de Python es uno de sus mayores diferenciadores: limpia, legible y basada en indentación.

Uso de indentación

Python usa la indentación (espacios o tabuladores) para delimitar bloques de código, en lugar de llaves {} como en otros lenguajes.
Regla estricta:
- Generalmente se usan 4 espacios por nivel (recomendado por PEP 8).
- Todo el bloque debe tener la misma indentación.
- Mezclar tabuladores y espacios causa TabError.

Ejemplo correcto:

```python
def calcular_area_rectangulo(base, altura):
    if base > 0 and altura > 0:
        area = base * altura
        print(f"El área es: {area}")
        return area
    else:
        print("Base y altura deben ser positivas")
        return 0
```

Ejemplo incorrecto:

```python
def ejemplo_malo():
if True:  # sin indentación → IndentationError
print("Esto falla")
```

Ventajas:
- Obliga a escribir código limpio y consistente.
- Mejora la legibilidad para equipos.

Consejo: Configura tu editor (VS Code, PyCharm, etc.) para convertir tabuladores en 4 espacios automáticamente.

Comentarios
Los comentarios sirven para documentar el código y no se ejecutan.
- Comentarios de una línea: con #

# Esto es un comentario de una sola línea

```python
edad = 30  # puedo ponerlo al final de una línea de código
•	Comentarios multilínea: con triple comilla """ (docstrings) o múltiples #

"""
Esto es un comentario multilínea.
Se usa frecuentemente como docstring para documentar funciones,
clases o módulos.
"""

# Línea 1 del comentario
# Línea 2 del comentario
# Línea 3 del comentario
•	Docstrings (recomendados):
Python
def suma(a, b):
    """
    Retorna la suma de dos números.
    
    Parámetros:
        a (int o float): primer número
        b (int o float): segundo número
    
    Retorna:
        int o float: suma de a y b
    """
    return a + b
```

## Bloques de código
Un bloque de código es un grupo de sentencias que se ejecutan juntas (dentro de una función, bucle, condicional, etc.).

## Estructura típica:

```python
# Ejemplo completo con varios bloques
def procesar_lista(numeros):
    """
    Imprime números pares de una lista.
    """
    for numero in numeros:          # inicio del bloque for
        if numero % 2 == 0:         # inicio del bloque if
            print(f"{numero} es par")
        else:                       # bloque else (mismo nivel que if)
            print(f"{numero} es impar")
    # fin del bloque for (vuelve al nivel de la función)
    
    print("Procesamiento terminado")
# Bloques anidados:

for i in range(3):
    for j in range(2):
        print(f"i={i}, j={j}")
    print("Fin de j para este i")
```

- La indentación define claramente la jerarquía de los bloques.

## Librerías
Una de las mayores fortalezas de Python es su ecosistema de librerías.

## Librerías estándar
Python incluye una biblioteca estándar muy completa que viene instalada por defecto. No necesitas instalar nada extra.
Algunos módulos más útiles:
Módulo	Descripción	

Ejemplo de uso

| Módulo        | Descripción                              | Ejemplo de uso |
|--------------|------------------------------------------|---------------|
| `math`       | Funciones matemáticas                    | `import math; math.sqrt(16)` → `4.0` |
| `random`     | Generación de números aleatorios         | `import random; random.randint(1, 10)` |
| `datetime`   | Manejo de fechas y horas                 | `from datetime import datetime; datetime.now()` |
| `os`         | Interacción con el sistema operativo     | `import os; os.getcwd()` → directorio actual |
| `sys`        | Acceso a parámetros del intérprete       | `import sys; sys.version` |
| `json`       | Trabajo con datos en formato JSON        | `import json; json.loads('{"nombre": "Ana"}')` |
| `collections`| Estructuras de datos avanzadas           | `from collections import Counter; Counter([1,1,2])` |
| `itertools`  | Herramientas para trabajar con iteradores| `import itertools; list(itertools.combinations([1,2,3], 2))` |


```python
##Ejemplo práctico combinando varios:

import os
import datetime
import random

print("Directorio actual:", os.getcwd())
print("Fecha y hora:", datetime.datetime.now())

numero_aleatorio = random.randint(1, 100)
print(f"Número aleatorio del día: {numero_aleatorio}")
```

Librerías externas (pip)
Las librerías externas se instalan con el gestor de paquetes pip y provienen del Python Package Index (PyPI).

## Instalación básica:

pip install nombre_paquete
pip install requests pandas numpy matplotlib

### Ejemplos de librerías externas muy populares

| Librería | Uso principal | Instalación | Ejemplo de importación / uso |
|--------|---------------|-------------|-------------------------------|
| `requests` | Peticiones HTTP sencillas | `pip install requests` | `import requests; r = requests.get('https://api.github.com')` |
| `pandas` | Análisis y manipulación de datos | `pip install pandas` | `import pandas as pd; df = pd.read_csv('datos.csv')` |
| `numpy` | Cálculo numérico de alto rendimiento | `pip install numpy` | `import numpy as np; arr = np.array([1, 2, 3])` |
| `matplotlib` | Visualización de datos (gráficos) | `pip install matplotlib` | `import matplotlib.pyplot as plt; plt.plot([1, 2, 3])` |
| `flask` | Desarrollo web ligero | `pip install flask` | `from flask import Flask` |
| `django` | Desarrollo web completo | `pip install django` | `import django` |
| `beautifulsoup4` | Web scraping (análisis de HTML/XML) | `pip install beautifulsoup4` | `from bs4 import BeautifulSoup` |



Ejemplo real con requests y json:

```python
import requests

respuesta = requests.get("https://api.chucknorris.io/jokes/random")
if respuesta.status_code == 200:
    broma = respuesta.json()["value"]
    print("Broma de Chuck Norris:", broma)
```

## 1.3 Proceso de ejecución en Python
El proceso de ejecución de un programa en Python es diferente al de lenguajes compilados como C o Java. Python es un lenguaje interpretado (aunque con un paso intermedio de compilación a bytecode), lo que significa que el código no se traduce completamente a lenguaje máquina antes de ejecutarse, sino que se interpreta en tiempo de ejecución.

A continuación se detalla el proceso completo de manera más precisa y ampliada, con ejemplos:

Pasos detallados del proceso de ejecución

## 1. Escritura del código fuente
El programador escribe el código en un archivo con extensión .py (por ejemplo, mi_programa.py). Este archivo contiene texto plano con instrucciones en Python.Ejemplo:

```python
# mi_programa.py
nombre = "Ana"
edad = 25
print(f"Hola, me llamo {nombre} y tengo {edad} años.")
```
## 2. Lectura y análisis léxico/sintáctico (parsing)
Cuando se ejecuta el programa con python mi_programa.py, el intérprete de Python:
- Lee el código fuente completo.
- Lo divide en tokens (análisis léxico).
- Construye un árbol de sintaxis abstracta (AST) verificando que la sintaxis sea correcta.

Si hay errores de sintaxis (SyntaxError), el programa falla en esta etapa.

Ejemplo de error en esta fase:

```python
print("Hola"  # Falta cerrar el paréntesis
```
Resultado: SyntaxError: unexpected EOF while parsing

## 3. Compilación a bytecode
Python compila el AST a un código intermedio llamado bytecode (código de bytes). Este bytecode es independiente de la plataforma y se almacena internamente en objetos code.

Si el archivo .pyc correspondiente (en la carpeta __pycache__) está actualizado, Python reutiliza el bytecode ya compilado para ahorrar tiempo.

El bytecode es lo que realmente ejecuta la máquina virtual de Python (Python Virtual Machine o PVM).

Puedes ver el bytecode generado con el módulo dis:

```python
import dis

def saludar():
    print("Hola mundo")

dis.dis(saludar)
```

## 4. Ejecución en la Máquina Virtual de Python (PVM)

La PVM interpreta y ejecuta el bytecode instrucción por instrucción (opcode por opcode).
- Carga constantes y variables.
- Realiza operaciones.
- Gestiona la pila de ejecución, el scope, llamadas a funciones, etc.

Durante esta fase pueden aparecer errores en tiempo de ejecución (RuntimeError, NameError, TypeError, etc.).Ejemplo de error en tiempo de ejecución:

```python
numero = "10"
resultado = numero + 5  # TypeError
```

## 5. Finalización
Una vez ejecutadas todas las instrucciones, el programa termina y devuelve el control al sistema operativo.

```md
Código fuente (.py)
       ↓
Análisis léxico y sintáctico → Árbol AST
       ↓ (si hay errores → SyntaxError)
Compilación → Bytecode (.pyc cacheado)
       ↓
Ejecución en PVM instrucción por instrucción
       ↓ (posibles excepciones en runtime)
Salida / Resultado del programa
```

### Diferencias clave con lenguajes compilados

| Aspecto                  | Python (interpretado con bytecode)                  | Lenguajes compilados (C, Go)                  |
|--------------------------|-----------------------------------------------------|-----------------------------------------------|
| Compilación              | A bytecode (intermedio)                             | Directo a código máquina                      |
| Velocidad de inicio      | Más rápido (no hay enlace)                          | Más lento (compilación completa)              |
| Portabilidad             | Alta (bytecode corre en cualquier PVM)              | Baja (binario específico de plataforma)       |
| Detección de errores     | Muchos en tiempo de ejecución                       | La mayoría en tiempo de compilación           |

Este proceso híbrido (interpretado con compilación intermedia) permite a Python combinar flexibilidad, portabilidad y una buena velocidad de desarrollo.

# 1.4 Importancia y alcance del lenguaje

Python es uno de los lenguajes de programación más populares y utilizados a nivel mundial. Según índices como el **TIOBE Index** y **PYPL (PopularitY of Programming Language)**, Python ha ocupado consistentemente los primeros lugares durante los últimos años, superando incluso a lenguajes tradicionales como Java y C++ en popularidad.

Esta posición se debe a su **versatilidad**, **simplicidad** y a un ecosistema extremadamente rico que permite aplicarlo en una amplia variedad de dominios.

### Áreas de aplicación principales

- **Ciencia de datos y estadística**  
  Python domina este campo gracias a bibliotecas como *pandas*, *NumPy*, *SciPy*, *Matplotlib* y *Seaborn*. Herramientas como *Jupyter Notebook* facilitan el análisis exploratorio y la visualización interactiva.

- **Inteligencia artificial y aprendizaje automático**  
  Es el lenguaje líder en IA. Bibliotecas como *TensorFlow*, *PyTorch*, *scikit-learn*, *Keras* y *Hugging Face Transformers* permiten desarrollar desde modelos básicos hasta redes neuronales profundas y modelos de lenguaje grandes (LLM).

- **Desarrollo web**  
  Frameworks potentes como *Django* (baterías incluidas, ideal para aplicaciones robustas) y *Flask*/*FastAPI* (ligeros y flexibles) hacen de Python una opción excelente tanto para backend como para APIs RESTful y servicios web modernos.

- **Automatización de procesos y scripting**  
  Python es ideal para tareas de automatización: administración de sistemas, procesamiento de archivos, web scraping (*BeautifulSoup*, *Scrapy*), testing automático, DevOps (*Ansible* está escrito en Python) y bots.

- **Análisis de información institucional y académica**  
  Universidades, centros de investigación y organismos gubernamentales lo utilizan ampliamente para procesar grandes volúmenes de datos, generar informes automatizados y realizar simulaciones científicas.

- **Otras áreas relevantes**  
  - Desarrollo de videojuegos (*Pygame*, *Godot* con soporte Python).  
  - Ciberseguridad y pentesting (*scripts* personalizados y herramientas como *Scapy*).  
  - Finanzas cuantitativas (*pandas*, *QuantLib*).  
  - Bioinformática (*Biopython*).  
  - Internet de las cosas (IoT) con *MicroPython* en dispositivos embebidos.

### Ventajas clave de Python

- **Curva de aprendizaje baja**  
  Sintaxis clara, legible y cercana al lenguaje natural. Esto permite que principiantes aprendan rápidamente y que profesionales escriban código mantenible.

- **Gran cantidad de recursos y bibliotecas**  
  El repositorio oficial **PyPI** contiene más de 500.000 paquetes. Prácticamente cualquier funcionalidad que necesites ya está implementada y disponible con un simple `pip install`.

- **Comunidad activa y extensa**  
  Millones de desarrolladores contribuyen con tutoriales, foros (*Stack Overflow*), documentación y eventos. Esto facilita resolver problemas y mantenerse actualizado.

- **Uso extendido en la industria, investigación y gobierno**  
  Empresas como Google, Netflix, Instagram, Spotify, NASA, CERN y Banco Mundial utilizan Python intensivamente. Su adopción en entornos críticos demuestra madurez y confiabilidad.

- **Multiplataforma y portable**  
  El mismo código funciona en Windows, macOS y Linux sin modificaciones.

- **Integración sencilla con otros lenguajes**  
  Puede llamar código en C/C++ (*Cython*, *ctypes*) para optimizar rendimiento cuando es necesario.

### Conclusión

La combinación de simplicidad, potencia y un ecosistema maduro hace que Python no solo sea un lenguaje excelente para aprender a programar, sino también una herramienta estratégica en entornos profesionales y científicos. Su alcance sigue creciendo, especialmente con el auge de la inteligencia artificial y la ciencia de datos, consolidándolo como uno de los lenguajes más importantes del presente y del futuro cercano.


# 1.5 Implementación del entorno de desarrollo (instalación, configuración, IDEs)

Para comenzar a programar en Python, es esencial configurar un entorno de desarrollo adecuado. Esto incluye la instalación de Python, la gestión de paquetes y entornos virtuales, y la elección de un editor o IDE (Integrated Development Environment).

A enero de 2026, la versión estable más reciente de Python es **Python 3.14** (la serie 3.15 está en fase pre-release alpha). Siempre se recomienda instalar la última versión estable desde el sitio oficial.

### Instalación de Python

La forma recomendada es descargar el instalador oficial desde [https://www.python.org/downloads/](https://www.python.org/downloads/). El sitio detecta automáticamente tu sistema operativo y ofrece la versión adecuada.

#### En Windows
1. Descarga el instalador ejecutable (.exe) para Windows.
2. Ejecútalo como administrador.
3. **Importante**: Marca la casilla **"Add python.exe to PATH"** (agregar Python al PATH del sistema).
4. Selecciona "Install Now" para una instalación estándar.
5. Al finalizar, verifica abriendo la Command Prompt (cmd) y ejecutando:


#### En macOS
1. Descarga el instalador (.pkg) para macOS.
2. Ejecútalo y sigue las instrucciones del asistente.
3. Python se instalará en `/Applications/Python 3.x`.
4. Verifica en Terminal:

Nota: En macOS recientes, se usa `python3` para evitar conflictos con la versión antigua de Python 2 que venía preinstalada.

Alternativa recomendada: Usa **Homebrew** (gestor de paquetes):


#### En Linux (Ubuntu/Debian, Fedora, etc.)
La mayoría de distribuciones incluyen Python preinstalado, pero para la versión más reciente:
- **Ubuntu/Debian**:


2. **Entornos virtuales**
Los entornos virtuales de Python son directorios aislados que permiten gestionar dependencias y librerías específicas para cada proyecto, evitando conflictos entre versiones y asegurando la portabilidad

Para crear un entorno virtual se realiza lo siguiente:

Actívalo:

- Windows: `mi_entorno\Scripts\activate`
- macOS/Linux: `source mi_entorno/bin/activate`

Desactívalo: `deactivate`

3. **Variables de entorno**: En Windows, asegúrate de que Python esté en PATH (lo hace el instalador si marcaste la opción).

### IDEs y editores recomendados (2026)

| IDE/Editor                  | Descripción                                                                 | Ideal para                          | Gratuito/Pago          |
|-----------------------------|-----------------------------------------------------------------------------|-------------------------------------|------------------------|
| **Visual Studio Code (VS Code)** | Editor ligero y extensible. Con extensión oficial de Python (Microsoft), ofrece autocompletado, debugging, linting y soporte para Jupyter. El más popular en 2026. | Todo tipo de proyectos, principiantes y expertos | Gratuito (open source) |
| **PyCharm**                | IDE completo de JetBrains. Edición Community (gratuita) y Professional (paga con más features como web y ciencia de datos). Excelente refactoring y debugging. | Proyectos grandes, desarrollo profesional | Community: Gratuito<br>Professional: Pago |
| **Cursor**                 | Editor basado en VS Code pero con integración profunda de IA (code completion avanzada). Muy popular en 2026 para desarrollo asistido por IA. | Desarrolladores que usan IA para codificar más rápido | Gratuito con opciones premium |
| **JupyterLab / Notebook**  | Entorno interactivo basado en navegador, ideal para notebooks (.ipynb). Perfecto para experimentación. | Ciencia de datos, ML, análisis exploratorio | Gratuito |
| **Spyder**                 | IDE científico incluido en Anaconda. Interfaz similar a MATLAB/RStudio, con explorador de variables y gráficos integrados. | Ciencia de datos y computación científica | Gratuito |
| **Thonny**                 | IDE simple y amigable, con debugger paso a paso visual. Viene con Python incluido. | Principiantes y educación | Gratuito |
| **IDLE**                   | IDE básico incluido con Python. Suficiente para scripts simples. | Primeros pasos, pruebas rápidas | Gratuito (incluido) |

**Recomendación general**:
- Principiantes: Thonny o VS Code.
- Desarrollo general: VS Code o PyCharm Community.
- Ciencia de datos/IA: JupyterLab, Spyder o PyCharm Professional.
- Con IA avanzada: Cursor.

### Otras herramientas útiles
- **Anaconda/Miniconda**: Distribución para ciencia de datos (incluye conda, Jupyter, Spyder y cientos de paquetes preinstalados).
- **poetry** o **uv**: Gestores modernos de dependencias y entornos (alternativas a pip + venv).



Con estos pasos, tendrás un entorno de desarrollo Python listo y profesional. ¡Ahora puedes empezar a escribir tu primer "Hello World"!

