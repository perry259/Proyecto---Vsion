# Sistema de Visión Artificial para Detección de Cascos de Seguridad mediante YOLO

## Integrantes

* Marco Lopez
* Jesus Baez

---

# Descripción del Proyecto

Este proyecto tiene como objetivo implementar un sistema de Visión Artificial utilizando un modelo de la familia YOLO (You Only Look Once) para la detección automática de equipo de seguridad industrial, específicamente cascos de protección.

El modelo será entrenado mediante un conjunto de imágenes etiquetadas para reconocer la presencia de cascos en un entorno laboral, con la finalidad de proponer una solución aplicable dentro de un almacén o línea de producción donde se requiera mantener los estándares de seguridad.

---

# Objetivo

Desarrollar un modelo de detección de objetos capaz de identificar el uso correcto de casco de seguridad mediante imágenes o video en tiempo real, demostrando cómo una solución basada en inteligencia artificial puede integrarse en procesos industriales para mejorar la supervisión y prevención de riesgos.

---

# Tecnologías Utilizadas

* Python 3.x
* YOLOv8
* OpenCV
* PyTorch
* NumPy
* Matplotlib
* GitHub

---

# Estructura del Proyecto

```text
YOLO-Cascos/
│
├── dataset/
│   ├── train/
│   ├── valid/
│   ├── test/
│   └── data.yaml
│
├── src/
│   ├── train.py
│   └── detect.py
│
├── evidencias/
│   ├── imagenes de prueba
│   └── videos de detección
│
├── requirements.txt
│
└── README.md
```

---

# Instalación

Clonar el repositorio:

```bash
git clone (https://github.com/perry259/Proyecto---Vsion.git)
```

Ingresar a la carpeta del proyecto:

```bash
cd YOLO-Cascos
```

Instalar las dependencias:

```bash
pip install -r requirements.txt
```

---

# Entrenamiento del Modelo

El modelo YOLO será entrenado utilizando un dataset de imágenes etiquetadas con elementos relacionados al equipo de seguridad industrial.

Para iniciar el entrenamiento ejecutar:

```bash
python src/train.py
```

Durante el entrenamiento el modelo aprenderá las características visuales necesarias para identificar los cascos de seguridad.

---

# Prueba del Modelo

Para realizar detecciones en nuevas imágenes:

```bash
python src/detect.py
```

El modelo generará predicciones indicando la ubicación del objeto detectado mediante cuadros delimitadores (bounding boxes).

---

# Dataset

El dataset utilizado contiene imágenes relacionadas con seguridad industrial, donde se encuentran objetos etiquetados para permitir el entrenamiento supervisado del modelo YOLO.

Las imágenes son divididas en:

* Train: imágenes utilizadas para entrenar el modelo.
* Validation: imágenes utilizadas para evaluar el aprendizaje durante el entrenamiento.
* Test: imágenes utilizadas para comprobar el funcionamiento final.

---

# Caso de Estudio: Implementación Industrial

## Problema a Resolver

En ambientes industriales como almacenes y líneas de producción es necesario asegurar que los trabajadores utilicen correctamente su equipo de protección personal (EPP).

Actualmente muchas inspecciones se realizan de manera manual, lo que puede provocar errores humanos o falta de supervisión constante.

La propuesta es implementar un sistema automático capaz de detectar si los trabajadores cuentan con casco de seguridad antes de ingresar o durante su actividad dentro del área industrial.

---

# Hardware Propuesto

El sistema estaría compuesto por:

* Cámara industrial o cámara IP instalada en puntos estratégicos.
* Computadora industrial con capacidad de procesamiento para ejecutar YOLO.
* Sistema de comunicación con PLC.
* Pantalla de monitoreo.
* Sistema de alarma o señalización.

---

# Flujo de Funcionamiento

1. Una cámara captura imágenes del área de trabajo.
2. El modelo YOLO analiza cada imagen en tiempo real.
3. El sistema identifica si existe presencia de casco de seguridad.
4. Si el trabajador cumple con el estándar:

   * Permite continuar el proceso.
5. Si detecta ausencia de casco:

   * Envía una alerta al sistema de control.
   * Puede activar una alarma visual o sonora.
   * Puede detener temporalmente la línea de producción.

---

# Aplicación en una Línea de Producción

El sistema podría instalarse en el acceso a una zona industrial o cerca de una línea de producción.

Cuando un operador ingresa al área de trabajo, la cámara verifica automáticamente el cumplimiento del equipo de seguridad.

La información generada por el modelo puede enviarse a un PLC industrial para tomar decisiones automáticas y ayudar a mantener los estándares de seguridad.

---

# Evidencias

Dentro de la carpeta `evidencias` se almacenarán:

* Imágenes con detecciones realizadas por YOLO.
* Capturas del modelo funcionando.
* Videos de prueba.

---

# Resultados Esperados

Se espera obtener un modelo capaz de reconocer correctamente cascos de seguridad y demostrar una aplicación práctica de la Visión Artificial dentro de un ambiente industrial.

---

# Repositorio

Este repositorio contiene:

* Código fuente del entrenamiento y pruebas.
* Configuración del modelo.
* Dataset utilizado.
* Evidencias del funcionamiento.
* Documentación del caso de estudio.

---

# Licencia

Proyecto realizado con fines académicos para la materia de Visión Artificial.
