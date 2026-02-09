# Estrategia de búsqueda (search_strategy.md)

## Objetivo
Identificar y recopilar literatura académica y profesional reciente relevante para una revisión sistematizada sobre:
1) adopción y crecimiento del PLN en contextos organizacionales;
2) perfil profesional del lingüista computacional/experto en PLN y señales de empleabilidad;
3) evidencia sobre calidad del dato (anotación, ruido de etiquetas) y evaluación de modelos;
4) tendencias operativas relevantes para la integración del PLN en entornos organizacionales.

## Periodo y alcance temporal
El período de búsqueda y recopilación se extendió de **septiembre de 2024 a enero de 2026**.

## Ventanas temporales aplicadas (según fuente/consulta)
La ventana temporal de resultados se aplicó de manera **diferenciada por fuente/consulta** (p. ej., 2019–2026 en arXiv/Google Scholar y 2023–2026 en varios informes de mercado), tal como se documenta en el PRISMA textual.

## Fuentes y bases consultadas (según PRISMA)
La identificación inicial se realizó mediante búsquedas iterativas y recuperación de registros en un conjunto heterogéneo de fuentes académicas, institucionales, comerciales y de industria. El total de registros identificados en esta fase fue n = 255 (antes de deduplicación), contabilizado a partir del registro maestro exportado. Dado que la estrategia de búsqueda se ejecutó en iteraciones (con solapamientos entre plataformas, recolecciones repetidas y registros coincidentes entre fuentes), los recuentos por fuente no se reportan como un desglose aditivo del total, sino como evidencia de cobertura de tipos de fuente y dominios.

Las fuentes consultadas incluyeron, de forma representativa:

- Repositorios y buscadores académicos: arXiv y Google Scholar, además de acceso a editoriales/plataformas científicas y repositorios académicos relevantes (p. ej., Nature/Scientific Reports, Frontiers, y repositorios de artículos/actas cuando aplicaba).

- Fuentes institucionales y organismos: publicaciones de OECD, recursos institucionales universitarios (p. ej., páginas de programas/carreras), y estadísticas o perfiles ocupacionales de organismos oficiales (p. ej., BLS).

- Informes comerciales de mercado (NLP/IA): firmas de inteligencia de mercado (p. ej., Straits Research, Precedence Research, Mordor Intelligence, Future Market Insights, Coherent Market Insights, Fortune Business Insights, Technavio).

- Industria y práctica profesional (evidencia aplicada): informes y contenidos técnicos de empresas o laboratorios (p. ej., IBM, Databricks, Google Research) y documentación/guías técnicas de proveedores del ecosistema de anotación y operación de modelos (p. ej., Deasy Labs, Label Studio, HitechDigital, CloudFactory, Labelforce AI, Milvus).

- Fuentes profesionales de empleo y perfiles: guías y descripciones de rol (p. ej., WGU, Edmates), portales de tendencias laborales o perfiles (p. ej., Zippia) y ofertas/puestos publicados (p. ej., Remocate, Sigma Group), tratadas como evidencia contextual según criterios de verificabilidad.

- Asimismo, se consultaron fuentes comunitarias (p. ej., Reddit y LinkedIn) exclusivamente como apoyo contextual para identificar vocabulario, debates y etiquetas ocupacionales; estas fuentes no se consideraron evidencia válida para resultados cuantitativos ni para conclusiones, y se trataron diferenciadamente en el cribado y la síntesis.

## Herramientas y procedimiento general
- Se utilizó Perplexity Pro como apoyo para localizar y agregar fuentes potencialmente relevantes, a partir de consultas iterativas y refinamiento de términos.
- La selección final y la redacción del manuscrito se realizaron con criterio conservador: se priorizaron afirmaciones apoyadas directamente por las fuentes citadas y accesibles (ver notes_ai_assistance.md).

## Tipos de fuentes consultadas
1) Literatura académica (p. ej., artículos y preprints).
2) Informes de mercado / análisis sectoriales con cifras explícitas (mercado, adopción, crecimiento).
3) Fuentes institucionales y profesionales sobre competencias, formación y empleabilidad (universidades, portales especializados, etc.).

## Estrategia booleana (según PRISMA)
Se emplearon consultas booleanas y combinaciones de términos. En el PRISMA se documentan las siguientes búsquedas y recuentos de resultados:

1) (linguistics OR "computational linguist*" OR "language science")
   AND (natural language processing OR NLP OR "language technolog*")
   AND (artificial intelligence OR AI OR "machine learning")
   - Registros encontrados: 89

2) ("computational linguist*" OR "linguistic* computing") AND enterprise
   - Registros encontrados: 34

3) (linguistic annotation OR "data annotation") AND NLP AND (performance OR quality OR accuracy)
   - Registros encontrados: 28

4) ("NLP market" OR "natural language processing market") AND (2024 OR 2025 OR 2026)
   - Registros encontrados: 52

5) ("AI skills gap" OR "talent shortage") AND (linguistic* OR language OR NLP)
   - Registros encontrados: 15

6) ("computational linguist*" OR "language scientist") AND (salary OR employment OR career OR market)
   - Registros encontrados: 29

## Criterios de inclusión y exclusión (resumen operativo)
Criterios de inclusión: fuentes que abordaran al menos uno de estos ejes:
- rol del especialista lingüístico/lingüista computacional en proyectos de PLN;
- competencias y tareas asociadas al perfil en contextos profesionales;
- calidad de datos lingüísticos y su impacto en evaluación/rendimiento;
- mercado laboral: empleabilidad, salarios, señales formativas;
- adopción organizacional/mercado de PLN y tendencias operativas.

## Criterios de exclusión documentados en PRISMA:
- duplicados;
- publicaciones fuera del período aplicado en la revisión (con exclusión de excepciones metodológicas);
- artículos de opinión/editorial sin datos cuantitativos;
- fuentes con datos no verificables o URL no permanente;
- metodología opaca o no transparente;
- falta de acreditación institucional;
- especulación sin base empírica.

## Registro y volumen de fuentes
- Se consultaron 76 fuentes primarias (registro maestro). 
- En el archivo con la matriz de extracción de datos (*data extraction matrix*) constan todas las entradas documentadas y con sus 17 variables correspondientes.

## Extracción de información
Para cada fuente incluida (cuando procedía) se extrajeron:
- metadatos (autor/organización, año, URL/título, tipo de fuente);
- datos cuantitativos (si aplica): valores, unidad, horizonte temporal, métrica;
- síntesis cualitativa: hallazgos relevantes para las dimensiones temáticas del manuscrito;
- notas de calidad/limitaciones (p. ej., transparencia metodológica, naturaleza comercial/divulgativa).

Nota: Las fuentes no académicas se incluyeron en síntesis cualitativa únicamente si presentaban autoría identificable, trazabilidad y contenido verificable; en caso contrario se restringieron a contexto.

## Evaluación de calidad (criterios adaptados)
Dada la heterogeneidad del corpus:
- Estudios empíricos: claridad metodológica, validez de conclusiones, adecuación de evidencia.
- Informes de mercado/adopción: reputación del emisor, trazabilidad de cifras, claridad metodológica (cuando disponible).
- Fuentes profesionales/institucionales: pertinencia para competencias/empleabilidad y consistencia con otras fuentes.

## Limitaciones
- El proceso de identificación inicial estuvo asistido por IA (ver notes_ai_assistance.md). Es posible que alguna fuente pertinente no haya sido recuperada; por ello, se priorizaron afirmaciones respaldadas por fuentes trazables y se realizó verificación manual de los resultados clave.
- Parte de las fuentes relevantes son comerciales o divulgativas; se trataron con cautela y se formularon inferencias de forma conservadora.

## Resultado del proceso (PRISMA)
- Registros identificados: 255
- Duplicados eliminados: 50
- Registros tras deduplicación: 205
- Excluidos en cribado por título/resumen: 103
- Evaluados a texto completo: 102
- Excluidos tras lectura a texto completo: 26
- Incluidos en síntesis final: 76 (n=65 como síntesis cualitativa; n=0 como síntesis cuantitativa; n=9 como fuentes contextuales comunitarias; y n=3 fuentes metodológicas no sintetizadas)

Las fuentes comunitarias se emplearon mayoritariamente como contexto; excepcionalmente, algunas se utilizaron para síntesis cualitativa cuando aportaron información verificable y pertinente.

(Para el detalle del flujo y las exclusiones con razones, ver prisma_flow.md y excluded_sources.csv).

## Nota de reportabilidad PRISMA-S (búsqueda asistida por Perplexity Pro)
Aunque esta revisión sigue la estructura PRISMA, la fase de identificación se apoyó en **Perplexity Pro** como motor de descubrimiento/agregación de resultados. Por ello, no se dispone de (ni es reproducible de forma equivalente) el conjunto completo de elementos que PRISMA-S suele requerir cuando la búsqueda se ejecuta directamente en bases concretas (p. ej., “query exacta tal cual” por base, campos específicos buscados —título/resumen/palabras clave—, y filtros nativos aplicados por plataforma).

En su lugar, para asegurar trazabilidad se reporta:
- el **periodo** de búsqueda (septiembre 2024–enero 2026),
- las **consultas booleanas** principales utilizadas y sus recuentos,
- el **tipo de fuentes** cubiertas (académicas, institucionales, comerciales/industria, profesionales/comunitarias),
- y los **criterios de inclusión/exclusión**, junto con el flujo PRISMA y la matriz de extracción.

Se asume como limitación que los resultados pueden variar por fecha y por el algoritmo de recuperación de la herramienta; para mitigarlo se priorizaron fuentes con **URL verificable**, se evitó sostener conclusiones en fuentes comunitarias y se verificó manualmente la correspondencia entre afirmaciones y fuentes citadas. Para detalles, ver `notes_ai_assistance.md`.
