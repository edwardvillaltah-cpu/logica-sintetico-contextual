# MOTOR COMPUTACIONAL LSC-CALC (PYTHON CORE)
## IMPLEMENTACIÓN DE TRAZABILIDAD Y VERIFICACIÓN DE NO COMPENSACIÓN CRÍTICA

**Autor:** Ronald Edward Hernández Villalta  
**ORCID:** [0009-0003-1235-157X](https://orcid.org/0009-0003-1235-157X)  
**DOI de la Obra:** [10.6084/m9.figshare.34007775](https://doi.org/10.6084/m9.figshare.34007775)  
**Registro de Propiedad Intelectual:** Presentación N.° 2026001383 (CNR, El Salvador)  
**Licencia:** Creative Commons Atribución-NoComercial 4.0 Internacional (CC BY-NC 4.0)

---

## 1. ARQUITECTURA DEL MOTOR COMPUTACIONAL
El motor computacional **LSC-CALC** traduce los axiomas de la Lógica Sintético-Contextual en rutinas ejecutables para automatizar la evaluación de premisas, garantizar la trazabilidad libre de opacidad algorítmica y aplicar de manera estricta el **Axioma de No Compensación Crítica ($VI_2 \le VI_1$)**.

---

## 2. CÓDIGO FUENTE COMPLETO (PYTHON)

```python
# ==============================================================================
# MOTOR COMPUTACIONAL LSC-CALC v1.6 - CORE ENGINE
# Autor: Ronald Edward Hernandez Villalta
# Licencia: CC BY-NC 4.0
# ==============================================================================

from dataclasses import dataclass, field
from typing import Dict, List, Optional
import datetime


@dataclass
class ContextTuplet:
    """Estructura de la tupla formal del objeto Case_3.0 en LSC."""
    context_id: str
    regime_k: str  # Nominal (K0), Critico (K1), Excepcion (K2)
    vi_1_primary: float  # Umbral basal primario
    vi_2_secondary: float  # Variable secundaria
    evidence_score: float  # Ponderacion probatoria
    defeaters_present: List[str] = field(default_factory=list)


class LSCContextEngine:
    """
    Motor de Inferencia y Evaluacion de No Compensacion Critica.
    Garantiza la trazabilidad auditable y bloquea la degradacion basal.
    """

    def __init__(self, vi_primary_threshold: float = 0.85):
        self.vi_1_threshold = vi_primary_threshold

    def validate_case(self, case: ContextTuplet) -> Dict[str, object]:
        """
        Evalua la tupla contra el Axioma Basal VI_2 <= VI_1
        y verifica la presencia de derrotores (defeaters) activos.
        """
        # Verificacion del Axioma Rector de No Compensacion
        non_compensation_pass = case.vi_2_secondary <= case.vi_1_primary
        primary_sustained = case.vi_1_primary >= self.vi_1_threshold

        # Determinacion del estado de inferencia
        if not primary_sustained or not non_compensation_pass:
            status = "BLOQUEADO_VIOLACION_BASAL"
            authorized = False
        elif case.defeaters_present:
            status = "INCOMPLETO_DERROTOR_ACTIVO"
            authorized = False
        else:
            status = "EVALUABLE_AUTORIZADO"
            authorized = True

        # Generacion de la cadena de trazabilidad auditable
        audit_trail = {
            "timestamp": datetime.datetime.utcnow().isoformat(),
            "context_id": case.context_id,
            "regime": case.regime_k,
            "metrics": {
                "vi_1_primary": case.vi_1_primary,
                "vi_2_secondary": case.vi_2_secondary,
                "vi_1_threshold": self.vi_1_threshold,
                "evidence_score": case.evidence_score
            },
            "defeaters": case.defeaters_present,
            "evaluation": {
                "axiom_non_compensation": non_compensation_pass,
                "primary_sustained": primary_sustained,
                "status": status,
                "action_authorized": authorized
            }
        }
        return audit_trail


# ==============================================================================
# EJECUCIÓN Y DEMOSTRACIÓN DE AUDITORÍA
# ==============================================================================
if __name__ == "__main__":
    engine = LSCContextEngine(vi_primary_threshold=0.80)

    # Caso 1: Intento de compensacion ilegitima (Debe ser BLOQUEADO)
    caso_prueba = ContextTuplet(
        context_id="EVAL_CASO_001",
        regime_k="K0_NOMINAL",
        vi_1_primary=0.65,     # Degradado por debajo del umbral 0.80
        vi_2_secondary=0.90,   # Intento de compensacion
        evidence_score=0.95,
        defeaters_present=[]
    )

    resultado = engine.validate_case(caso_prueba)

    print("=== REGISTRO DE TRAZABILIDAD AUDITABLE (LSC-CALC) ===")
    print(f"Caso Evaluado: {resultado['context_id']}")
    print(f"Estado de Inferencia: {resultado['evaluation']['status']}")
    print(f"Accion Autorizada: {resultado['evaluation']['action_authorized']}")
    print(f"Axioma VI_2 <= VI_1 Cumplido: {resultado['evaluation']['axiom_non_compensation']}")
