## TIPOS DE DATOS Y ALGORITMOS APLICADOS II
### 5.1 Uso avanzado de listas, conjuntos, cadenas y diccionarios

### Marco teórico general

En Python, las estructuras de datos permiten organizar, almacenar y manipular información de manera eficiente. La correcta elección de una estructura impacta directamente en:

- La complejidad algorítmica
- El consumo de memoria
- La claridad del código

Desde un enfoque universitario, el estudio de listas, conjuntos, cadenas y diccionarios se relaciona con:

- **Tipos de datos abstractos (TDA)**
- **Complejidad temporal y espacial**
- **Programación estructurada y orientada a datos**
- **Resolución algorítmica de problemas reales**

Cada estructura responde a necesidades distintas, como acceso secuencial, unicidad, asociación clave–valor o procesamiento de texto.

---

### 5.1.1 Listas (`list`)

### Fundamento teórico

Las listas implementan una **secuencia ordenada e indexada**, equivalente a un arreglo dinámico. Internamente, Python gestiona memoria de forma que permite crecimiento dinámico, lo cual implica:

- **Acceso por índice:** `O(1)`
- **Inserciones/eliminaciones:** `O(n)`

Son ideales cuando:

- El orden importa
- Se requieren recorridos secuenciales
- Se trabaja con colecciones homogéneas o heterogéneas

---

### Características clave de las listas

- **Ordenadas**
- **Mutables**
- **Permiten duplicados**
- **Acceso por índice**

# Características clave de las listas en Python (con ejemplos)

## 1) Listas **ordenadas**
El orden de inserción se mantiene al acceder o recorrer.

### Ejemplo 1
```python
numeros = [10, 20, 30]
print(numeros)  # Output: [10, 20, 30]
```








