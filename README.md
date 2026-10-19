# ADA · Informes de análisis y diseño de algoritmos

Colección de diez informes en español, desarrollados en **Jupyter Notebook con Python 3**, para estudiar algoritmos mediante explicaciones, implementaciones y análisis teórico y experimental.

Los informes abordan ordenamiento, divide y vencerás, programación dinámica, estrategias voraces, caminos mínimos y complejidad computacional. Según el tema, incluyen ejemplos, demostraciones de correctitud, análisis del tiempo de ejecución, visualizaciones y comparaciones entre algoritmos.

## Índice de informes

| Tema | Contenido | Notebook | Ejecutar en línea |
| --- | --- | --- | --- |
| InsertionSort | Ordenamiento por inserción, invariante de bucle, mejor y peor caso y comparación con BubbleSort. | [Ver informe](Informe_InsertionSort.ipynb) | [Abrir en Colab](https://colab.research.google.com/github/JosephDonoso/ADA-Informes/blob/main/Informe_InsertionSort.ipynb) |
| MergeSort | Divide y vencerás, mezcla de secuencias, recurrencias y comparación con InsertionSort. | [Ver informe](Informe_MergeSort.ipynb) | [Abrir en Colab](https://colab.research.google.com/github/JosephDonoso/ADA-Informes/blob/main/Informe_MergeSort.ipynb) |
| QuickSort | Particionamiento, variantes de selección de pivote y comparación con MergeSort. | [Ver informe](Informe_QuickSort.ipynb) | [Abrir en Colab](https://colab.research.google.com/github/JosephDonoso/ADA-Informes/blob/main/Informe_QuickSort.ipynb) |
| BucketSort | Ordenamiento por buckets, comparación con RadixSort, CountingSort e InsertionSort y variantes con 10 y 100 buckets. | [Ver informe](Informe_BucketSort.ipynb) | [Abrir en Colab](https://colab.research.google.com/github/JosephDonoso/ADA-Informes/blob/main/Informe_BucketSort.ipynb) |
| Subarreglo de suma máxima | Solución recursiva con divide y vencerás y comparación con Kadane y fuerza bruta. | [Ver informe](Informe_MaxSubArray.ipynb) | [Abrir en Colab](https://colab.research.google.com/github/JosephDonoso/ADA-Informes/blob/main/Informe_MaxSubArray.ipynb) |
| Corte de varilla | Optimización de ingresos mediante recursión y programación dinámica con enfoque bottom-up. | [Ver informe](Informe_CorteVarilla.ipynb) | [Abrir en Colab](https://colab.research.google.com/github/JosephDonoso/ADA-Informes/blob/main/Informe_CorteVarilla.ipynb) |
| Problema de la mochila | Comparación de implementaciones bottom-up y voraz en tiempo, operaciones y ganancias obtenidas. | [Ver informe](Informe_Knapsack.ipynb) | [Abrir en Colab](https://colab.research.google.com/github/JosephDonoso/ADA-Informes/blob/main/Informe_Knapsack.ipynb) |
| Árbol binario de búsqueda óptimo | Construcción de árboles según probabilidades de búsqueda, soluciones recursiva y dinámica y visualización del árbol. | [Ver informe](Informe_%C3%81rbol_binario_de_b%C3%BAsqueda_%C3%B3ptimo.ipynb) | [Abrir en Colab](https://colab.research.google.com/github/JosephDonoso/ADA-Informes/blob/main/Informe_%C3%81rbol_binario_de_b%C3%BAsqueda_%C3%B3ptimo.ipynb) |
| Bellman-Ford | Caminos mínimos desde una fuente, visualización de grafos y comparación experimental con Dijkstra. | [Ver informe](Informe_Bellman_Ford.ipynb) | [Abrir en Colab](https://colab.research.google.com/github/JosephDonoso/ADA-Informes/blob/main/Informe_Bellman_Ford.ipynb) |
| Complejidad y NP-Hard | Discusión de clases de complejidad y reducciones relacionadas con suma de subconjuntos y mochila. | [Ver informe](Informe_NP_Hard.ipynb) | [Abrir en Colab](https://colab.research.google.com/github/JosephDonoso/ADA-Informes/blob/main/Informe_NP_Hard.ipynb) |

## Cómo utilizar los informes

### Leer o ejecutar en línea

Abre **Ver informe** para consultar el notebook en GitHub, o **Abrir en Colab** para trabajar con él en línea. Cada notebook también incluye un botón de acceso a Colab en su primera celda.

### Ejecutar localmente

Necesitas Python 3 y un entorno para abrir notebooks. Desde una terminal:

```powershell
git clone https://github.com/JosephDonoso/ADA-Informes.git
cd ADA-Informes
python -m venv .venv
```

Activa el entorno virtual según tu sistema:

```powershell
# Windows (PowerShell)
.\.venv\Scripts\Activate.ps1
```

```bash
# Linux / macOS
source .venv/bin/activate
```

Instala JupyterLab y las bibliotecas externas utilizadas por los notebooks:

```bash
python -m pip install jupyterlab matplotlib numpy pandas plotnine networkx pydot termcolor
python -m jupyterlab
```

Abre el informe que quieras explorar, selecciona el kernel de Python del entorno y ejecuta las celdas en orden, desde el inicio, para cargar las funciones antes de usar los ejemplos y experimentos.

### Dependencias por uso

| Biblioteca o herramienta | Uso en los informes |
| --- | --- |
| Matplotlib | Gráficos de tiempos, comparaciones y operaciones. |
| NumPy | Datos numéricos, probabilidades y apoyo a los experimentos. |
| termcolor | Salida coloreada en ejemplos de ordenamiento y subarreglo máximo. |
| NetworkX | Representación y visualización de grafos y árboles. |
| pydot y Graphviz | Distribución visual del árbol binario de búsqueda óptimo. |
| pandas y plotnine | Comparación gráfica de ganancias en el problema de la mochila. |

Para visualizar el árbol binario de búsqueda óptimo, instala también **Graphviz** en el sistema y asegúrate de que su ejecutable `dot` esté disponible en el `PATH`. El paquete Python `pydot` utiliza esa instalación externa.

## Exploración y experimentos

- Varios algoritmos admiten `verbose=True` para mostrar su ejecución paso a paso. Los informes de árboles y grafos incluyen opciones de visualización cuyos nombres se indican en cada notebook.
- Los experimentos utilizan entradas aleatorias; los resultados y tiempos pueden variar entre ejecuciones y equipos.
- Las variantes recursivas y de fuerza bruta pueden tardar considerablemente al aumentar el tamaño de entrada. Comienza con los ejemplos pequeños de cada informe.
- El informe de NP-Hard se centra en la exposición teórica y las reducciones; no sigue el mismo formato experimental que los demás.

El repositorio conserva los informes como notebooks independientes. No incluye un archivo de dependencias con versiones fijadas; la instalación anterior reúne las bibliotecas identificadas en sus importaciones.
