# Prompts Gemini Deep Research para La Chiva del Pasado

## Cuando usarlos

- Usa estos tres prompts para cada tema nuevo que el usuario te de para La Chiva del Pasado, sin excepcion.

- Adapta cada prompt al tema nuevo y conserva su estructura, sus preguntas y sus reglas de honestidad.

- Corre la investigacion propia en paralelo y cruza sus resultados con los informes de Gemini antes de escribir el guion.

- Lee la skill de produccion de La Chiva del Pasado antes de convertir los informes en guion.

## Como adaptar cada prompt

- Reemplaza el titulo del video, el numero de items, la lista inicial de items y la ventana de epoca por los del tema nuevo.

- Reemplaza los momentos buscados en el prompt de anecdotas por los momentos propios de cada item nuevo.

- Conserva intactos los lugares donde escuchar, las tareas numeradas, el formato de entrega y las reglas de honestidad.

- Conserva la variable principal del prompt de investigacion: la fuerza del recuerdo vivido, no la historia empresarial.

- Mantiene el idioma en espanol y la exigencia de enlaces en todas las afirmaciones importantes.

## Prompt 1: Investigacion

```
Investiga a profundidad, con fuentes verificables y enlaces, cuales son [TEMA EN PLURAL] MAS NOSTALGICOS PARA LOS COLOMBIANOS que vivieron entre los anos [VENTANA] (audiencia actual de 35 a 65 anos, dentro y fuera de Colombia). El objetivo es un video de YouTube de nostalgia colombiana titulado "[TITULO DEL VIDEO]", en formato de cuenta regresiva de [N] items y unos [DURACION] minutos.

La variable principal NO es la historia empresarial: es la FUERZA DEL RECUERDO VIVIDO. Un item es "muy nostalgico" si cumple la mayoria de estas: (1) la gente lo reconoce al instante sin que se lo expliquen; (2) aparece repetidamente en listas, articulos, videos o publicaciones colombianas de nostalgia; (3) tiene ganchos emocionales concretos (sonido, material, empaque, ritual de uso en familia); (4) su ausencia todavia se comenta hoy ("se acuerdan de...?"), o su regreso genera reaccion; (5) era nacional, no solo de una region.

TAREAS:
1. Evalua esta lista inicial de [N] y di, con evidencia, si cada una merece estar entre las [N] MAS nostalgicas o si hay alguna debil: [LISTA INICIAL].
2. Busca OMISIONES: items que las fuentes colombianas de nostalgia repitan mucho y no esten en la lista. Si una omision es mas nostalgica que alguna de la lista, propon el cambio y justificalo.
3. Para cada item final: que era, epoca de auge en Colombia, presencia nacional o regional (marca la regionalidad con claridad), y QUE PASO EXACTAMENTE (cierre, fin de comercializacion, desplazamiento, con anos y fuente). Si sigue existiendo de otra forma, dilo: no aceptes "desaparecio" sin comprobarlo.
4. Senales de demanda: si existen videos de YouTube u otros contenidos sobre ese tema, registra los titulos y las vistas aproximadas como evidencia de interes real.
5. Entrega la lista FINAL recomendada de [N] en orden de cuenta regresiva: la parada 1 debe ser la de mayor carga nostalgica nacional, y la parada [N] (la primera que se muestra) debe ser de reconocimiento inmediato para enganchar en el primer minuto. Justifica el orden.
6. Reglas de honestidad: no inventes fechas, nombres, esloganes ni datos; lo que no puedas confirmar con una fuente, marcalo "sin confirmar". Todas las afirmaciones importantes deben llevar su enlace.

Responde en espanol, con una tabla resumen (item, epoca, que paso, nivel de nostalgia: imprescindible / fuerte / debil, evidencia principal) y las secciones de cambios propuestos y orden final.
```

## Prompt 2: Audiencia

```
Investiga a profundidad QUE COMENTA Y QUE QUIERE LA AUDIENCIA COLOMBIANA en los espacios publicos de internet sobre [TEMA]. La audiencia son colombianos que vivieron los anos [VENTANA] (hoy de 35 a 65 anos), dentro y fuera del pais. El objetivo es un canal de YouTube de nostalgia colombiana ("La Chiva del Pasado") que lanzara un video titulado "[TITULO DEL VIDEO]", y queremos que la seleccion y el enfoque salgan de lo que la GENTE realmente recuerda y pide, no solo de lo que publican los medios.

DONDE ESCUCHAR (solo contenido publico y accesible; si una plataforma no te deja ver los comentarios, dilo expresamente y trabaja con lo que este indexado o sea visible):
- Comentarios de YouTube en videos sobre [TEMA] y nostalgia colombiana.
- Reddit, especialmente r/Colombia y hilos de nostalgia ("se acuerdan de...?", "que extranan?").
- TikTok e Instagram: publicaciones y comentarios publicos de cuentas y videos de nostalgia colombiana.
- Facebook: grupos y paginas publicas de nostalgia colombiana ("fotos antiguas", "Colombia de antes", grupos de ciudades).
- Foros y secciones de comentarios de articulos de prensa sobre el tema.

TAREAS:
1. Lo que la gente menciona por su cuenta: haz la lista de los items que los PROPIOS USUARIOS nombran mas en comentarios cuando hablan de lo que extranan (no los del titulo del video: los que la gente agrega en los comentarios). Para cada uno: frecuencia aproximada, la emocion dominante y 2 a 3 citas textuales breves con su enlace.
2. Lo que piden y no existe: detecta los deseos repetidos ("deberian hacer un video de...", "nadie habla de...", "que paso con...?", "yo extrano..."). Lista los huecos de contenido que la audiencia ya esta pidiendo.
3. Como lo recuerdan: los rituales, frases y escenas que mas se repiten. Esto servira para escribir el guion desde la vivencia.
4. Lo que les molesta de los videos actuales: errores que los comentaristas corrigen ("eso no era asi", "eso no era colombiano", "todavia existe"), quejas de datos falsos o de tono. Esto es oro: es lo que la audiencia NO perdona.
5. Pon a prueba esta lista de candidatas: [LISTA INICIAL]. Para cada una di: la menciona la audiencia por su cuenta en comentarios, o solo aparece en listas de medios? Esa diferencia es la conclusion mas importante del informe.
6. Recomendacion final: los [N] items que la AUDIENCIA elegiria, en orden de cuenta regresiva (la 1 = la mas recordada por la gente), separando con claridad "lo que dicen los medios" de "lo que dice la gente" cuando no coincidan.

REGLAS DE HONESTIDAD: no inventes comentarios ni cifras de frecuencia; cada cita textual debe ser real y llevar su enlace; si una fuente es un video o hilo concreto, citalo con titulo y enlace; lo que no puedas verificar, marcalo "sin confirmar". Responde en espanol, con la tabla de items mas mencionados por la audiencia al inicio.
```

## Prompt 3: Anecdotas

```
Busca en los espacios publicos de internet SOLO ANECDOTAS Y EXPERIENCIAS PERSONALES que los colombianos cuentan sobre estos [N] items. Nada de analisis, nada de historia empresarial, nada de opiniones sueltas: quiero HISTORIAS que la gente vivio, contadas por ellos mismos, porque serviran para escribir los guiones de un canal de nostalgia ("La Chiva del Pasado") narrados desde la vivencia.

LOS [N] ITEMS (con el momento que buscamos de cada uno):
[LISTA NUMERADA CON UN MOMENTO CONCRETO POR ITEM]

DONDE BUSCAR: comentarios de Reddit (r/Colombia: hilos de "cual recuerdan con mas nostalgia?", "productos descontinuados que extranan", "que extranan?"), publicaciones y comentarios publicos de Facebook (paginas y grupos de nostalgia colombiana y de fotos antiguas), comentarios de YouTube en videos de nostalgia colombiana, y comentarios publicos de TikTok e Instagram si son accesibles. Si una plataforma no te deja ver comentarios, dilo y sigue con las demas.

QUE CUENTA COMO ANECDOTA (esto es lo unico que quiero):
- Esta contada en primera persona por alguien que la vivio.
- Tiene una escena concreta: un momento, un lugar, una persona (la mama, el amigo del colegio, la abuela), un gesto o un detalle sensorial (un olor, un sonido, un sabor, una textura, una frase que alguien decia).
- Emociona: es graciosa, tierna, triste o picaresca. Lo anecdotico y nostalgico primero.
NO quiero: datos de empresas, fechas, correcciones historicas, quejas, listas sin historia, ni comentarios que solo digan "yo lo recuerdo" sin contar nada.

FORMATO DE ENTREGA: un banco de anecdotas organizado por item (en el orden de arriba), con 3 a 5 anecdotas por item si existen:
Para cada anecdota:
- Cita textual entre comillas, tal como la escribio la persona (conserva su espanol coloquial, sus errores y su puntuacion; no la corrijas ni la adornes).
- Fuente: plataforma y enlace.
- La escena que revive (una sola linea tuya): que momento de la vida de antes captura.
Al final, una seccion "Anecdotas huerfanas": historias excelentes que aparezcan sobre OTROS items que no estan en la lista (serviran para videos futuros), con el mismo formato.

REGLAS DE HONESTIDAD (innegociables): no inventes anecdotas ni completes las que esten a medias; no fusiones historias de dos personas en una; si algo es tu parafrasis y no cita literal, etiquetalo "parafrasis", nunca lo presentes como textual. Si de un item encuentras pocas anecdotas o ninguna, dilo tal cual ("sin anecdotas aprovechables") en vez de rellenar. Responde en espanol.
```

## Reglas que nunca cambian

- Adapta el tema y conserva la estructura.

- Exige fuentes con enlaces y marca "sin confirmar" lo no verificado.

- Separa lo que dicen los medios de lo que dice la gente.

- Entrega los informes en espanol y guardalos junto al tema en la carpeta del video.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.
