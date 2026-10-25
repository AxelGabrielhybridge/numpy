# 🧪 NumPy & Procesamiento de Imágenes en Python

Un espacio dedicado al aprendizaje práctico de **NumPy**, manipulación de arreglos multidimensionales y análisis básico de imágenes utilizando Python y Jupyter Notebooks.

Este repositorio contiene libretas interactivas diseñadas para explorar los conceptos fundamentales de la computación científica y el procesamiento de imágenes digitales.

---

## 📁 Estructura del Proyecto

```text
numpy/
├── 1_numpy_avanzado.ipynb   # NumPy avanzado: arreglos, dimensiones y matrices aleatorias
├── 2_ejercicios.ipynb       # Análisis de imágenes (beagle.jpg) con Matplotlib
├── beagle.jpg               # Imagen de muestra para el análisis visual
└── .venv/                   # Entorno virtual con las dependencias instaladas
```

---

## 📓 Descripción de los Notebooks

### 1. 🧮 `1_numpy_avanzado.ipynb` - NumPy Avanzado
Notebook consolidado que combina la introducción a arreglos de NumPy con la generación y visualización de matrices aleatorias usando Python puro.

* **Parte 1 — Arreglos NumPy:**
  * Creación de arreglos multidimensionales con `np.array()` y `dtype='float'`.
  * Inspección de atributos esenciales:
    * `.ndim`: número de dimensiones.
    * `.shape`: dimensiones en formato de tupla `(filas, columnas)`.
    * `.size`: total de elementos.

* **Parte 2 — Matrices Aleatorias:**
  * Generación dinámica de matrices cuadradas $N \times N$ con `random.randint`.
  * Formateo simétrico en consola usando f-strings y `.join()`.
  * Ejemplos con matrices de $5 \times 5$, $10 \times 10$ y $20 \times 20$.

### 2. 🖼️ `2_ejercicios.ipynb` - Análisis de una Imagen
Procesamiento digital de imágenes: cómo una fotografía se representa como una matriz tridimensional en memoria.

* **Conceptos clave:**
  * Lectura de `beagle.jpg` con `plt.imread()` de Matplotlib.
  * Análisis de la estructura `(Alto, Ancho, Canales RGB)` mediante `.shape`.
  * Inspección de valores de píxeles individuales en coordenadas específicas (valores en rango $[0, 255]$).

---

## 🛠️ Requisitos e Instalación

### Dependencias Principales
* **NumPy**, **Matplotlib** y **Pandas**: arreglos, gráficos y tabla de píxeles.
* **JupyterLab** e **ipykernel**: apertura y ejecución de los notebooks.
* **nbformat** y **nbclient**: validación y ejecución completa desde un kernel limpio.

Las versiones directas verificadas con Python 3.12 están en `requirements.txt`.

### Configuración del Entorno

Desde la carpeta del repositorio, crea el entorno y actívalo:

```powershell
# Windows / PowerShell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -c "import sys; print(sys.executable)"
python -m pip install -r requirements.txt
python -m jupyterlab
```

```bash
# macOS / Linux
python3 -m venv .venv
source .venv/bin/activate
python -c "import sys; print(sys.executable)"
python -m pip install -r requirements.txt
python -m jupyterlab
```

Si PowerShell restringe la activación, usa directamente
`.\.venv\Scripts\python.exe` para esos comandos de Python. No hace falta cambiar
la política global. Selecciona el kernel de `.venv` en JupyterLab y ejecuta los
notebooks desde la carpeta que contiene `beagle.jpg`.

### Checkpoint 3: trabajo y comprobaciones

Se reejecutaron desde cero las 6 celdas de código de `1_numpy_avanzado.ipynb` y
las 11 de `2_ejercicios.ipynb`, sin errores. Las soluciones de C2 se conservaron;
se hizo visible el tipo `ndarray` y se añadieron comprobaciones de RGB, medias por
canal y correspondencia entre píxeles y DataFrame. Se guardaron las seis figuras
y la tabla HTML de sus primeras cinco filas.

La imagen incluida mide **1024 × 1024**, tiene tres canales `uint8` y su píxel
`[0, 0]` es `[29, 46, 10]`. Los valores de la imagen didáctica del temario
dependen de ese otro archivo. La media global de esta imagen es
`119.40487066904704`; el canal verde tiene la mayor media
(`145.15760898590088`). El DataFrame conserva sus **1,048,576 píxeles** en tres
columnas. No se requiere descargar un CSV para los ejercicios de estos notebooks.

---

## 🚀 ¿Cómo empezar?

1. Abre **`1_numpy_avanzado.ipynb`** para aprender las propiedades de los arreglos NumPy y practicar la generación de matrices aleatorias.
2. Continúa con **`2_ejercicios.ipynb`** para cargar `beagle.jpg` y explorar cómo se representa una imagen como una matriz 3D con canales RGB.

---
> [!NOTE]
> Este proyecto forma parte de una ruta de aprendizaje orientada a **Ciencia de Datos**, **Computación Científica** y **Procesamiento de Imágenes**. ¡Perfecto para entusiastas del análisis de datos que inician su viaje en Python!
