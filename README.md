# Proyecto de Visión Artificial con YOLO

## Integrantes

* Marco Lopez
* Jesus Baez

## Descripción del Proyecto

Este proyecto tiene como objetivo aplicar técnicas de Visión Artificial mediante el entrenamiento de un modelo de la familia YOLO (You Only Look Once) para la detección y reconocimiento de objetos en imágenes.

El modelo será entrenado utilizando un conjunto de datos específico y posteriormente evaluado mediante imágenes y videos de prueba para verificar su desempeño.

## Objetivos

* Comprender el funcionamiento de los modelos de detección de objetos YOLO.
* Preparar y procesar un conjunto de datos para entrenamiento.
* Entrenar un modelo de detección de objetos.
* Evaluar el desempeño del modelo mediante pruebas reales.
* Analizar una posible implementación industrial o comercial de la solución desarrollada.

## Tecnologías Utilizadas

* Python 3.x
* YOLOv8
* OpenCV
* NumPy
* Matplotlib
* PyTorch
* Git y GitHub

## Estructura del Proyecto

```text
Proyecto-YOLO/
│
├── dataset/
│   ├── train/
│   ├── valid/
│   └── test/
│
├── evidencias/
│
├── notebooks/
│
├── src/
│
├── README.md
├── requirements.txt
└── .gitignore
```

## Instalación

Clonar el repositorio:

```bash
git clone URL_DEL_REPOSITORIO
```

Entrar al directorio:

```bash
cd Proyecto-YOLO
```

Instalar dependencias:

```bash
pip install -r requirements.txt
```

## Entrenamiento

Ejecutar el script de entrenamiento:

```bash
python src/train.py
```

## Detección

Ejecutar el script de detección:

```bash
python src/detect.py
```

## Dataset

El conjunto de datos utilizado para el entrenamiento se encuentra dentro de la carpeta `dataset`.

Se utilizarán imágenes etiquetadas para entrenar el modelo YOLO y permitir la identificación automática de los objetos seleccionados.

## Evidencias

Las pruebas y resultados obtenidos se almacenarán en la carpeta `evidencias`, donde se incluirán imágenes y videos con las detecciones realizadas por el modelo.

## Caso de Estudio

### Problema a Resolver



### Hardware Propuesto

* Cámara industrial o webcam.
* Computadora con capacidad de procesamiento para ejecutar el modelo.
* Sistema de control o automatización.
* Dispositivo de actuación (brazo robótico, pistón neumático, alarma, etc.).

### Flujo de Funcionamiento

1. La cámara captura imágenes en tiempo real.
2. El modelo YOLO analiza cada imagen.
3. Se identifica el objeto de interés.
4. Se genera una acción basada en el resultado de la detección.
5. El sistema registra o actúa sobre el objeto detectado.

## Resultados



## Repositorio

El código fuente, documentación y evidencias del proyecto se encuentran disponibles en este repositorio de GitHub.

## Licencia

Proyecto desarrollado con fines académicos para la materia de Visión Artificial.
