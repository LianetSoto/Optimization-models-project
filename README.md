# Optimization Models Project

## 📋 Descripción

Este proyecto implementa y compara dos métodos de optimización no lineal (Gradiente Descendente y Quasi-Newton BFGS) para minimizar una función objetivo compleja. El objetivo es analizar el desempeño de estos algoritmos en diferentes escenarios, especialmente considerando que la función tiene un mínimo global único en (0,0) pero no es convexa en todo su dominio.

## Función Objetivo

`f(x,y) = (eˣ + eʸ) arctan(x² + y²)`

## 🚀 Instalación y Configuración

### Prerrequisitos
- **Python 3.8+**
- **Bibliotecas de Python:**
  - `numpy`
  - `scipy`
  - `matplotlib`
  - `jupyter`

## 🧪 Generación y Ejecución de Casos de Prueba
Para probar la implementacion de los algoritmos se cuenta con varias opciones:

### Opción 1: Casos Predefinidos
El proyecto incluye 32 casos de prueba organizados en 2 categorías:

🔹 **Puntos Cercanos al Origen (0,0)**  
🔸 **Puntos Lejanos al Origen (0,0)**

### Opción 2: Crear Nuevos Casos de Prueba
Puedes modificar el archivo `casos_prueba.json` para agregar nuevos casos.

### Opción 3: Crear Tu Propio Archivo JSON
Crea tu propio archivo JSON personalizado con tus propios casos.

## 📊 Parámetros Configurables en JSON

Cada caso de prueba acepta estos parámetros:

```json
{
  "casos_prueba": [
    {
      "name": "Mi-Caso-Personalizado",
      "x0": [x, y_inicial],
      "learning_rate": 0.01,
      "tolerance": 1e-6,
      "max_iterations": 100,
      "category": "personalizado"
    }
  ]
}
Parámetros configurables:
x0: Punto inicial [x, y]
learning_rate: Tasa de aprendizaje para Gradiente Descendente
tolerance: Tolerancia para criterio de parada
max_iterations: Número máximo de iteraciones
category: Categoría para organización
```

```python
# Ejecutar con tu archivo personalizado
resultados = ejecutar_experimentos("mis_casos_personalizados.json")

# O guardar con un nombre específico
resultados = ejecutar_experimentos(
    "mis_casos_personalizados.json", 
    "resultados_personalizados.json"
)