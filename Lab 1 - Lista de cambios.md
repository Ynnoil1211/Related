# Lab 1 — Lista de cambios a realizar

**Archivo:** `Lab 1 .docx.md` (informe "Static and Dynamic Analysis of a Mass-Spring System")

**Resumen de verificación:** toda la aritmética del informe es internamente consistente (regresiones, tablas, incertidumbres, porcentajes). Los problemas están en las **afirmaciones de coherencia** (consistencia con la teoría y entre métodos), en una **explicación físicamente incorrecta** (intercepto negativo) y en el **veredicto final contradictorio**.

---

## 1. Abstract — quitar la afirmación de "consistencia dentro de la incertidumbre" (no justificada)

**Ubicación:** Abstract, penúltima oración.

**Texto actual:**
> Both results are consistent with the theoretical value of 35 N/m and with each other within experimental uncertainty. The static method produced a lower relative uncertainty and a marginally better linear fit, while the dynamic method offered a more direct test of the system's oscillatory behavior.

**Reemplazo sugerido:**
> Both results are close to the theoretical value of 35 N/m (within ~8% and ~4% respectively), although the static result lies outside the uncertainty of the expected value. The two methods differ from each other by about 12%, a discrepancy that suggests a systematic effect not captured by the ideal model, most likely the spring's pre-tension. The static method produced a lower relative uncertainty and a marginally better linear fit, while the dynamic method offered a more direct test of the system's oscillatory behavior.

**Por qué:** con las incertidumbres declaradas (37.8 ± 0.7 y 33.7 ± 1.0):
- k_static vs. 35 N/m → diferencia de 2.8 N = **4σ** (no consistente)
- k_static vs. k_dynamic → diferencia de 4.1 N = **3.4σ** frente a la incertidumbre combinada (√(0.7² + 1.0²) = 1.2 N)

---

## 2. Discussion — tres cambios

### 2a. Corregir la atribución del intercepto negativo (físicamente incorrecta)

**Texto actual:**
> In the dynamic graph, the intercept (-0.095 s²) is likewise close to zero and slightly negative, which is physically consistent with the fact that a truly massless spring should give T² = 0 when m = 0; the small deviation from zero can be attributed to the spring's own mass, which was neglected in the ideal model but in reality contributes an effective mass to the oscillating system.

**Reemplazo sugerido:**
> In the dynamic graph, the intercept (-0.095 s²) is likewise close to zero and slightly negative, which is physically consistent with the fact that a truly massless spring should give T² = 0 when m = 0; however, the sign of this deviation is hard to explain physically: the spring's own mass would add a positive effective mass and therefore a *positive* intercept, so the negative sign points instead to a systematic timing bias, such as the reaction time when starting the stopwatch, which shortens the measured period most noticeably at low masses.

**Por qué:** la masa del resorte entra como T² = 4π²(m + m_eff)/k → intercepto **positivo**. Un intercepto negativo no puede explicarse por la inercia del resorte; sugiere un sesgo sistemático de cronometraje.

### 2b. Corregir la contradicción en el veredicto de fiabilidad

**Texto actual (dos oraciones que se contradicen):**
> However, the dynamic method is arguably more reliable as a measurement of the "true" oscillatory behavior of the system, because it is less sensitive to a possible pre-tension or nonlinearity in the spring near its unstretched length, and it directly tests the physical law that governs the system's actual motion. Considering both the accuracy (closeness to the theoretical 35 N/m) and the precision (size of the uncertainty), the static method is the more reliable of the two for this experiment; the dynamic method remains a valuable independent check, since its result agrees with the static result within the combined uncertainties.

**Reemplazo sugerido:**
> However, the dynamic method is more reliable as a measurement of the "true" oscillatory behavior of the system, because it is less sensitive to a possible pre-tension or nonlinearity in the spring near its unstretched length, and it directly tests the physical law that governs the system's actual motion. It is also the only result consistent with the theoretical value within its uncertainty (1.3σ vs. 4σ for the static method), and its 4% deviation from 35 N/m is smaller than the static method's 8%. The static method's larger deviation, combined with its positive intercept, is consistent with a slight pre-tension in the spring that the ideal model neglects. The two results nevertheless differ by about 12%, more than their combined uncertainties, which indicates a systematic discrepancy between the two methods that merits further investigation.

**Por qué:** la precisión favorece al método estático (2% vs. 3%), pero la exactitud favorece al dinámico (4% vs. 8% de desviación; 1.3σ vs. 4σ). Un resultado a 4σ de la teoría suele indicar error sistemático, por lo que declarar el estático "más fiable" no se sostiene. Además, la afirmación final de concordancia es falsa (3.4σ).

### 2c. Eliminar la afirmación de concordancia falsa

Incluida dentro del reemplazo 2b (la oración "...since its result agrees with the static result within the combined uncertainties" queda eliminada). No requiere edición adicional si se usa el reemplazo de 2b.

---

## 3. Conclusions — tres cambios

### 3a. Reemplazar la afirmación de concordancia

**Texto actual:**
> When compared against the theoretical reference value of 35 N/m, the static method deviated by about 8% and the dynamic method by about 4%, and the two results agree with one another within their combined uncertainties.

**Reemplazo sugerido:**
> When compared against the theoretical reference value of 35 N/m, the static method deviated by about 8% and the dynamic method by about 4%. Only the dynamic result is consistent with the reference value within its uncertainty, and the two methods differ from each other by about 12% — more than their combined uncertainties — suggesting a systematic effect, most likely pre-tension in the spring, that the ideal model does not account for.

### 3b. Corregir la atribución a la masa del resorte

**Texto actual:**
> The near-zero intercepts obtained in both linearized graphs support the theoretical assumption that the spring behaves ideally over the range studied, with only minor deviations attributable to pre-tension in the static case and to the spring's non-negligible mass in the dynamic case.

**Reemplazo sugerido:**
> The near-zero intercepts obtained in both linearized graphs support the theoretical assumption that the spring behaves ideally over the range studied, with minor deviations attributable to pre-tension in the static case and to a systematic timing bias in the dynamic case (the negative intercept cannot be explained by the spring's own mass, which would shift it in the opposite direction).

### 3c. Corregir el veredicto final

**Texto actual:**
> The static method proved to be the more reliable technique for determining the elastic constant in this experiment, while the dynamic method served as a valuable independent verification that captures the system's actual oscillatory behavior.

**Reemplazo sugerido (opción A — decantarse por el dinámico):**
> The dynamic method proved to be the more reliable technique for determining the elastic constant, since it is the only result consistent with the theoretical value within its uncertainty, while the static method — despite its higher precision — deviates from the expected value by 4σ and appears to be affected by the spring's pre-tension.

**Reemplazo alternativo (opción B — veredicto neutro):**
> Neither method can be declared unambiguously more reliable: the static method is more precise (2% vs. 3% relative uncertainty) but the dynamic method is more accurate (4% vs. 8% deviation from the theoretical value), and the 12% disagreement between them points to a systematic effect — most likely pre-tension — that should be studied further.

---

## 4. Appendix B — números de figura incorrectos

**Ubicación:** Appendix B.

**Texto actual:**
> ***Appendix B:** Linearized graphs (see Figures 1 and 2 in Section 3.2 above).*

**Corrección:** cambiar a **Figures 2 and 3**. La Sección 3.2 contiene la Figura 2 (estática) y la Figura 3 (dinámica); la Figura 1 es el montaje de la Sección 2.

---

## 5. Sección 2.3 (nota del procedimiento) — "randomly chosen" es inexacto

**Texto actual:**
> ...the actual experiment was conducted with eight randomly chosen masses ranging from 200 g to 1100 g, as instructed by the professor.

**Corrección:** reemplazar "eight randomly chosen masses" por **"eight selected masses"** (los valores 200–1100 g son sistemáticos, no aleatorios).

---

## 6. Verificar el renderizado de ecuaciones en el .docx

En la exportación en markdown las ecuaciones aparecen corruptas — la Ec. (2) se ve como `T = 2πmk` y la linealización como `T2= (42k)m` (se perdieron la raíz cuadrada y el símbolo π). Verificar que el documento real muestre:

- Ec. (2): **T = 2π√(m/k)**
- Sección 3.3, caso dinámico: **T² = (4π²/k)m**
- Appendix C.2: **T = 2π√(m/k)**, **T² = (4π²/k)m**, y el cálculo final **k_dynamic = 4(3.1416)²/1.173 = 39.478/1.173 ≈ 33.65 N/m**

Si el .docx los renderiza bien, no hay que cambiar nada. También verificar que los placeholders `[image1]`–`[image4]` correspondan a las figuras reales (montaje, dos gráficas, hoja manuscrita).

---

## 7. Appendix C.1, paso 4 — simplificación menor (opcional)

**Texto actual:**
> Since y = m_static · x is equivalent to W = k · x, it follows directly that: k_static = Slope = 37.78 N/m.

**Corrección (opcional):** añadir una nota de que el ajuste incluyó un intercepto pequeño:

> Since y = m_static·x + b is equivalent to W = k·x, with the small intercept b = 0.64 N attributed to pre-tension, it follows directly that k_static = slope = 37.78 N/m.

---

## Tabla resumen

| # | Ubicación | Tipo | Acción |
|---|---|---|---|
| 1 | Abstract | Afirmación no justificada | Reformular la consistencia (ver §1) |
| 2a | Discussion | Físicamente incorrecto | Reformular la explicación del intercepto (ver §2a) |
| 2b | Discussion | Veredicto contradictorio | Reformular la conclusión de fiabilidad (ver §2b) |
| 3a | Conclusions | Afirmación no justificada | Reformular la concordancia (ver §3a) |
| 3b | Conclusions | Físicamente incorrecto | Corregir la atribución a la masa del resorte (ver §3b) |
| 3c | Conclusions | Veredicto no justificado | Corregir el veredicto final (ver §3c) |
| 4 | Appendix B | Referencia incorrecta | "Figures 2 and 3" |
| 5 | §2.3 nota | Redacción inexacta | "eight selected masses" |
| 6 | Todo el documento | Verificación de renderizado | Confirmar √ y π en las ecuaciones |
| 7 | Appendix C.1 | Simplificación excesiva | Nota opcional sobre el intercepto |

---

## Justificación numérica (para el profesor, si pregunta)

| Comparación | Diferencia | Incertidumbre combinada | σ |
|---|---|---|---|
| k_static (37.8 ± 0.7) vs. 35 N/m | 2.8 N | 0.7 N | **4.0σ** |
| k_dynamic (33.7 ± 1.0) vs. 35 N/m | 1.3 N | 1.0 N | 1.3σ |
| k_static vs. k_dynamic | 4.1 N | √(0.7² + 1.0²) = 1.2 N | **3.4σ** |

- Diferencia relativa entre métodos: 4.1/33.7 ≈ **12%** (supera incluso la meta del 10% del propio informe)
- Intercepto dinámico negativo: la masa del resorte daría T² = 4π²(m + m_eff)/k → intercepto **positivo**
- Lo verificado y correcto: pendientes (37.78 y 1.173), interceptos (0.64 y −0.095), k = 4π²/slope = 33.66, incertidumbres (0.74 y 1.00), desviaciones (8% y 4%), incertidumbres relativas (2% y 3%), R² (0.998 vs. 0.995), sumas del apéndice (Σx = 1.343 m, ΣW = 55.860 N)
