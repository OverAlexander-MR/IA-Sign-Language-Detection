# IA-Sign-Language-Detection
# Proyecto de Redes Neuronales con PyTorch
### Autores: Over Alexander Mejia Rosado y Ronald Mateo Ceballos Lozano
### Asignatura: Redes Neuronales y Aprendizaje Profundo
Como proyecto de la asignatura Redes Neuronales y Aprendizaje Profundo, se decidio realizar la construcción de una Red Convolucional Neuronal (CNN) que detecte el abecedario en lenguaje de señas americano. Para ello se tomo un dataset de Kaggle con las siguientes caracteristicas:

### Clasificador del Abecedario de Lenguaje de Señas Americano:

- **Cantidad de Datos**: El número de datos es de 87000 con un tamaño de 200x200 pixeles.
- **Cantidad de Clases**: Existen 29 clases de las cuales 26 son para las del abecedario (A-Z) y 3 clases para "Space", "Delete y "Nothing".

Se decidio filtrar las clases del dataset para reducir el tiempo de entrenamiento del modelo y solo analizar las vocales del abecedario y "Nothing" que relaciona a un espacio vacio. Gracias a esto nuestro dataset quedo de la siguiente manera:

- **Cantidad de Datos**: El número de datos es de 18000 con un tamaño de 200x200 pixeles.
- **Cantidad de Clases**: Existen 6 clases de las cuales 5 son para las vocales (A, E, I, O, U) y la ultima clase para "Nothing", cada clase tiene 3000 imagenes.

En el directorio donde se descargaron los archivos se eliminaron de forma manual las clases que no se implementaron.

# Versiones de Python, Numpy, Matplotlib usadas
`Python 3.10.12`
`Pytorch 2.5.1`
`Matplotlib 3.8.0`
`Torchvision 0.20.1`
`Skicit-learn 1.5.2`

## Carga y Preparación de los datos
Para crear el modelo y entrenarlo, se utilizarán los datos del dataset con las vocales en lenguaje de señas americano filtrados, es decir los 18000 datos correspondientes a las vocales y al espacio vacio. Se realiza una redimensión de `200x200` a `32x32` y disminuir la complejidad del modelo.
