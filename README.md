# Proyecto individual de Data Analytics sobre Siniestros Viales

![wink](https://i.imgur.com/902EI23.jpeg)

## Introducción 📑

En este proyecto se realiza un analisis sobre siniestros viales en la Ciudad Autonoma de Buenos Aires (CABA), con el fin de generar información que le permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales. Para ello, el Observatorio de Movilidad y Seguridad Vial (OMSV), centro de estudios que se encuentra bajo la órbita de la Secretaría de Transporte del Gobierno de la Ciudad Autónoma de Buenos Aires nos disponibilizan un dataset oficial del gobierno de Argentina en donde se encuentra toda la información. En los datos hay información acerca de los siniestros viales que ocurrieron entre los años 2016 y 2021, además de información útil para llevar a cabo el análisis sin poner en peligro la identidad de los involucrados.

## Contexto 📜

Los siniestros viales, también conocidos como accidentes de tráfico o accidentes de tránsito, son eventos que involucran vehículos en las vías públicas y que pueden tener diversas causas, como colisiones entre automóviles, motocicletas, bicicletas o peatones, atropellos, choques con objetos fijos o caídas de vehículos. Estos incidentes pueden tener consecuencias que van desde daños materiales hasta lesiones graves o fatales para los involucrados.

En Argentina, cada año mueren cerca de 4.000 personas en siniestros viales. Aunque muchas jurisdicciones han logrado disminuir la cantidad de accidentes de tránsito, esta sigue siendo la principal causa de muertes violentas en el país.

El Observatorio de Movilidad y Seguridad Vial (OMSV) solicita la elaboración de un proyecto de análisis de datos, con el fin de generar información que le permita a las autoridades locales tomar medidas para disminuir la cantidad de víctimas fatales de los siniestros viales.

## Objetivo 🚀

A través de este estudio, buscamos:

- Comprender las principales causas de accidentes de tráfico en Buenos Aires.
- Identificar los grupos más vulnerables.
- Descubrir patrones relacionados con horarios y lugares con la mayor incidencia de accidentes.
- Ofrecer recomendaciones basadas en los hallazgos para mejorar la seguridad vial para la prevención de siniestros viales e implementación de políticas efectivas y así
disminuir la cantidad de víctimas fatales en la Ciudad de Buenos Aires, Argentina.

## Fuente de datos 📁

Este proyecto se desarrolló en base al dataset otorgado por el gobierno de CABA, denominado Homicidios, que se encuentra en formato de Excel y contiene dos hojas de datos:

Hechos: contiene datos específicamente relacionados a los siniestros como lo son la fecha y hora del siniestro, cantidad de víctimas, el lugar de hecho, la comuna, la dirección, la geolocalización, el tipo de víctima y los acusados.

Víctimas: contiene datos relacionados con las víctimas y estos son la edad, el sexo, el rol, la fecha de fallecimiento, así como también la fecha del siniestro.
Se vincula a los hechos mediante el id del hecho.

En este documento se detallan todas las definiciones manejadas en los datos y en el desarrollo de este proyecto. En [este link](https://data.buenosaires.gob.ar/dataset/victimas-siniestros-viales) se encuentran los datos utilizados en el análisis.

## Tecnologías utilizadas ⚡

Partimos con los datos fuentes en formato .xlsx y se utilizó **Python** y **Pandas** para los procesos de extracción, transformación y carga de los datos, como así también para el análisis exploratorio de los datos.

Durante el desarrollo del proyecto se hizo uso de librerias como **Seaborn**, **Numpy** y **Matplotlib**.

Finalmente, para la construcción de un dashboard interactivo se utiliza **Power BI**, el cuál se puede [consultar aquí](https://github.com/rafaelopz1/PI2SiniestrosViales/blob/main/dashboard/Siniestros_viales.pbix).
Puedes encontrar el [Dashboard online e interactivo aquí](https://www.novypro.com/project/análisis-de-siniestros-viales-en-caba-argentina).

Se usó el control de versiones **Git** para desarrollar y publicar el proyecto en este repositorio.

## ETL y EDA 📊

Preparación de datos:

Primero, se realizó un proceso de ETL para organizar y limpiar los datos de "HECHOS" y "VÍCTIMAS". Se ajustaron los nombres de las variables, se examinaron los registros en busca de valores nulos y duplicados, y se descartaron columnas redundantes o con información incompleta. Tras estas tareas, ambos conjuntos de datos de "Homicidios" se combinaron en uno solo llamado df_homicidios.

Análisis exploratorio:

Luego, se llevó a cabo un análisis exploratorio exhaustivo (EDA) para descubrir patrones en los datos. El objetivo era obtener información útil que las autoridades locales pudieran utilizar para tomar medidas y reducir el número de víctimas mortales por homicidios. Para más detalles sobre el EDA, consulte el [notebook EDA](https://github.com/rafaelopz1/PI2SiniestrosViales/blob/main/EDA.ipynb)

## Análisis destacados 📊

Se realizó un análisis de los homicidios en diferentes escalas temporales. Alrededor del 60% de las víctimas fatales se distribuyeron en los primeros tres años del conjunto de datos, con una notable disminución en 2020 debido a la cuarentena por COVID-19. Aunque hubo un pico de víctimas en diciembre, esta tendencia no se repitió claramente en los distintos años, y se atribuye a la flexibilización de las medidas de cuarentena.

El 70% de las víctimas fatales ocurrieron de lunes a viernes, lo cual podría estar relacionado con los desplazamientos diarios al trabajo. Sin embargo, no se encontraron diferencias significativas en la distribución semanal, lo que indica que la cantidad de víctimas los sábados y domingos es similar en general.

En cuanto a las franjas horarias, se registró un mayor número de víctimas (12% del total) entre las 6 y las 8 de la mañana, lo cual sugiere el impacto de los desplazamientos laborales. Sin embargo, dentro de esta franja horaria, el 55% de las víctimas ocurrieron durante los fines de semana.

Al analizar el perfil de las víctimas, se encontró que el 77% eran hombres. Casi la mitad de las víctimas se encontraban en el rango de edad de 25 a 40 años, y el 84% de ellos eran hombres.

En cuanto al rol de la víctima, se determinó que el 48% eran conductores. De estos conductores, el 77% se movilizaba en moto y el 19% en auto. En términos de medios de transporte, el 42% de las víctimas eran conductores de moto, y el 88% de estos conductores de moto eran hombres.

En cuanto a la responsabilidad en los hechos, los autos estuvieron implicados en el 29% de los casos, mientras que el 75% involucró a vehículos como autos, colectivos y camione

En cuanto a la distribución espacial de los hechos, se destacó que en todas las comunas de CABA los accidentes se concentraron en las avenidas. El 62% de las víctimas perdieron la vida en estas avenidas, y el 82% de estos accidentes ocurrieron en los cruces de las avenidas con otras calles. Este patrón se mantuvo consistente a lo largo de los años. Además, el rol de la víctima al momento del hecho varió entre moto y peatón en diferentes comunas.

## KPI ✔️

Se plantearon 3 KPIs (Indicadores clave de proceso), en relación a la disminución de la cantidad de víctimas fatales de los siniestros viales. A continuación se enlistan los KPIs utilizados.

> 1. Reducir en un 10% la tasa de homicidios en siniestros viales de los últimos seis meses, en CABA, en comparación con la tasa de homicidios en siniestros viales del semestre anterior
>
> Las tasas de mortalidad relacionadas con siniestros viales suelen ser un indicador crítico de la seguridad vial en una región. Se define como Tasa de homicidios en siniestros viales al número de víctimas fatales en accidentes de tránsito por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico, en este caso se toman 6 meses. Su fórmula es: (Número de homicidios en siniestros viales / Población total) * 100,000

En el año 2021, la Tasa de homicidios en siniestros viales se estableció en 1.77, lo que indica que durante los primeros seis meses de ese año ocurrieron aproximadamente 1.77 homicidios en accidentes de tránsito por cada 100,000 habitantes. El objetivo planteado consistía en reducir esta tasa en un 10% para el siguiente semestre de 2021, es decir, alcanzar un valor de 1.60. Al calcular el indicador clave de desempeño (KPI) para este período, se obtuvo una Tasa de homicidios en siniestros viales de 1.35, lo que significa que se logró cumplir con el objetivo propuesto para el segundo semestre de 2021.


> 2. Reducir en un 7% la cantidad de accidentes mortales de motociclistas en el último año, en CABA, respecto al año anterior.
>
> Durante el análisis exploratorio, se observó que el 42% de las víctimas mortales se encontraban utilizando motos al momento del hecho. Por lo tanto, se consideró importante proponer el seguimiento de la cantidad de accidentes mortales que involucran a este tipo de conductores. La fórmula utilizada para medir la evolución de estos accidentes mortales con víctimas en moto es: (Número de accidentes mortales con víctimas en motocicletas en el año anterior - Número de accidentes mortales con víctimas en moto en el año actual) / (Número de accidentes mortales con víctimas en moto en el año anterior) * 100

Se determinó la Cantidad de accidentes mortales de motociclistas para el año 2020, que arrojó un valor de -44.00. Esto estableció un objetivo de -40.92 para el mismo año, lo que representaba una reducción del 7%. Al calcular la Cantidad de accidentes mortales de motociclistas para el año 2021, se obtuvo un valor de 64.29, lo que indica un aumento del 64% en la cantidad de fallecimientos de conductores de motocicletas en comparación con el año anterior.

> 3. Reducir en un 10% la tasa de homicidios en las avenidas en el último año, en CABA, respecto al año anterior
>
> Durante el análisis exploratorio, se observó que el 62% de las víctimas mortales se encontraban transitando por avenidas al momento del hecho. La Tasa de homicidios en las avenidas se define como el número de víctimas fatales en accidentes de tránsito en avenidas por cada 100,000 habitantes en un área geográfica durante un período de tiempo específico, en este caso, anual. La fórmula utilizada para calcular esta tasa es: (Número de hechos mortales con víctimas en avenidas / Total pobación) * 100,000

En 2020, la Tasa de homicidios en las avenidas se calculó en 1.68. A partir de este valor, se estableció un objetivo de 1.51 para el año 2021, lo que implicaba una reducción del 10%. Sin embargo, al calcular la tasa para el año 2021, se obtuvo un resultado de 1.97. Esto significa que no solo no se alcanzó el objetivo, sino que la tasa de homicidios en las avenidas aumentó en comparación con el año 2020.

En resumen, mientras que en 2020 se observó una tasa de 1.68 homicidios por cada 100.000 habitantes en las avenidas, en 2021 la tasa aumentó a 1.97, lo que representa un aumento del 17%.

# Dashboard interactivo 🎮

Se desarrolló un dashboard en Power BI con el objetivo de presentar de manera visual y comprensible la información recopilada durante el proyecto. El dashboard cuenta con elementos visuales interactivos que permiten apreciar los cambios al hacer clic en cada uno de ellos. Esta función facilita la explicación de los hallazgos obtenidos, brindando una experiencia más dinámica y comprensible al usuario.

## Conclusiones ‼️

Durante el período comprendido entre 2016 y 2021, se registraron un total de 717 víctimas fatales en accidentes de tránsito. El 70% de estas víctimas ocurrieron durante la semana. En cuanto a la franja horaria, el 17% de los accidentes ocurrieron entre las 5 y las 7 de la mañana. Se observó que el mes de diciembre presentó el mayor número de fallecimientos durante el período analizado.

En términos de género, el 77% de las víctimas fatales fueron hombres, y más de la mitad de ellos (61%) tenían edades comprendidas entre los 18 y 39 años. En cuanto al tipo de usuario, los motociclistas representaron el 42% de las víctimas mortales. Además, se encontró que el 62% de los homicidios ocurrieron en algún punto de las avenidas de CABA, y el 51% de ellos tuvieron lugar en intersecciones entre la autopista y otras calles. En este sentido, el 75% de los accidentes ocurrieron en cruces de calles.

Finalmente, en el segundo semestre del año 2021 se logró cumplir con el objetivo de reducir la tasa de homicidios en siniestros viales. Sin embargo, no se cumplieron los objetivos de disminuir la cantidad de accidentes mortales en motociclistas ni en las avenidas para el año 2021 en comparación con el año 2020.

## Autor
Rafael Oropeza
[Linkedin](https://www.linkedin.com/in/rafael-oropeza-594853151/) 
rafael415oropeza@gmail.com
