# LÓGICA SINTÉTICO-CONTEXTUAL (LSC-FSC-CALC)
## TOMO II – AXIOMÁTICA FORMAL Y ESPECIFICACIÓN TÉCNICA LSC 3.0

**Autor:** Ronald Edward Hernández Villalta  
**ORCID:** [0009-0003-1235-157X](https://orcid.org/0009-0003-1235-157X)[cite: 5.2]  
**DOI de la Obra:** [10.6084/m9.figshare.34007775](https://doi.org/10.6084/m9.figshare.34007775)[cite: 5.2]  
**Registro de Propiedad Intelectual:** Presentación N.° 2026001383 (CNR, El Salvador)[cite: 5.2, 5.3]  
**Licencia:** Creative Commons Atribución-NoComercial 4.0 Internacional (CC BY-NC 4.0)[cite: 5.2]

---

## ÍNDICE GENERAL DEL TOMO II
1. **Especificación del Lenguaje Formal $LSC\text{-}CALC$**
   - Alfabeto, Operadores y Sintaxis Formal
2. **La Tupla Estructural LSC 3.0**
   - Definición Ampliada del Sistema
   - Estructura Mínima: $Case_{3.0}$
3. **Principio de Separación Categorial Estricta**
   - Distinción entre Verdad, Validez, Evidencia, Aplicabilidad e Integridad
4. **Semántica Contextual y Reglas de Inferencia**
   - Transiciones de Estado y Ponderación de Premisas

---

## 1. ESPECIFICACIÓN DEL LENGUAJE FORMAL $LSC\text{-}CALC$

El sistema LSC 3.0 formaliza el análisis contextual extendiendo la lógica de primer orden e introduciendo operadores de marco pragmático y sintáctico.

### 1.1 Alfabeto y Operadores Fundamentales
- **Variables Proposicionales:** $p, q, r, \dots$
- **Operador Contextual ($\mathcal{C}_k$):** Modula la validez de una proposición bajo el marco pragmático $k$.
- **Operador de Síntesis ($\odot$):** Representa la integración de premisas heterogéneas generando propiedades emergentes no reductibles a los componentes aislados.

---

## 2. LA TUPLA ESTRUCTURAL LSC 3.0

El cálculo deductivo de la Lógica Sintético-Contextual se define mediante la tupla formal ampliada:

$$\text{LSC-CALC} = \langle L, Syn, Sem, Inf, \mathcal{E}, C, R, K, D, V, \Theta \rangle$$

Donde:
- **$L$**: Lenguaje base y alfabeto formal.
- **$Syn / Sem$**: Sintaxis y semántica contextualizada.
- **$Inf$**: Reglas de inferencia deductivo-sintéticas.
- **$\mathcal{E}$**: Sistema de evaluación y ponderación de evidencia.
- **$C$**: Representación del marco y contexto pragmático.
- **$R / K / D$**: Matrices de evaluación de riesgo, selección de régimen y decisión.
- **$V$**: Evaluación de integridad y conservación de variables basales.
- **$\Theta$**: Parámetros de ajuste y umbrales normativos.

### 2.1 Estructura del Objeto Fundamental: $Case_{3.0}$
La unidad mínima de evaluación computable dentro del sistema se formaliza como:

$$Case_{3.0} = \langle ID, Argument, Context, Evidence, Relations, Bridges, Justifications, Dependencies, Risk, Criticality, Defeaters, Uncertainty, Synthesis \rangle$$

---

## 3. PRINCIPIO DE SEPARACIÓN CATEGORIAL ESTRICTA

Para prevenir ambigüedades y falacias de equivalencia en el análisis formal, la LSC postula la separación estricta entre dimensiones:

$$\text{VERDAD} \neq \text{VALIDEZ} \neq \text{EVIDENCIA} \neq \text{APLICABILIDAD} \neq \text{INTEGRIDAD} \neq \text{ACCIÓN}$$

- Un argumento puede poseer **validez** sintáctica interna pero carecer de **aplicabilidad** en un contexto determinado ($C_k$).
- Una proposición puede ser **verdadera** pero carecer de **evidencia** suficiente ($\mathcal{E}$) para justificar una sentencia decisoria.
- Ninguna decisión puede pretender validez si transgrede la **integridad de las condiciones basales** ($VI_2 \le VI_1$).

---

## 4. SEMÁNTICA CONTEXTUAL Y REGLAS DE INFERENCIA

1. **Inferencia Condicionada:** Un argumento $A$ deriva válidamente en $B$ si y solo si la transición se sostiene bajo la cobertura del contexto $C_k$.
2. **Evaluación de Derrotabilidad:** Las premisas están sujetas a derrotores contextuales ($Defeaters$) que pueden suspender la validez de la conclusión sin invalidar la coherencia interna de las premisas primarias.

---
*Obra registrada y protegida bajo los términos de la Licencia Creative Commons Atribución-NoComercial 4.0 Internacional (CC BY-NC 4.0).*[cite: 5.2]
