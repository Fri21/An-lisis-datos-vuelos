# Laboratoria

## 🛫 Análisis-datos-vuelos
![shutterstock_66961171](https://github.com/user-attachments/assets/a48cfcd2-79d6-497b-9f36-1f66030448ea)

# 📑Temas

- [Introducción](#introducción)
- [Hipótesis a validar o refutar](#hipótesis-a-validar-o-refutar)
- [Objetivo](#objetivo)
- [Equipo](#equipo)
- [Herramientas de apoyo](#herramientas-de-apoyo)
  - [Procesamiento de los datos](#procesamiento-de-los-datos)
  - [Análisis exploratorio](#análisis-exploratorio)
  - [Validación de hipótesis](#validación-de-hipótesis)
- [Resultados](#resultados)
- [Conclusiones](#conclusiones)
- [Recomendaciones](#recomendaciones)

- ## 📄Introducción

- El transporte aéreo en Estados Unidos es fundamental para conectar miles de destinos diariamente, pero los retrasos y cancelaciones pueden tener un impacto considerable en las operaciones, la satisfacción de los pasajeros y los costos operativos de las aerolíneas. Este proyecto se centra en analizar los patrones de retraso y cancelación de vuelos durante enero de 2023, un mes clave que presenta una amplia gama de desafíos logísticos y meteorológicos.

El objetivo principal es identificar factores determinantes que influyen en la puntualidad de los vuelos, incluyendo rutas, aeropuertos, aerolíneas, tiempos del día y motivos específicos de retraso y cancelación. A través de este análisis, se pretende ofrecer insights útiles para mejorar la planificación y optimización de las operaciones aéreas, así como para comprender mejor el comportamiento de las aerolíneas y aeropuertos en términos de eficiencia operativa.

Mediante la aplicación de técnicas de análisis estadístico y visualización de datos, este proyecto busca proporcionar una comprensión más profunda sobre los patrones de retraso, lo que permitirá a los interesados en la industria tomar decisiones más informadas y estratégicas para reducir las demoras y mejorar la experiencia de los pasajeros.

## 📈Hipótesis a validar o refutar

+ Aerolíneas: Algunas aerolíneas tienen un historial de retrasos significativamente mayor que otras.
+ Aeropuertos: Algunos aeropuertos tienden a tener retrasos más frecuentes o severos en comparación con otros.
+ Duración del Vuelo: Los vuelos más largos tienden a tener mayores tiempos de retraso en comparación con los vuelos más cortos.
+ Horas del Día: Los retrasos en los vuelos son más comunes durante las horas punta del día.
+ Motivos de Retraso: Algunos motivos de retraso son más prevalentes que otros, indicando causas específicas más comunes para el retraso de vuelos.
+ Códigos de Cancelación: Algunos códigos de cancelación son más prevalentes que otros, indicando causas específicas más comunes para la cancelación de vuelos.

## 🎯Objetivo

"Evaluar y caracterizar los patrones de retraso y cancelaciones en los vuelos de Estados Unidos durante enero de 2023, con el fin de identificar rutas, aeropuertos, aerolíneas y factores específicos que contribuyen significativamente a estos retrasos, utilizando técnicas de análisis estadístico como las correlaciones y el riesgo relativo."

## 👩🏻‍🤝‍👩🏻Equipo
- [Frida Castillo](https://github.com/Fri21)
- [Jaqueline Mera](https://github.com/JaquelineMera)

- ## ⚙Herramientas de apoyo
<details>
<summary> ⚙️ Lenguajes </summary>

+ SQL
+ Python

</details>

<details>
<summary> ⚙️ Herramientas </summary>

+ Google BigQuery
+ Google Colab
+ Canva
+ Power Bi

</details>

## 💻Procesamiento de los datos
+ Identificar valores nulos a través COUNTIF e IS NULL.
+ Identificar duplicados a través de COUNT, GROUP BY, HAVING.
+ Identificar datos discrepantes en variables categóricas con REGEXP_REPLACE.
+ Identificar datos discrepantes en variables numéricas con MAX, MIN y AVG.
+ Comprobar y modificar tipos de datos con SAFE_CAST y CAST.
+ Crear nuevas variables DAY OF WEEK: Día de la semana a partir de FORMAT_DATE, ROUTE_CITY: Ruta de ciudad a ciudad a partir de ORIGIN_CITY y DEST_CITY, ROUT_AIRPORT: Ruta de aeropuerto a aeropuerto a partir de ORIGIN y DEST, HOUR_CRS_DEP_T: Hora del día a partir de EXTRACT y TIME, DISTANCE_QUARTILE: Número de cuartil por distancia a partir de NTILE(4), TOTAL_DELAY: Suma de los 5 motivos de DELAY, es el total de minutos, TOTAL_NUM_DELAY: Identifica si hay retraso o no, 1 para retraso, 0 sin retraso, STATUS_VUELO: Identifica si es un vuelo está, A TIEMPO, RETRASO, DESVIADO y CANCELADO, STATUS_VUELO_DES: Descripción de STATUS VUELO, describe, el tipo principal del retraso o la multifactorialidad del mismo, describe, el tipo de cancelado, además, asigna la etiqueta a desviados y a tiempo, EXCLUDING_CARRIER: Grupo no expuesto de Carrier, EXCLUDING_WEATHER: Grupo no expuesto de Weather, EXCLUDING_NAS: Grupo no expuesto de NAS, EXCLUDING_SECURITY: Grupo no expuesto de SECURITY, EXCLUDING_LATE_AIRCRAFT: Grupo no expuesto LATE AIRCRAFT. 
+ Construir tablas auxiliares utilizando WITH.
+ Unir las tablas utilizando LEFT JOIN.

## 🔎Análisis exploratorio
+ Agrupar datos según variables categóricas a través de tablas
+ Visualizar las variables categóricas a través de gráficos de barras y líneas 
+ Aplicar medidas de tendencia central en BPM, Playlists y Streams
+ Aplicar medidas de dispersión BPM, Playlists y Streams
+ Visualizar distribución a través de Hitogramas BPM, Playlists y Streams
