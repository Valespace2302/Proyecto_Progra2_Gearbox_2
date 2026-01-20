# Proyecto_Progra2_Gearbox_2
# Proyecto Final – Programación II

## Monitoreo y detección de fallas en una caja de engranajes

Este proyecto analiza señales de vibración de una caja de engranajes
utilizando el dataset **NASA PHM 2009 – Gearbox Fault Detection**.
El objetivo es detectar fallas mecánicas mediante análisis estadístico
de la señal en el dominio del tiempo.

---

## Objetivo
Implementar un sistema básico de monitoreo de vibraciones que permita:
- Analizar señales normales y con falla
- Extraer características estadísticas
- Detectar anomalías mediante umbrales
- Visualizar resultados con gráficos

---

## Estructura del repositorio
Proyecto_Progra2_Gearbox/
├── data/
│ ├── Run_9.csv
│ ├── Run_88.csv
│ └── features.csv
├── Gearbox_Fault_Detection_Dataset_-PHM_2009(NASA).ipynb
└── README.md


---

## Cómo ejecutar
1. Abrir el archivo Gearbox_Fault_Detection_Dataset_-_PHM_2009_(NASA).ipynb en Google Colab o Jupyter Notebook.
2. Verificar que los archivos CSV estén en la carpeta `data/`.
3. Ejecutar las celdas del notebook en orden.
4. El notebook genera gráficos y un archivo `features.csv` con las estadísticas por ventana.

---

## Resultados
El análisis de vibraciones permitió caracterizar el comportamiento del sistema de engranajes bajo condiciones normales y con falla.
La señal de vibración en condición normal presenta amplitudes estables, mientras que la condición con falla muestra mayor variabilidad y picos más elevados.

Mediante el ventaneo de la señal y la extracción de características estadísticas (media, desviación estándar, RMS y valor pico), se generó una tabla de features por ventana.
El valor RMS fue utilizado como indicador principal para la detección de anomalías.

Se definió un umbral basado en el comportamiento normal del sistema. Las ventanas que superan este umbral fueron marcadas como anómalas, permitiendo identificar eventos de posible falla y calcular el porcentaje de tiempo fuera de rango como KPI.

Como resultado del procesamiento, se generó el archivo features.csv, el cual contiene las características estadísticas por ventana y es utilizado para el análisis y la detección de fallas.
- Gráficos de señal de vibración (normal vs falla)
- Detección de anomalías mediante RMS
- KPI de porcentaje de ventanas fuera de rango
- Simulación masa–resorte–amortiguador

---



