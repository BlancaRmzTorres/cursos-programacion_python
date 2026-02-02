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








