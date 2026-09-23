ConnectaTel – Análisis de Comportamiento de Clientes
📌 Descripción del proyecto

ConnectaTel es una empresa de telecomunicaciones en Latinoamérica. Este proyecto analiza el comportamiento de sus clientes con datos registrados hasta 2024, con el objetivo de construir un perfil estadístico de los usuarios, detectar comportamientos atípicos y crear segmentos de clientes que apoyen decisiones de retención y diseño de planes.

📂 Datasets utilizados

-  plans.csv → información de los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).

-  users.csv → información de los clientes (edad, ciudad, fecha de registro, plan, churn).

-  usage.csv → detalle del uso real de los servicios (llamadas y mensajes), a nivel evento.

🧩 Etapas del análisis

-  Carga y exploración — revisión de estructura, tipos de dato y forma de cada dataset.

-  Detección de problemas de calidad — valores nulos, sentinels (-999 en edad, "?" en ciudad) y fechas fuera de rango.

-  Limpieza de datos — corrección de sentinels, fechas inválidas y verificación de nulos MAR (Missing At Random) en duration/length.

-  Construcción de user_profile — agregación de usage por usuario (mensajes, llamadas, minutos) y combinación con users.

-  Distribuciones y outliers — histogramas por plan y detección de valores atípicos con boxplots + método IQR.

-  Segmentación de clientes — clasificación por nivel de uso (grupo_uso) y por edad (grupo_edad).

-  Insight ejecutivo — hallazgos y recomendaciones de negocio para el equipo de Estrategia de ConnectaTel.


▶ Cómo abrir el notebook en Google Colab

Open In Colab O manualmente:

Abre notebooks/S7_ConnectaTel_analysis.ipynb en GitHub.

Haz clic en Open in Colab.

📘 Cómo reproducir el análisis

1.  Abre el notebook en Colab o Jupyter.
2.  Ejecuta las celdas en orden, de arriba hacia abajo.
3.  El notebook carga automáticamente plans.csv, users_latam.csv y usage.csv desde /datasets/.
4.  Librerías necesarias: pandas, seaborn, matplotlib (preinstaladas en Colab).

🧠 Objetivo del análisis

Identificar y corregir problemas de calidad en los datos de ConnectaTel.

Construir un perfil de uso por cliente combinando datos de registro y de consumo.

Detectar patrones de uso extremo (outliers) y evaluar si representan errores o comportamiento real de clientes.

Segmentar clientes por edad y nivel de uso para identificar oportunidades comerciales y de retención.
