
Análisis de Siniestralidad Mortal en Accidentes de Tráfico en Madrid
Este repositorio contiene un Análisis Exploratorio de Datos (EDA) exhaustivo sobre la siniestralidad mortal en accidentes de tráfico ocurridos en la ciudad de Madrid entre los años 2019 y 2023. El objetivo principal es proporcionar a una aseguradora insights clave para optimizar sus modelos de tarificación de seguros a todo riesgo, basándose en una comprensión profunda de los factores de riesgo asociados a las fatalidades.

1. Visión General del Proyecto
En el competitivo sector asegurador, la precisión en la tarificación es fundamental. Este proyecto aborda la necesidad de una aseguradora de refinar sus primas para seguros de vehículos, mediante la identificación de patrones y contextos de mayor riesgo de mortalidad en accidentes de tráfico en Madrid. El análisis se enfoca en factores como la evolución temporal, las condiciones climáticas, el tipo de vehículo, el tipo de accidente, la ubicación geográfica (distrito) y el rango de edad.

2. Contenido del Repositorio
README.md: Este archivo, que proporciona una descripción general del proyecto.
memoria_proyecto.pdf (o .docx/.md): El documento principal que detalla la introducción, metodología, resultados, conclusiones y las implicaciones estratégicas para la aseguradora.
notebooks/:
Madrid_traffic_accidents.ipynb: El Jupyter Notebook que contiene todo el código Python utilizado para la carga de datos, limpieza, transformación, análisis exploratorio y generación de visualizaciones.
data/:
traffic_accidents_clean.csv: El dataset original utilizado para el análisis.
.
3. Metodología
El Análisis Exploratorio de Datos se llevó a cabo siguiendo un proceso estructurado:

Carga y Limpieza de Datos:
Lectura del dataset traffic_accidents_clean.csv.
Conversión de la columna fecha a formato datetime.
Gestión de valores faltantes en columnas categóricas (imputación por moda) y numéricas (imputación por media).
Eliminación de registros duplicados.
Transformación y Creación de Variables:
Generación de la variable binaria num_muertes (1 para fallecido, 0 para no fallecido).
Categorización de la hora_24h en franja_horaria (Madrugada, Mañana, Tarde, Noche).
Análisis de Factores de Riesgo:
Cálculo de Muertes Absolutas (conteo directo).
Cálculo de la Tasa de Mortalidad por 100 Accidentes (indicador de letalidad).
Cálculo de la Proporción de Muertes Totales (contribución al total de fatalidades).
Análisis y visualización para los siguientes factores:
Evolución anual.
Condiciones climáticas.
Tipo de vehículo.
Tipo de accidente.
Distrito geográfico en Madrid.
Rango de edad de los implicados.

4. Resultados Clave y Conclusiones (Resumen)
El análisis ha arrojado conclusiones significativas para la aseguradora:

Tendencia General: La siniestralidad mortal en Madrid mostró un descenso entre 2021-2022 (posiblemente por la pandemia), con un leve repunte en 2023.
Condiciones Climáticas: La mayoría de las muertes absolutas ocurren en días despejados (alta frecuencia de tráfico), pero los accidentes bajo condiciones nubladas o de lluvia intensa son proporcionalmente más letales.
Tipo de Vehículo: Las motocicletas (>125cc) presentan, con diferencia, la tasa de mortalidad más alta por accidente, destacando su vulnerabilidad intrínseca.
Tipo de Accidente: El despeñamiento es el más letal si ocurre, pero los atropellos a personas son el tipo de accidente que más contribuye a las muertes absolutas anuales en Madrid, debido a su mayor frecuencia en el entorno urbano.
Distrito: Moncloa-Aravaca y Fuencarral-El Pardo muestran las tasas de letalidad más altas por accidente. La contribución absoluta de muertes varía anualmente entre distritos clave como Centro, Latina y Hortaleza.
Rango de Edad: El grupo "75+" es consistentemente el más letal en caso de accidente y, en los últimos años, el que más contribuye a las muertes absolutas en Madrid.

5. Implicaciones Estratégicas para Aseguradoras
Estos hallazgos son fundamentales para:

Tarificación Basada en Riesgo: Ajustar primas para motocicletas, conductores de edad avanzada, y según el distrito de residencia/operación, reflejando la letalidad inherente de cada factor.
Desarrollo de Productos: Diseñar coberturas específicas y ofertas adaptadas a riesgos identificados (ej., coberturas mejoradas para motos, productos para seniors).
Marketing Dirigido: Crear campañas de comunicación que eduquen a los clientes sobre los riesgos específicos y promuevan una conducción más segura en Madrid.
Responsabilidad Social Corporativa (RSC): Liderar iniciativas de seguridad vial en colaboración con autoridades locales, enfocadas en grupos de edad vulnerables, tipos de accidente de alto riesgo (atropellos) y distritos clave.

6. Requisitos
Este proyecto se ejecuta con Python y las siguientes librerías:

pandas
numpy
matplotlib
seaborn
Puedes instalar estas librerías usando pip:

pip install pandas numpy matplotlib seaborn

7. Uso
Para replicar el análisis:

Clona este repositorio:


git clone https://github.com/Porpi01/Madrid-traffic-accidents-analysis.giy
cd nombre_del_repositorio
Asegúrate de tener los datos traffic_accidents_clean.csv en la carpeta data/.
Abre el Jupyter Notebook Madrid_traffic_Accidents.ipynb en tu entorno preferido (Jupyter Lab, Jupyter Notebook, VS Code).
Ejecuta las celdas secuencialmente para realizar el EDA y generar las visualizaciones.