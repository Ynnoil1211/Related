PRÁCTICA No. 2: ERRORES Y MEDICIONES

1. OBJETIVOS
El alumno identificará las principales causas de error en las mediciones experimentales y procederá a realizar mediciones correctamente, aplicando criterios estadísticos rigurosos para la cuantificación de incertidumbres y el descarte de datos anómalos.

2. MARCO TEÓRICO
2.1 Concepto de Medición e Instrumentos
La medición es el proceso de asignar un valor numérico, acompañado de su unidad, a una propiedad física mediante la comparación con un patrón de referencia [1, Ch. 1]. Un instrumento es un dispositivo que traduce una variable física (mensurando) en una lectura o señal interpretable [1, Sec. 2.1]. Todo proceso de medición perturba, en mayor o menor grado, el sistema medido; el instrumento actúa como una extensión de las facultades humanas, pero introduce errores inherentes al acto mismo de medir [2, pp. 108–110].
2.1.1 Exactitud, precisión, resolución y rango
Exactitud (accuracy): cercanía entre el valor indicado por el instrumento y el valor verdadero o de referencia. Se cuantifica como inexactitud o incertidumbre de medición: el rango dentro del cual se espera que se encuentre el valor verdadero [2, Sec. 3.1; 6, Sec. 2.2.1].
Precisión: grado de concordancia (dispersión) de lecturas repetidas alrededor de su valor medio, independientemente de la exactitud [6, Sec. 2.2.2]. Un instrumento puede ser preciso pero inexacto (sesgo), o exacto pero impreciso. La precisión se cuantifica mediante la desviación estándar de las lecturas.
Resolución: cambio mínimo en el mensurando que produce un cambio observable en la salida del instrumento [6, Sec. 2.2.8].
Rango o span: intervalo entre los valores mínimo y máximo que el instrumento puede medir [6, Sec. 2.2.4].
2.2 Clasificación de Errores
2.2.1 Errores sistemáticos
Son errores que permanecen constantes o varían de forma predecible, siempre en el mismo sentido (sesgo positivo o negativo) [2, Sec. 3.2]. No se reducen al promediar lecturas repetidas; se corrigen mediante calibración o corrección del procedimiento [3, Sec. 4.2]. Principales fuentes:
Error de calibración: desviación del instrumento respecto del patrón.
Error de paralaje: lectura incorrecta de escalas analógicas por observar la aguja desde un ángulo; se elimina con espejos de escala o instrumentos digitales [6, Sec. 6.2].
Error de carga: el instrumento extrae corriente del circuito y altera la variable. Se desarrolla en la sección 2.5.3.
Error ambiental: variación de las características del instrumento por temperatura, humedad, etc. (deriva de cero y de sensibilidad) [6, Sec. 2.2.9].
2.2.2 Errores aleatorios
Son perturbaciones impredecibles que producen errores positivos y negativos en proporción aproximadamente igual [2, Sec. 3.5; 6, Sec. 3.5]. Provienen del ruido térmico (ruido de Johnson), del ruido de cuantización en medidores digitales, de vibraciones y de variaciones del observador. Se modelan con la distribución normal y se reducen promediando:
σ_X̄ = σ / √n
donde σ es la desviación estándar de una observación y σ_X̄ es el error estándar de la media con n mediciones [2, pp. 108–115; 4]. Cuadruplicar el número de mediciones reduce el error a la mitad.
2.2.3 Errores espurios (gruesos)
Son datos anómalos que no pertenecen a la población de lecturas; se originan por fallas transitorias del instrumento, transitorios de alimentación o errores humanos de registro [6, Sec. 3.5]. A diferencia de los aleatorios, su magnitud es desproporcionadamente grande y deben eliminarse antes del análisis estadístico mediante los criterios de la sección 2.4.
2.3 Análisis Cuantitativo
2.3.1 Métricas de error
Para una medición X_med y un valor verdadero X_verdadero:
Error absoluto: ΔX = |X_med − X_verdadero|
Error relativo: ε = ΔX / X_verdadero
Error porcentual: ε% = (ΔX / X_verdadero) × 100%
2.3.2 Desviación estándar e incertidumbre
La desviación estándar muestral (n − 1 grados de libertad) es:
σ = √[ Σ(Xi − X̄)² / (n − 1) ]
El error probable es PE = 0.6745·σ, pues en la distribución normal ±0.6745σ contiene el 50% de la población; la probabilidad de que un error aleatorio exceda PE es 50% [4]. Los intervalos de confianza estándar son: 68.3% (±1σ), 95.5% (±2σ) y 99.7% (±3σ) [6, Sec. 3.5].
2.3.3 Propagación de errores
Para magnitudes independientes [6, Sec. 3.6]:
Suma/resta: ΔZ = √( ΔX² + ΔY² )
Multiplicación/división: ΔZ/Z = √( (ΔX/X)² + (ΔY/Y)² )
2.4 Criterios Rigurosos para Descartar Datos
2.4.1 Criterio del texto original (4 × error probable)
El texto original establece: descartar si |Xi − X̄| > 4·PE, donde PE = 0.6745·σ. Como 4·PE ≈ 2.7σ, el criterio es más permisivo que el de 4σ estricto [2, p. 112].
El criterio de 4σ (P(|z|>4) ≈ 1 en 15 800 bilateral; ≈ 1 en 31 600 unilateral) daría 4σ = 1.24 V; 0.99 V < 1.24 V → no se descartaría. Por ello, la formulación con error probable es la apropiada para muestras pequeñas.
2.4.2 Criterio de Chauvenet
Para muestras pequeñas (n = 5 a 30), se calcula la desviación normalizada:
d = |Xi − X̄| / σ
y se rechaza el dato si d supera el valor crítico para n (por ejemplo, 1.96 para n = 10; 2.24 para n = 20) [3, Sec. 4.4]. Equivale a rechazar si n·P < 0.5.
2.5 Especificaciones Técnicas de Instrumentos
2.5.1 Exactitud (Accuracy)
Formato típico de especificación: ±(% de lectura + % de rango) o ±(% de lectura + dígitos) [3, Sec. 2.2].
2.5.2 Resolución
Cambio mínimo detectable [6, Sec. 2.2.8]. Un multímetro de 3.5 dígitos en rango de 10 V indica hasta 9.999 V, con resolución de 0.001 V (1 mV).
2.5.3 Impedancia de entrada
Un voltímetro con impedancia finita Rm carga el circuito. El error de carga es [6, Sec. 3.2.1]:
E_m / E_0 = Rm / (R_Th + Rm)
Valores típicos: voltímetros 10–20 MΩ; osciloscopios 1 MΩ en paralelo con 20 pF [6, Sec. 6.3]. Regla práctica: Rm ≥ 100·R_Th para errores menores al 1%.
2.6 Metodología Correcta de Medición
2.6.1 Pre-medición
Verificar calibración y cero del instrumento.
Seleccionar el rango adecuado (operar en el tercio superior del rango para minimizar el error porcentual [6, Sec. 2.2.1]).
Verificar impedancia de entrada.
Estabilización térmica del equipo (5 a 10 minutos).
2.6.2 Durante la medición
Realizar mínimo 5 a 10 mediciones independientes para permitir el análisis estadístico.
Dejar tiempo entre lecturas para evitar correlación.
Documentar cualquier anomalía observada.
2.6.3 Post-medición
Calcular media y desviación estándar.
Identificar valores atípicos (criterios de la sección 2.4).
Calcular la incertidumbre final: δX = σ/√n.
Reportar: X = X̄ ± δX, indicando el nivel de confianza.
2.7 Normas Internacionales
La terminología estadística se rige por la norma ISO 3534-1:2006 [4]; la expresión de la incertidumbre de medición sigue la guía NIST SP 811 (equivalente al GUM) [5], que recomienda reportar incertidumbres expandidas con factor de cobertura k (k = 2 para aproximadamente 95% de confianza). En instrumentación digital, la norma IEEE 754 define la aritmética de punto flotante que afecta la propagación numérica de errores en el procesamiento de datos.
REFERENCIAS BIBLIOGRÁFICAS
[1] J. Fraden, Handbook of Modern Sensors: Physics, Designs, and Applications, 5th ed. New York, NY, USA: Springer, 2016, ch. 1–2.
[2] D. C. Baird, Experimentation: An Introduction to Measurement Theory and Experiment Design, 3rd ed. Upper Saddle River, NJ, USA: Prentice Hall, 1994, pp. 108–115.
[3] J. P. Bentley, Principles of Measurement Systems, 4th ed. Harlow, U.K.: Pearson/Prentice Hall, 2005.
[4] International Organization for Standardization, Statistics -- Vocabulary and Symbols -- Part 1: General Statistical Terms and Terms Used in Probability, ISO 3534-1:2006, Geneva, Switzerland, 2006.
[5] National Institute of Standards and Technology, Guide for the Use of the International System of Units (SI), NIST Special Publication 811, U.S. Department of Commerce, Gaithersburg, MD, USA, 2008.
[6] A. S. Morris, Measurement and Instrumentation Principles, 3rd ed. Oxford, U.K.: Butterworth-Heinemann, 2001.
