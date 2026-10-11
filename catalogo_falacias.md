# CATÁLOGO FORMAL DE FALACIAS (LSC-CALC 1.6)
## SISTEMA DE DETECCIÓN Y EVALUACIÓN DE DESVIACIONES PRAGMÁTICO-SINTÁCTICAS

**Autor:** Ronald Edward Hernández Villalta  
**ORCID:** [0009-0003-1235-157X](https://orcid.org/0009-0003-1235-157X)  
**DOI de la Obra:** [10.6084/m9.figshare.34007775](https://doi.org/10.6084/m9.figshare.34007775)  
**Registro de Propiedad Intelectual:** Presentación N.° 2026001383 (CNR, El Salvador)  
**Licencia:** Creative Commons Atribución-NoComercial 4.0 Internacional (CC BY-NC 4.0)

---

## 1. INTRODUCCIÓN Y MARCO FORMAL
En el sistema de la **Lógica Sintético-Contextual (LSC-FSC-CALC)**, una falacia no se define únicamente como una invalidez de deducción formal o una falsedad aislada de premisas, sino como una **ruptura o desviación pragmático-sintáctica en el marco de cobertura contextual ($C_k$)**.

El Catálogo LSC-CALC 1.6 categoriza los sesgos, distorsiones y violaciones argumentativas en función de la manipulación de evidencia ($\mathcal{E}$), la opacidad de premisas y la transgresión del **Axioma de No Compensación Crítica ($VI_2 \le VI_1$)**.

---

## 2. CATEGORIZACIÓN FORMAL DE FALACIAS

### 2.1 Falacias de Ruptura Basal (Violaciones de Integridad $V$)

* **F-01: Falacia de Compensación Ilegítima ($VI_2 > VI_1$)**
  * **Definición:** Intentar justificar el colapso, deterioro o sacrificio de una variable de sustentabilidad primaria ($VI_1$) mediante el incremento artificial en utilidad, votos, popularidad o beneficios en una variable secundaria ($VI_2$).
  * **Mecanismo de Detección:** $V(VI_1) < \text{Umbral} \wedge \Delta VI_2 > 0 \implies \text{BLOQUEO\_AUTOMÁTICO}$.
  * **Ejemplo Analítico:** Justificar la destrucción irreversible de una fuente hídrica local argumentando que incrementará los ingresos fiscales a corto plazo.

* **F-02: Falacia de Disociación Contextual (Descontextualización)**
  * **Definición:** Extraer una proposición de su marco de cobertura original ($C_1$) y evaluarla de manera rígida en un entorno distinto ($C_2$) omitiendo los operadores de transición de estado necesarios.
  * **Mecanismo de Detección:** Evaluador de transición de contexto nulo $T(C_1 \to C_2) = \emptyset$.
  * **Ejemplo Analítico:** Aplicar una norma de excepción de emergencia ($K_2$) como si fuera una regla estática de régimen nominal ordinario ($K_0$) sin verificar el cambio de restricciones.

---

### 2.2 Falacias de Evidencia e Incertidumbre ($\mathcal{E}$)

* **F-03: Falacia de Opacidad Algorítmica (Caja Negra)**
  * **Definición:** Presentar una conclusión o sentencia decisoria como normativamente vinculante apelando a un procesamiento automatizado opaco o subjetivo sin proporcionar la cadena de custodia lógica ni la trazabilidad en la tupla del objeto $Case_{3.0}$.
  * **Mecanismo de Detección:** Ausencia de la tupla de trazabilidad o dependencias lógicas explícitas en el motor.
  * **Ejemplo Analítico:** Validar una decisión punitiva o asignación crítica argumentando que "el modelo o la IA estadística lo determinó", sin mostrar las premisas de origen.

* **F-04: Falacia de Incommensurabilidad Equivalente**
  * **Definición:** Otorgar el mismo peso probatorio y la misma categoría analítica a la evidencia directa respaldada por datos verificables que a opiniones subjetivas, consensos políticos o creencias no contrastadas dentro de la matriz de decisión ($D$).
  * **Mecanismo de Detección:** $\mathcal{E}_{\text{opinión}} \equiv \mathcal{E}_{\text{empírica}}$ en la ponderación del sistema.
  * **Ejemplo Analítico:** Ponderar al 50% la opinión de un comité de popularidad frente a los datos técnicos de degradación de una variable basal.

---

### 2.3 Falacias de Derrotabilidad y Regímenes Normativos ($K$)

* **F-05: Falacia de Inmunización a Derrotores (*Defeater Immunity*)**
  * **Definición:** Ignorar, censurar o descartar sistemáticamente la introducción de derrotores socavadores (*undercutting defeaters*) o rebatidores que alteran o invalidan la transición inferencial dentro de un régimen crítico ($K_1$).
  * **Mecanismo de Detección:** $Defeater \in C_k \wedge \text{InferenceStatus} = \text{Unmodified}$.
  * **Ejemplo Analítico:** Sostener la validez inalterable de una premisa directiva a pesar de la aparición documentada de evidencia contextual que destruye el nexo causal.

* **F-06: Falacia de Falsa Emergencia (Artificialidad de Régimen $K_2$)**
  * **Definición:** Declarar de manera injustificada un estado de excepción o régimen de emergencia ($K_2$) con el único propósito de saltarse los controles del régimen nominal ($K_0$) y eludir el principio de no compensación.
  * **Mecanismo de Detección:** $R_{\text{real}} < \text{Umbral de Excepción} \wedge K_{\text{asignado}} = K_2$.
  * **Ejemplo Analítico:** Fabricar una crisis ficticia para suspender la auditoría ordinaria de las variables basales del sistema.

---

## 3. PROTOCOLO DE EVALUACIÓN EN LSC-CALC
Cualquier caso procesado a través del motor computacional evalúa los argumentos contra este catálogo estructurado. Ante la presencia de cualquiera de estas desviaciones, el sistema emite un estado de bloqueo o alerta de inconsistencia, resguardando la integridad del marco analítico.

---
*Obra registrada y protegida bajo los términos de la Licencia Creative Commons Atribución-NoComercial 4.0 Internacional (CC BY-NC 4.0).*


