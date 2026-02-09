# Data Dictionary — extraction_matrix.csv

## 1) Descripción general
**Nombre del dataset:** `extraction_matrix.csv`  
**Propósito:** Matriz de extracción de una revisión (tipo PRISMA) sobre empleabilidad y perfil del lingüista computacional en empresas que adoptan/adaptan PLN.  
**Unidad de análisis:** una *fuente* (artículo académico, informe institucional, report de mercado, post profesional/comunitario, etc.).  
**Nivel de granularidad:** 1 fila = 1 fuente.  
**Formato observado:** TSV (valores separados por tabulador).  
**Valores faltantes:** no se representa con `NA`; la ausencia de dato suele expresarse como `No`, campo vacío o texto en `Notas_Adicionales`.

---

## 2) Diccionario de variables (columnas)

### 2.1 Identificación y metadatos bibliográficos

#### `ID_Fuente`
- **Tipo:** entero (ID)
- **Requerido:** sí
- **Descripción:** Identificador único y secuencial de la fuente en la matriz.
- **Reglas/validación:** debe ser único; idealmente entero positivo consecutivo.
- **Ejemplo:** `1`

#### `Titulo_Fuente`
- **Tipo:** texto
- **Requerido:** sí
- **Descripción:** Título completo de la fuente (tal y como se cita/identifica).
- **Reglas/validación:** conservar mayúsculas/minúsculas relevantes; permitir saltos de línea si el título es largo (recomendable normalizar a una línea en CSV).
- **Ejemplo:** `PRISMA Statement: Preferred Reporting Items for Systematic Reviews`

#### `Autor_Institucion`
- **Tipo:** texto
- **Requerido:** sí
- **Descripción:** Autor(es) o institución responsable de la fuente.
- **Notas:** mezcla autores personales (`Moher et al.`) e institucionales (`OECD`, `IBM`).
- **Ejemplo:** `Moher et al.`

#### `AÒo_Publicacion`
- **Tipo:** entero (año) / texto corto
- **Requerido:** sí
- **Descripción:** Año de publicación.
- **Observación de calidad:** el nombre de columna contiene un problema de codificación (`AÒo` en lugar de `Año` o `Ano`). Conviene normalizar.
- **Ejemplo:** `2024`

#### `Tipo_Fuente`
- **Tipo:** categórica (texto)
- **Requerido:** sí
- **Descripción:** Naturaleza/ámbito de la fuente.
- **Valores observados:**  
  - `Academica`  
  - `Comercial`  
  - `Institucional`  
  - `Institucional/Mixta`  
  - `Gubernamental`  
  - `Industria`  
  - `Profesional`  
  - `Comunitaria`  
  - `Tendencias`  
  - `Otra`
- **Uso recomendado:** distinguir evidencia académica vs *grey literature* vs fuentes comunitarias.
- **Ejemplo:** `Academica`

#### `Tema_Principal`
- **Tipo:** categórica (texto)
- **Requerido:** sí
- **Descripción:** Eje temático principal por el que se codifica la fuente.
- **Valores observados (no exhaustivos):**  
  - `Metodologia`  
  - `Mercado_NLP`  
  - `Empleo`  
  - `Competencias`  
  - `Brechas`  
  - `Impacto_Expertise`  
  - `Tendencias`  
  - Combinaciones con espacios: `Empleo Competencias`, `Mercado_NLP Brechas`, `Tendencias Competencias`, etc.
- **Reglas/validación:** si se admiten múltiples temas, definir separador formal (p. ej., `;`) para evitar ambigüedad.
- **Ejemplo:** `Mercado_NLP Empleo`

---

### 2.2 Variables de extracción de evidencias (contenido)

#### `Datos_Mercado`
- **Tipo:** mixto (texto / binario)
- **Requerido:** sí (puede ser `No`)
- **Descripción:** Evidencia o métricas sobre mercado de PLN (tamaño, CAGR, segmentación, adopción, etc.).
- **Valores observados:** `No`, `Sí`, o texto con cifras (`USD 30.68B 2024 ...`).
- **Ejemplo:** `USD 27.65 mil millones 2024`

#### `Datos_Empleo`
- **Tipo:** mixto (texto / binario)
- **Requerido:** sí
- **Descripción:** Evidencia sobre empleo (salarios, demanda, crecimiento, roles, proyecciones, empleadores).
- **Valores observados:** `No` o texto (p. ej., `Mediana USD 101000 ...`).
- **Ejemplo:** `Proyecciones empleo linguistas`

#### `Datos_Competencias`
- **Tipo:** mixto (texto / binario)
- **Requerido:** sí
- **Descripción:** Evidencia sobre competencias requeridas (técnicas, lingüísticas, MLOps/LLMOps, RAG, evaluación, etc.).
- **Ejemplo:** `Python ML estadistica NLP MLOps`

#### `Datos_Impacto_Expertise`
- **Tipo:** mixto (texto / binario)
- **Requerido:** sí
- **Descripción:** Evidencia del impacto de la pericia/experiencia lingüística (o experto humano) en resultados (calidad, performance, colaboración humano-IA, anotación, etc.).
- **Ejemplo:** `96.3% vs 88.6% mejora 7.7 puntos`

#### `Datos_Brechas`
- **Tipo:** mixto (texto / binario)
- **Requerido:** sí
- **Descripción:** Evidencia sobre brechas (skills gap, barreras de adopción, déficit de formación, data work, etc.).
- **Ejemplo:** `50% orgs brecha 33% barrera principal`

---

### 2.3 Trazabilidad y verificabilidad

#### `Verificabilidad_URL`
- **Tipo:** categórica (texto corto)
- **Requerido:** sí
- **Descripción:** Indicador de si la fuente es accesible/verificable mediante URL.
- **Valores observados:** `Si`, `No`, `Parcialmente`
- **Criterio implícito (según notas):**
  - `Si`: URL directa y accesible.
  - `Parcialmente`: fuente comunitaria o acceso no robusto (p. ej., Reddit), o URL con dudas.
  - `No`: sin URL o no verificable (no se observó en el extracto, pero existe en el esquema).
- **Ejemplo:** `Parcialmente`

#### `URL_Fuente`
- **Tipo:** URL (texto)
- **Requerido:** recomendado (si `Verificabilidad_URL` ≠ `No`)
- **Descripción:** Enlace a la fuente (paper, informe, post, PDF).
- **Reglas/validación:** URL completa; ideal evitar fragmentos `#:~:text=` si no aportan valor para trazabilidad (pueden romperse).
- **Ejemplo:** `https://www.nature.com/articles/s41598-024-82501-9`

#### `Notas_Adicionales`
- **Tipo:** texto
- **Requerido:** no
- **Descripción:** Comentarios cualitativos: rol de la fuente, cautelas (p. ej., comunitaria no usada para resultados), resumen del aporte.
- **Ejemplo:** `Fuente comunitaria ... usada solo para contextualización; no se emplea para resultados...`

---

### 2.4 Variables de rol en la revisión (PRISMA / síntesis)

#### `Rol_en_revision`
- **Tipo:** categórica (texto)
- **Requerido:** sí
- **Descripción:** Clasificación operacional del rol de la fuente en la revisión.
- **Valores observados:**
  - `SINTESIS_CUALITATIVA`
  - `METODOLOGIA_NO_SINTETIZADA`
  - `CONTEXTO_NO_SINTETIZADO`
- **Interpretación recomendada:**
  - `SINTESIS_CUALITATIVA`: fuente incluida en resultados/síntesis narrativa.
  - `METODOLOGIA_NO_SINTETIZADA`: fuente usada para justificar/reportar método (PRISMA, PRISMA-S), no para hallazgos.
  - `CONTEXTO_NO_SINTETIZADO`: fuente solo contextual, explícitamente excluida de conclusiones/resultados centrales.
- **Ejemplo:** `CONTEXTO_NO_SINTETIZADO`

#### `Incluida_en_sintesis_cualitativa`
- **Tipo:** binaria (texto corto)
- **Requerido:** sí
- **Descripción:** Marca de inclusión en síntesis cualitativa (síntesis narrativa/temática).
- **Valores observados:** `Si`, `No`
- **Reglas/validación:** debe ser coherente con `Rol_en_revision` (p. ej., si `Rol_en_revision= SINTESIS_CUALITATIVA`, entonces `Si`).
- **Ejemplo:** `Si`

#### `Incluida_en_sintesis_cuantitativa`
- **Tipo:** binaria (texto corto)
- **Requerido:** sí
- **Descripción:** Marca de inclusión en síntesis cuantitativa (meta-análisis u otro agregado cuantitativo).
- **Valores observados:** `Si`, `No` (en el extracto, predomina `No`).
- **Reglas/validación:** si es `Si`, entonces deberían existir datos estructurados (idealmente numéricos) en campos de evidencia.
- **Ejemplo:** `No`

---
