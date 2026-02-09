# Risk of bias (Risk of bias and evidence governance.md)

## Objetivo
Este documento describe el enfoque adoptado para la **evaluación de calidad y/o riesgo de sesgo** de las fuentes incluidas en esta revisión, y justifica las decisiones metodológicas tomadas dada la **naturaleza mixta** del corpus (literatura académica + informes institucionales + reportes de mercado + fuentes profesionales/comunitarias).

## Declaración principal (no se realizó evaluación formal)
No se realizó una **evaluación formal** de calidad metodológica ni una herramienta estandarizada de **riesgo de sesgo** (p. ej., RoB 2, ROBINS-I, CASP, MMAT, etc.). Esta decisión se tomó por las siguientes razones:

1. **Heterogeneidad de tipos de fuente**: el conjunto incluye artículos académicos, documentos institucionales/gubernamentales, informes comerciales/industria, y publicaciones profesionales/comunitarias, que no son comparables bajo un único instrumento de appraisal.
2. **Enfoque del estudio**: el objetivo de la revisión es principalmente **descriptivo y de síntesis cualitativa** (perfil profesional, competencias, tendencias, brechas y evidencia de impacto), no una estimación causal o un meta-análisis de efectos donde un RoB formal sea imprescindible.
3. **Limitaciones de la información disponible**: una parte relevante de las fuentes (p. ej., informes de mercado y entradas corporativas) no reporta metodología con el detalle suficiente para aplicar herramientas clásicas de evaluación de sesgo de forma consistente y reproducible.

## Estrategia alternativa aplicada (controles mínimos de calidad y trazabilidad)
Aunque no se aplicó una escala formal de calidad, se implementaron **controles mínimos** para mitigar problemas de trazabilidad y uso indebido de evidencia:

### 1) Verificabilidad por URL (trazabilidad)
Cada registro incluye el campo **`Verificabilidad_URL`** con categorías:
- **`Si`**: enlace accesible y verificable.
- **`Parcialmente`**: enlace potencialmente inestable o de naturaleza comunitaria (p. ej., foros), o con verificabilidad limitada.
- **`No`**: sin enlace verificable (si aplica).

**Criterio de uso:** cuando `Verificabilidad_URL` fue `Parcialmente`, la fuente se trató como evidencia de contexto o apoyo débil, evitando su uso para afirmaciones centrales.

### 2) Clasificación del rol en la revisión (control de peso de evidencia)
Se aplicó una codificación explícita mediante **`Rol_en_revision`**:
- **`SINTESIS_CUALITATIVA`**: fuentes usadas para construir resultados y síntesis narrativa.
- **`METODOLOGIA_NO_SINTETIZADA`**: fuentes usadas para justificar/reportar metodología (p. ej., PRISMA/PRISMA-S), sin entrar en resultados.
- **`CONTEXTO_NO_SINTETIZADO`**: fuentes usadas solo para contextualizar (p. ej., discusión profesional o comunitaria), y **no** para sostener conclusiones.

Esta clasificación se complementa con:
- **`Incluida_en_sintesis_cualitativa`** (Si/No)
- **`Incluida_en_sintesis_cuantitativa`** (Si/No)

### 3) Separación explícita de fuentes comunitarias/profesionales
Las fuentes etiquetadas como **comunitarias** (p. ej., Reddit, ciertas publicaciones en LinkedIn) se incluyeron, cuando procedía, **exclusivamente para contextualización**, evitando:
- derivar estimaciones numéricas,
- generalizar como evidencia representativa,
- sustentar afirmaciones centrales o conclusiones.

## Uso de herramientas de IA y control del riesgo asociado
La fase de **identificación/descubrimiento** de fuentes estuvo asistida por la herramienta **Perplexity Pro** (septiembre 2024–enero 2026) como apoyo para localizar literatura potencialmente relevante mediante consultas iterativas. Esta asistencia se limitó a la **recuperación de candidatos** y no se utilizó para generar datos, completar lagunas de evidencia ni inferir resultados no presentes en las fuentes.

Dado que el uso de un motor asistido por IA puede introducir sesgos de recuperación (p. ej., priorización de fuentes más accesibles o populares, variabilidad en resultados por fecha), se aplicaron controles de mitigación:
- **Trazabilidad/verificabilidad**: toda afirmación incluida en el manuscrito se rastrea a una fuente citada y accesible; se penalizaron o excluyeron fuentes con URL inestable/no permanente.
- **Transparencia metodológica**: se evitó usar como evidencia central materiales con metodología opaca (especialmente en literatura comercial).
- **Separación por rol**: las fuentes comunitarias/profesionales identificadas durante la búsqueda se conservaron solo para contexto y no para sostener afirmaciones centrales ni resultados cuantitativos.
- **Verificación manual**: se comprobó manualmente la correspondencia entre afirmaciones y contenido de las fuentes utilizadas.

Estas decisiones se describen con mayor detalle en el anexo de asistencia de IA (`notes_ai_assistance.md`).


## Implicaciones para la interpretación de resultados
Dado que no se realizó un appraisal formal:

1. **Las conclusiones se interpretan como síntesis narrativa** y no como inferencias causales.
2. Las cifras procedentes de **informes comerciales** se reportan como **indicadores de mercado** sujetos a variaciones metodológicas entre proveedores; se prioriza su uso comparativo y contextual, no como “mediciones oficiales”.
3. Se enfatiza la **triangulación**: cuando una afirmación es relevante, se procura apoyarla en más de un tipo de fuente (académica + institucional + industria) o se formula con cautela.

## Limitaciones
- La ausencia de evaluación formal puede incrementar el riesgo de incorporar sesgos propios de literatura gris (p. ej., sesgo comercial, falta de metodología reproducible, selectividad en reportes).
- Algunas fuentes relevantes pueden contener datos útiles pero no auditables en profundidad sin acceso a anexos, metodología interna o datos subyacentes.

## Justificación de adecuación al propósito
Para una revisión mixta orientada a describir **tendencias, roles, competencias y brechas** en un ecosistema profesional (PLN/empleabilidad), el enfoque adoptado prioriza:
- **transparencia** (qué se incluyó y con qué rol),
- **trazabilidad** (URLs verificables),
- **prudencia en el peso de evidencia** (exclusión explícita de fuentes comunitarias del núcleo de resultados),
lo que se considera proporcionado al objetivo del estudio y a las restricciones del tipo de literatura disponible.

## Recomendación para trabajos futuros
En extensiones futuras de esta revisión, se propone implementar un appraisal por capas:
- **Académicas**: herramienta tipo MMAT/CASP según diseño.
- **Literatura gris**: AACODS (Authority, Accuracy, Coverage, Objectivity, Date, Significance).
- **Corporativo/mercado**: checklist de transparencia mínima (metodología declarada, definición de mercado, fuentes de datos, supuestos, fecha, replicabilidad).

