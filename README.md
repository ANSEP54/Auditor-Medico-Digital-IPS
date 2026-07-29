# Auditor-Medico-Digital-IPS
Prototipo de inteligencia artificial para la detección preventiva de inconsistencias entre historia clínica y prefactura en una IPS.
# Auditor Médico Digital H&L

Prototipo de inteligencia artificial para la detección preventiva
de inconsistencias entre historia clínica y prefactura en una
Institución Prestadora de Servicios de Salud.

## Descripción

El sistema cruza automáticamente archivos de atenciones, historia
clínica y prefactura para identificar posibles inconsistencias antes
de la emisión final del cobro.

La solución combina reglas administrativas explicables con una red
neuronal desarrollada en TensorFlow y Keras.

## Funcionalidades

- Identificación de procedimientos realizados y no facturados.
- Detección de servicios facturados sin registro clínico.
- Detección de cantidades discordantes.
- Cálculo de probabilidad de inconsistencia.
- Clasificación en alerta, revisión preventiva o aprobación.
- Estimación de valores potencialmente no facturados.
- Estimación de valores expuestos a glosas o rechazos.
- Interfaz web desarrollada con Gradio.
- Generación de resultados descargables.

## Archivos de entrada

El prototipo recibe tres archivos CSV:

1. Atenciones.
2. Historia clínica detallada.
3. Prefactura.

Los archivos utilizados públicamente deben contener únicamente datos
simulados o anonimizados.

## Modelo de inteligencia artificial

La solución utiliza una red neuronal densa con 12 variables predictoras.

Resultados obtenidos en el conjunto de prueba:

- Exactitud: 91,53 %
- Precisión: 86,11 %
- Recall: 67,39 %
- F1-score: 75,61 %
- ROC-AUC: 84,13 %
- PR-AUC: 78,36 %

## Resultados operativos

- 3.124 registros procesados.
- 926 alertas generadas.
- 968 revisiones preventivas.
- 1.230 registros aprobados.
- $112.689.000 potencialmente no facturados.
- $131.163.000 expuestos a posibles glosas o rechazos.

Los valores económicos corresponden a estimaciones realizadas con los
datos suministrados para el proyecto y no representan pérdidas
financieras definitivas.

## Tecnologías utilizadas

- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- TensorFlow/Keras
- Gradio
- Matplotlib
- OpenPyXL

## Uso

1. Abrir el archivo `Auditor_IPS.ipynb` en Google Colab.
2. Ejecutar las celdas en orden.
3. Cargar los archivos CSV solicitados.
4. Ejecutar la auditoría preventiva.
5. Consultar y descargar los resultados.

## Limitaciones

El sistema es una herramienta académica de apoyo y no reemplaza el
criterio del auditor médico ni la validación administrativa de la IPS.

La pertinencia clínica no puede determinarse únicamente mediante los
códigos CIE-10 y CUPS.

## Autora

Angie Sepúlveda  
Administradora en Salud  
Proyecto Capstone – Samsung Innovation Campus  
2026
