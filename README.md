# Repositorio de respaldo — Revisión sistematizada (RSL) y manuscrito
**Título del estudio/manuscrito:** *El lingüista computacional como perfil estratégico para el PLN empresarial*  
**Versión del manuscrito:** Blanca Hernández Pardo_Comunicación2 (febrero 2026) - Pendiente de publicar en editorial tras congreso CIEI 2026 (https://ciei.es/)
**Autor/a:** Dr.ª Blanca Hernández Pardo
**Contacto:** bhpardo@comillas.edu 
**Repositorio:** [URL del repo cuando lo publiques]  
**Fecha de última actualización:** 2026-02-09

## 1. Descripción
Este repositorio contiene los materiales que respaldan una **revisión sistematizada de literatura** (orientada a síntesis cualitativa) sobre:
1) adopción y crecimiento del PLN en entornos organizacionales;  
2) perfil profesional del lingüista computacional y señales de empleabilidad;  
3) calidad del dato (anotación, ruido de etiquetas) y evaluación;  
4) tendencias operativas para despliegues empresariales (p. ej., RAG, LLMOps, explicabilidad).

La identificación inicial de fuentes estuvo asistida por **Perplexity Pro**; se documentan las implicaciones de trazabilidad y las medidas de mitigación en los anexos (ver `notes_ai_assistance.md` y `search_strategy.md`).

## 2. Contenidos del repositorio
- `search_strategy.md` — Estrategia de búsqueda (términos, fuentes consultadas, ventanas temporales, criterios).
- `prisma_flow.md` — Flujo PRISMA en formato textual (recuentos por fase).
- `excluded_sources.csv` — Registros excluidos, fase y motivo (incluye agregado de duplicados).
- `extraction_matrix.csv` / `extraction_matrix.xlsx` — Matriz de extracción (1 fila = 1 fuente).
- `data_dictionary.md` — Diccionario de variables de la matriz de extracción.
- `included_sources.bib` — Bibliografía de las fuentes incluidas.
- `risk of bias and evidence governance.md` — Enfoque de calidad/riesgo de sesgo y gobernanza de evidencia (corpus mixto).
- `notes_ai_assistance.md` — Declaración de uso de IA y verificación/trazabilidad.

## 3. Resumen metodológico (PRISMA)
Según el flujo PRISMA:
- Registros identificados: n = 255  
- Duplicados eliminados: n = 50  
- Registros tras deduplicación: n = 205  
- Excluidos en cribado (título/resumen): n = 103  
- Evaluados a texto completo: n = 102  
- Excluidos a texto completo: n = 26  
- Incluidos en el corpus final: n = 76  
(Ver detalle en `prisma_flow.md`.)

## 4. Cómo reutilizar / replicar
- Para ver **qué se incluyó y por qué**: `extraction_matrix.*` + `included_sources.bib`.
- Para ver **qué se excluyó y por qué**: `excluded_sources.csv`.
- Para ver **cómo se buscó** (y limitaciones PRISMA-S por herramienta): `search_strategy.md`.
- Para ver **cómo se gestionó calidad/riesgo** en un corpus mixto: `risk of bias and evidence governance.md`.
- Para ver **transparencia sobre IA**: `notes_ai_assistance.md`.

## 5. Cómo citar este repositorio

> Hernández Pardo, B. (2026). *Repositorio de respaldo de la RSL “El lingüista computacional como perfil estratégico para el PLN empresarial”* (versión 1.0) [Conjunto de datos y materiales]. Repositorio. [URL]

## 6. Licencia
Ver `LICENSE`.

## 7. Nota sobre limitaciones (PRISMA-S)
La búsqueda inicial se realizó con apoyo de una herramienta de agregación asistida por IA (Perplexity Pro), por lo que no se dispone de queries nativas reproducibles por base al nivel de detalle típico de PRISMA-S. Se reportan el periodo, consultas booleanas principales, tipos de fuente y criterios de inclusión/exclusión, junto con el flujo PRISMA y la matriz de extracción (ver `search_strategy.md` y `notes_ai_assistance.md`).
