# CATÁLOGO FORMAL DE FALACIAS (LSC-CALC 1.6)
## SISTEMA DE DETECCIÓN Y EVALUACIÓN DE DESVIACIONES PRAGMÁTICO-SINTÁCTICAS

**Autor:** Ronald Edward Hernández Villalta  
**ORCID:** [0009-0003-1235-157X](https://orcid.org/0009-0003-1235-157X)  
**DOI de la Obra:** [10.6084/m9.figshare.34007775](https://doi.org/10.6084/m9.figshare.34007775)  
**Registro de Propiedad Intelectual:** Presentación N.° 2026001383 (CNR, El Salvador)  
**Licencia:** Creative Commons Atribución-NoComercial 4.0 Internacional (CC BY-NC 4.0)

---

## 1. INTRODUCCIÓN Y MARCO FORMAL
En el sistema de la **Lógica Sintético-Contextual (LSC-FSC-CALC)**, una falacia no se define únicamente como una invalidez deducción-validez formal o una falsedad de premisas, sino como una **ruptura o desviación pragmático-sintáctica en el marco de cobertura contextual ($\mathcal{C}_k$)**.

El Catálogo LSC-CALC 1.6 categoriza los sesgos y violaciones en la argumentación en función de la manipulación de evidencia ($\mathcal{E}$), la opacidad de premisas y la violación del **Axioma de No Compensación Crítica ($VI_2 \le VI_1$)**.

---

## 2. CATEGORIZACIÓN FORMAL DE FALACIAS

### 2.1 Falacias de Ruptura Basal (Violaciones de Integridad $V$)
* **F-01: Falacia de Compensación Ilegítima ($VI_2 > VI_1$)**
  * **Definición:** Intentar justificar el colapso o deterioro de una variable de sustentabilidad primaria ($VI_1$) mediante el incremento en utilidad, votos o beneficios en una variable secundaria ($VI_2$).
  * **Mecanismo de Detección:** $V(VI_1) < \text{Umbral} \wedge \Delta VI_2 > 0 \implies \text{BLOQUEO\_AUTOMÁTICO}$.
  * **Ejemplo Analítico:** Justificar la contaminación irreversible de una fuente de agua potable local a cambio de un incremento temporal en los ingresos fiscales del municipio.

* **F-02: Falacia de Disociación Contextual (Descontextualización)**
  * **Definición:** Extraer una proposición de su marco de cobertura original $\mathcal{C}_1$ y evaluarla en un marco $\mathcal{C}_2$ sin aplicar la transformación de transiciones de estado requerida.
  * **Mecanismo de Detección:** Evaluador de transición de contexto nulo $T(\mathcal{C}_1 \to \mathcal{C}_2) = \emptyset$.

### 2.2 Falacias de Evidencia e Incertidumbre ($\mathcal{E}$)
* **F-03: Falacia de Opacidad Algorítmica (Caja Negra)**
  * **Definición:** Presentar una conclusión como normativamente vinculante apelando a un procesamiento opaco sin proporcionar la cadena de custodia lógica ni la trazabilidad de inferencia.
  * **Mecanismo de Detección:** Ausencia de la tupla de trazabilidad en $Case_{3.0}$.

* **F-04: Falacia de Incommensurabilidad Equivalente**
  * **Definición:** Asignar el mismo peso probatorio o la misma categoría analítica a la evidencia directa respaldada por datos que a opiniones o consensos sin respaldo empírico.
  * **Mecanismo de Detección:** $\mathcal{E}_{\text{opinión}} \equiv \mathcal{E}_{\text{empírica}}$ dentro de la matriz de decisión $D$.

### 2.3 Falacias de Derrotabilidad y Regímenes ($K$)
* **F-05: Falacia de Inmunización a Derrotores (*Defeater Immunity*)**
  * **Definición:** Negar o ignorar sistemáticamente la introducción de derrotores socavadores (*undercutting defeaters*) que invalidan la transición inferencial en un régimen crítico $K_1$.
  * **Mecanismo de Detección:** $Defeater \in \mathcal{C}_k \wedge \text{InferenceStatus} = \text{Unmodified}$.

---

## 3. PROTOCOLO DE EVALUACIÓN EN LSC-CALC
Cualquier caso analizado a través del motor computacional procesa el argumento contra el Catálogo LSC-CALC 1.6. Si se detecta cualquiera de los patrones anteriores, la sentencia de salida clasifica automáticamente la inferencia bajo el estado **`BLOQUEADO`** o **`DESVIACIÓN_PARACONSISTENTE`**, impidiendo la autorización de la acción.

---
*Obra registrada y protegida bajo los términos de la Licencia Creative Commons Atribución-NoComercial 4.0 Internacional (CC BY-NC 4.0).*
