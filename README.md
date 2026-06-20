# 🦺 Sistema Inteligente de Detección de Cascos de Seguridad mediante YOLOv8

---

## Alumnos

Marco Antonio Palos López

Jesus Antonio Baez Ortega

Ingeniería Mecatrónica

Proyecto Académico de Visión Artificial

---

## Descripción General

Este proyecto implementa un sistema de Visión Artificial basado en YOLOv8 Nano para la detección automática de cascos de seguridad (helmets) en entornos industriales.

El objetivo principal es apoyar el cumplimiento de las normas de seguridad dentro de almacenes, centros logísticos y áreas de producción, identificando en tiempo real a las personas que no portan correctamente su Equipo de Protección Personal (EPP).

Como etapa futura, este sistema podrá integrarse con alarmas sonoras, sistemas SCADA, PLCs o plataformas de monitoreo industrial para generar alertas automáticas cuando se detecte personal sin casco.

---

## Problema a Resolver

En muchos almacenes y plantas industriales existen zonas donde el uso del casco de seguridad es obligatorio.

La supervisión manual presenta limitaciones:

- Dependencia de supervisores humanos.
- Posibilidad de errores por distracción.
- Dificultad para monitorear múltiples áreas simultáneamente.
- Costos operativos elevados.

Este proyecto propone una solución automatizada basada en Inteligencia Artificial capaz de detectar el uso de cascos de seguridad mediante cámaras de vigilancia.

---

## Objetivos

### Objetivo General

Desarrollar un sistema de detección automática de cascos de seguridad utilizando redes neuronales convolucionales y el modelo YOLOv8 Nano.

### Objetivos Específicos

- Entrenar un modelo de detección de objetos utilizando YOLOv8.
- Detectar automáticamente cascos de seguridad en imágenes.
- Visualizar las detecciones mediante bounding boxes.
- Evaluar el desempeño del modelo utilizando métricas estándar.
- Sentar las bases para una futura integración con sistemas de alerta industrial.

---

## Tecnologías Utilizadas

- Python 3.10+
- Google Colab
- YOLOv8 Nano
- Ultralytics
- OpenCV
- NumPy
- Matplotlib
- Roboflow

---

## Arquitectura del Sistema

```text
Cámara / Imagen
       │
       ▼
Preprocesamiento
(OpenCV)
       │
       ▼
YOLOv8 Nano
(Modelo entrenado)
       │
       ▼
Detección de Cascos
       │
       ▼
Visualización de Resultados
(Bounding Boxes)
       │
       ▼
Futuras Alertas Sonoras
o Integración Industrial
```

---

## Estructura del Proyecto

```text
Proyecto/
│
├── Evidencias/
│   ├── train_batch0.jpg
│   ├── train_batch2.jpg
│   ├── PROYECTO.ipynb
│   └── capturas de resultados
│
├── conjunto de datos/
│   ├── train/
│   │   ├── images/
│   │   └── labels/
│   │
│   ├── valid/
│   │   ├── images/
│   │   └── labels/
│   │
│   ├── test/
│   │   ├── images/
│   │   └── labels/
│   │
│   ├── data.yaml
│   ├── README.dataset.txt
│   └── README.roboflow.txt
│
├── README.md
├── requisitos.txt
└── .gitignore
```

---

## Dataset

El conjunto de datos fue obtenido y anotado mediante Roboflow.

Características:

- Clase detectada: helmet
- Formato: YOLOv8
- División:
  - Entrenamiento (train)
  - Validación (valid)
  - Pruebas (test)

El dataset contiene imágenes de trabajadores utilizando cascos de seguridad en diferentes condiciones de iluminación, distancia y perspectiva.

---

## Entrenamiento del Modelo

Modelo utilizado:

- YOLOv8 Nano (yolov8n)

Parámetros principales:

```python
epochs = 20
imgsz = 640
```

Entrenamiento realizado en:

- Google Colab
- GPU NVIDIA T4

---

## Resultados

El modelo es capaz de:

✅ Detectar cascos de seguridad.

✅ Dibujar bounding boxes automáticamente.

✅ Mostrar el porcentaje de confianza de cada detección.

✅ Procesar imágenes cargadas por el usuario.

Ejemplo de salida:

```text
Cantidad de cascos detectados: 3

Casco 1: 96.41%
Casco 2: 94.12%
Casco 3: 92.87%
```

---

## Aplicaciones Industriales

Este proyecto puede utilizarse como base para:

- Supervisión automática de seguridad.
- Monitoreo de EPP en almacenes.
- Control de acceso a zonas restringidas.
- Prevención de accidentes laborales.
- Integración con sistemas de alarma.
- Integración con PLCs industriales.
- Integración con sistemas SCADA.

---

## Mejoras Futuras

### Detección de Personas sin Casco

Actualmente el sistema detecta únicamente la presencia de cascos.

Una mejora futura consiste en:

1. Detectar personas.
2. Detectar cascos.
3. Relacionar ambas detecciones.
4. Determinar si una persona porta casco.
5. Generar una alerta si no cumple con la normativa.

---

### Sistema de Alarma Sonora

Cuando una persona ingrese a una zona sin casco:

```text
⚠️ ALERTA DE SEGURIDAD

Se detectó personal sin Equipo
de Protección Personal.

Favor de colocarse el casco de seguridad.
```

---

### Implementación en Tiempo Real

Posibles integraciones:

- Cámaras IP.
- CCTV industrial.
- Raspberry Pi.
- NVIDIA Jetson Nano.
- PLC Siemens.
- PLC Allen Bradley.
- Sistemas SCADA.

---

## Instalación

Clonar repositorio:

```bash
git clone https://github.com/perry259/Proyecto---Vsion.git
```

Instalar dependencias:

```bash
pip install -r requisitos.txt
```

---


# Licencia

Proyecto realizado con fines académicos para la materia de Visión Artificial.
