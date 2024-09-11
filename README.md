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
 
## 〽Aplicar técnica de análisis 

Calculo de riesgo relativo

Se ha calculado el riesgo relativo utilizando los comandos `WITH`, `COUNT`, `COUNTIF`, `CASE`, `WHEN`, `MIN`, y `MAX` en BigQuery para los retrasos. La muestra se segmentó a partir de aerolíneas, aeropuertos, rutas, motivos y horas. Además, se hizo una segmentación por cuartiles para la distancia. Por último, se calculó el riesgo relativo para cancelaciones por motivo.

El riesgo relativo se define como:

Técnica estadística que estima la probabilidad de que ocurra un evento particular en un grupo especifico en comparación con otro grupo.

**Riesgo Relativo (RR)** = \[Tasa de Incidencia en el Grupo Expuesto\] / \[Tasa de Incidencia en el Grupo No Expuesto\]

## ✔Validación de hipótesis 

La validación de hipótesis se llevó a cabo en BigQuery.

Análisis de correlación entre métricas (Coeficiente de Pearson)
Riesgo relativo

## 📃Resultados


<details>
<summary> Hipótesis </summary>

 🟢**Hipótesis 1:** Algunas aerolíneas tienen un historial de retrasos significativamente mayor que otras.
 
Resultados: Aproximadamente el 50% de las aerolíneas presentan un riesgo relativo mayor a 1.02 de sufrir retrasos. Validación: Esta hipótesis se valida parcialmente, ya que aunque no todas las aerolíneas tienen un riesgo significativamente mayor, una proporción considerable lo tiene. Conclusión: Existe una variabilidad significativa entre las aerolíneas en cuanto a su historial de retrasos, lo que sugiere que ciertos operadores son menos puntuales que otros. Recomendación: Las aerolíneas con mayor riesgo deberían mejorar sus operaciones internas, optimizando la asignación de recursos y mejorando la planificación logística.

🟡**Hipótesis 2:** Algunos aeropuertos tienden a tener retrasos más frecuentes o severos en comparación con otros.

Resultados: Los aeropuertos con menor número de vuelos registrados tienen mayor riesgo de presentar retrasos. Validación: La hipótesis es válida, pero de manera inversa a lo esperado. Los aeropuertos con menor tráfico son más propensos a retrasos, posiblemente debido a menores infraestructuras o recursos limitados. Conclusión: Los aeropuertos con menor volumen de vuelos pueden tener una menor capacidad para gestionar los vuelos de manera eficiente. Recomendación: Se sugiere mejorar la infraestructura y capacidad operativa en estos aeropuertos con menor tráfico para reducir los retrasos.

![13](https://github.com/user-attachments/assets/bcf0747c-acb2-489c-bc9c-06e279be08a6)

🟢**Hipótesis 3:** Los vuelos más largos tienen mayores tiempos de retraso en comparación con los vuelos más cortos.

Resultados: Los vuelos en los cuartiles 3 y 4, los más largos, tienen un riesgo relativo de 1.06 y 1.11 respectivamente. Validación: La hipótesis es válida, ya que los vuelos más largos presentan un mayor riesgo de retraso, aunque la diferencia no es drástica. Conclusión: Los vuelos más largos tienen una ligera tendencia a sufrir más retrasos, lo que puede deberse a factores operativos o logísticos. Recomendación: Se recomienda una planificación más cuidadosa y la implementación de medidas preventivas adicionales para vuelos de larga distancia.

🟡**Hipótesis 4:** Los retrasos en los vuelos son más comunes durante las horas punta del día.

A partir de los resultados obtenidos, la hipótesis de que los retrasos en los vuelos son más comunes durante las horas punta del día se valida parcialmente. Si bien se registra un mayor número de retrasos a las 6:00 am y entre las 6:00 y 7:00 pm, el mayor riesgo relativo no ocurre en estas horas punta. El mayor riesgo relativo de retrasos (1.98-2.04) se presenta entre las 3:00 y 4:30 am, un periodo que no coincide con las horas de mayor tráfico aéreo. Aunque los retrasos son más frecuentes en las horas punta, el riesgo relativo sugiere que las primeras horas de la mañana, fuera de las horas punta, conllevan un riesgo más elevado de retraso. Por lo tanto, la hipótesis se apoya en términos de frecuencia de retrasos, pero no en relación con el mayor riesgo relativo.

![14](https://github.com/user-attachments/assets/25a8f16a-b6d5-4875-ab0d-32ff804edc04)

🟢**Hipótesis 5:** Algunos motivos de retrasos son más prevalentes que otros, indicando causas específicas más comunes para el retraso de un vuelo.

Resultados: El motivo más común es el retraso por operador, aunque muchos retrasos son multifactoriales. Validación: La hipótesis es válida. El retraso por operador es un motivo destacado, pero la multifactorialidad indica que otros factores también juegan un papel importante. Conclusión: Los retrasos operacionales son la principal causa, pero muchas veces los retrasos están impulsados por múltiples factores, lo que hace más difícil identificar una única causa. Recomendación: Se sugiere una mejor coordinación entre diferentes áreas operativas y mejorar la eficiencia en los procesos de control por parte de las aerolíneas para reducir los retrasos.

🟢**Hipótesis 6:** Algunos códigos de cancelación son más prevalentes que otros, indicando causas específicas más comunes para la cancelación de vuelos.

Resultados: El motivo principal de cancelación es el clima, y presenta el mayor riesgo. Validación: La hipótesis es válida. El clima es la causa principal de cancelación, lo que es comprensible dado su naturaleza incontrolable. Conclusión: Las condiciones climáticas extremas son la principal razón detrás de las cancelaciones, y este es un factor que no puede ser controlado fácilmente. Recomendación: Se recomienda mejorar las comunicaciones sobre previsiones climáticas y desarrollar políticas de cancelación y reprogramación más ágiles para mitigar el impacto de cancelaciones por clima.

![15](https://github.com/user-attachments/assets/569f8740-8d6a-4997-a31d-83ad63ebe91f)

</details>

## 📄Conclusiones


+ El análisis sugiere que las aerolíneas y aeropuertos con menos recursos tienen más riesgos de sufrir retrasos. 

+ Los vuelos más largos, los vuelos en las primeras horas del día y las condiciones climáticas también son factores críticos que afectan la puntualidad y las cancelaciones. 

+ Para reducir el impacto de estos factores, las aerolíneas deben centrarse en mejorar la eficiencia operativa y la planificación estratégica.

## 📝Recomendaciones

+ Implementar mejores estrategias operativas y optimizar el uso de recursos en aerolíneas y aeropuertos con alto riesgo.

+ Revisar los vuelos programados en horas de mayor riesgo y trabajar en estrategias para reducir retrasos en esos periodos.

+ Crear planes de contingencia más efectivos para mitigar retrasos por causas multifactoriales y condiciones climáticas adversas.

## 🌐Enlaces

### [Video]([https://www.loom.com/share/11ab5f29c6824351a116a8de530a6c9e?sid=7f22661d-77fe-4439-aa52-69fc54293ffe](https://www.loom.com/share/7ca237c552db4023b19f09bd467f928d?sid=5c013072-8f4f-4852-b436-131d2d15b983))


