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
- [Aplicar técnica de análisis](#aplicar-técnica-de-análisis)
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
+ Identificar valores nulos a través `COUNTIF` e `IS NULL`.
+ Identificar duplicados a través de `COUNT`, `GROUP BY`, `HAVING`.
+ Identificar datos discrepantes en variables categóricas con `REGEXP_REPLACE`.
+ Identificar datos discrepantes en variables numéricas con `MAX`, `MIN` y `AVG`.
+ Comprobar y modificar tipos de datos con `SAFE_CAST` y `CAST`.
+ Crear nuevas variables.
+ Unir las tablas utilizando `LEFT JOIN`.

## 🔎Análisis exploratorio
El análisis exploratorio se llevó a cabo en Power BI, cargando el consolidado desde BigQuery.

+ Agrupar y visualizar datos según variables categóricas:
  - Se agruparon retrasos y cancelaciones por aerolíneas, aeropuertos, rutas y motivos.
+ Aplicar medidas de tendencia central y dispersión:
  - Se calcularon medidas de tendencia central (media, mediana) y dispersión (mínimo, máximo, desviación estándar) para los retrasos.
+ Visualizar el comportamiento de los datos a lo largo del tiempo:
  - Se observó el comportamiento de los retrasos y cancelaciones durante el mes de enero, así como el promedio de minutos de retraso por hora del día.
+ Calcular cuartiles:
  - Se calcularon cuartiles para la variable `DISTANCE`.
+ Calcular correlación entre variables:
  - Se realizó una matriz de correlación en Google Colab.
 
## 〽 Aplicar técnica de análisis 

### Calculo de riesgo relativo

Se ha calculado el riesgo relativo utilizando los comandos `WITH`, `COUNT`, `COUNTIF`, `CASE`, `WHEN`, `MIN`, y `MAX` en BigQuery para los retrasos. La muestra se segmentó a partir de aerolíneas, aeropuertos, rutas, motivos y horas. Además, se hizo una segmentación por cuartiles para la distancia. Por último, se calculó el riesgo relativo para cancelaciones por motivo.

El riesgo relativo se define como:

Técnica estadística que estima la probabilidad de que ocurra un evento particular en un grupo especifico en comparación con otro grupo.

**Riesgo Relativo (RR)** = \[Tasa de Incidencia en el Grupo Expuesto\] / \[Tasa de Incidencia en el Grupo No Expuesto\]

## ✔ Validación de hipótesis 

La validación de hipótesis se llevó a cabo en BigQuery.

Análisis de correlación entre métricas (Coeficiente de Pearson)
Riesgo relativo





