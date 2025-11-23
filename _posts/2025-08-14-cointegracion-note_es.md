---
title: "Cointegración y Estructura de Largo Plazo: Una Intepretación desde el Rango Reducido"
date: 2025-08-14
tags:
  - Series de Tiempo
  - Cointegracion
  - Johansen
lang: es
lang_toggle_url: /cointegration-note/
lang_toggle_label: Eng
---

La cointegración suele presentarse como una técnica para detectar relaciones estables entre variables no estacionarias. Esa descripción es correcta, pero demasiado estrecha para entender la arquitectura dinámica que gobierna los procesos macroeconómicos de largo plazo. En contextos donde las series exhiben tendencias marcadas, alta persistencia o quiebres estructurales, el hecho de que ciertas combinaciones lineales permanezcan estacionarias abre una pregunta más profunda: ¿qué restricciones estructurales permiten que algunas relaciones se mantengan ancladas mientras el resto del sistema deriva con el tiempo?

Este texto desarrolla una perspectiva más formal articulando tres ideas: (i) las limitaciones inherentes de los métodos uniecuacionales basados en regresiones en niveles, (ii) la propuesta de Johansen de interpretar la cointegración como una restricción de rango sobre la matriz de largo plazo de un VAR, y (iii) la conexión entre esa interpretación y el marco general de las autoregresiones de rango reducido. El objetivo es presentar un argumento riguroso pero sobrio que sitúe el análisis del largo plazo dentro de una estructura coherente, donde los procesos de ajuste no cancelan las tensiones del sistema, sino que las organizan.

## 1. Limitaciones del Enfoque de Engle y Granger

El procedimiento de Engle–Granger —una regresión en niveles entre variables I(1), seguida de una prueba de raíz unitaria sobre los residuos— fue un aporte fundamental y sigue siendo un buen diagnóstico preliminar.

Sin embargo, desde una óptica formal, enfrenta restricciones conocidas:

- **Unidimensionalidad del espacio cointegrado:** solo recupera una relación de largo plazo, incluso cuando la estructura económica genera más de una.  
- **Dependencia de la variable dependiente:** la relación estimada cambia al modificar qué variable queda a la izquierda, lo cual introduce una asimetría sin fundamento teórico.  
- **Fragilidad en muestras pequeñas:** la superconsistencia no corrige los sesgos inducidos por la dependencia serial ni reemplaza la necesidad de una representación multivariada explícita.

## 2. El Enfoque de Johansen: Rango y Estructura de Largo Plazo

El método de Johansen parte de un VAR en niveles y lo reparametriza como un modelo de corrección de errores (VECM). En esta forma, la matriz de largo plazo `Π` concentra toda la información relevante para detectar cointegración, y su rango `r` indica cuántas combinaciones estacionarias existen.

La factorización `Π = αβ'` distingue dos componentes centrales:

- `β` define el **espacio cointegrado**, es decir, las combinaciones que eliminan la tendencia común;  
- `α` recoge los **mecanismos de corrección del error**, indicando dirección e intensidad del ajuste cuando el sistema se desvía de sus relaciones de largo plazo.

Los tests de traza y de máximo valor propio —derivados del problema de autovalores generalizado— permiten determinar el rango de `Π` sin imponer a priori relaciones particulares. Así, la estructura de largo plazo y la dinámica de corto plazo se estiman simultáneamente en un único sistema coherente, donde las fuerzas de ajuste pueden leerse como respuestas sistemáticas frente a desequilibrios que no desaparecen, sino que se reconfiguran.

## 3. Cointegración como Autoregresión de Rango Reducido

En términos más generales, un VAR irrestricto posee matrices de coeficientes de rango completo. La cointegración emerge cuando la matriz de largo plazo tiene un rango estrictamente inferior.

El sistema resultante contiene dos componentes:

- un **subespacio estable**, asociado a `β`, donde ciertas combinaciones son estacionarias;  
- un **subespacio de tendencias comunes**, donde se concentran las fuerzas persistentes del sistema.

Esta representación se aparta de la idea clásica de un punto de “equilibrio” único y favorece una lectura geométrica: el sistema no converge a un valor, sino que evoluciona hacia un subespacio definido por restricciones estructurales. En ese subespacio, las relaciones de largo plazo pueden interpretarse como condiciones de reproducción del sistema, en tensión con tendencias que empujan fuera de esos márgenes y obligan a ajustes recurrentes.

## 4. Implicancias para el Análisis Macroeconómico Aplicado

Adoptar esta perspectiva más estructural tiene varias consecuencias analíticas:

- **Reconocimiento de la multidimensionalidad del largo plazo:** muchos sistemas macroeconómicos generan múltiples relaciones estructurales simultáneas, algunas complementarias y otras abiertamente tensionadas entre sí.  
- **Coherencia entre corto y largo plazo:** el VECM integra ambos horizontes temporales de forma unificada, evitando divisiones artificiales entre “desequilibrios de corto plazo” y “equilibrios de largo plazo” como si fuesen esferas separadas.  
- **Mayor precisión histórica:** distinguir entre estabilidad estructural y deriva tendencial permite lecturas más finas de procesos históricos de larga duración, identificando cuándo las relaciones de largo plazo funcionan como restricciones de reproducción del sistema incluso en presencia de crisis reiteradas.  
- **Atención al tamaño muestral:** las pruebas de Johansen tienden a sobre-rechazar en muestras pequeñas; los ajustes de pequeña muestra y los métodos bootstrap son complementos valiosos y, en ciertos casos, necesarios para que la inferencia sobre estas relaciones estructurales no se sostenga en meros artefactos estadísticos.

## 5. Conclusión

La cointegración no debe verse solo como un mecanismo para “descontar tendencias”, sino como una forma de representar la geometría estructural del largo plazo y las maneras en que ciertas combinaciones condensan restricciones y conflictos del proceso macroeconómico. La lectura de Johansen y el enfoque de rango reducido ofrecen un aparato formal capaz de mostrar cómo algunas combinaciones económicas permanecen ancladas mientras otras evolucionan de manera persistente.

Esta perspectiva es especialmente útil en investigación histórica y comparada, donde las interacciones entre acumulación, distribución y productividad exigen distinguir entre estabilidad estructural y cambio sostenido. Más que ofrecer respuestas cerradas, esta interpretación de los métodos de cointegración abre un espacio de análisis donde la teoría, la historia y la econometría tienen un terreno fértil para dialogar.
