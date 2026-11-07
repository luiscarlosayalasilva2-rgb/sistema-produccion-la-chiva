# KIT DE RÉPLICA TOTAL — Sistema de producción de «La Chiva del Pasado»

**Qué es este documento:** un solo archivo autocontenido con TODO el sistema de producción del canal de YouTube «La Chiva del Pasado» tal como se entrega hoy (2026-11-05): edición, investigación, voces, miniaturas, descripciones y publicación. Está pensado para pegarse como contexto inicial en un chat nuevo de Muse y replicar el trabajo EXACTAMENTE, sin que falte nada operativo.

**Cómo usarlo:** léelo completo antes de producir nada. Cuando una regla tenga un número, una ruta, un texto exacto o una excepción, va tal cual en este documento: no la resumas, no la "mejores", no la interpretes. Si dos fuentes se contradicen, manda la indicada en la sección «Conflictos ya resueltos» (abajo). Si algo no está aquí, no se improvisa en producción: se propone, se aprueba y se incorpora.

**Fuera de alcance (mención única):** la búsqueda de empleo de Luis Carlos y el proyecto «Papás Primerizos» son otros sistemas y NO están en este documento.

**Fuentes de las que se compiló (todas leídas completas):** `~/MEMORY.md`; skill `~/workspace/custom-skills/la_chiva_del_pasado_production/SKILL.md`; libro de marca v1.5 `~/workspace/your_files/libro-marca-nostalgia-colombia/`; skill `~/workspace/custom-skills/gemini_deep_research_prompts/SKILL.md`; `~/workspace/nostalgia_colombia/muestras_voz_luis_carlos.md`; `~/workspace/nostalgia_colombia/prompt_maestro_miniaturas_colombianas.md`; repo `~/workspace/nostalgia_colombia/documental-expediente/docs/` (REGLAS_DURAS, NOVEDADES, ESTILO_DOCUMENTAL_EXPEDIENTE, PROCESO_COMPLETO, PROMPT_PARA_OTRA_IA, CLAUDE, README) + `src/pausas.py` y `src/voz.ps1`; `~/workspace/nostalgia_colombia/prompt_busqueda_comentarios_nostalgicos.md`; `~/workspace/nostalgia_colombia/informe_temas_virales_colombia.md`; `~/workspace/nostalgia_colombia/video_musica/descripcion_youtube.md`; conector `~/workspace/custom-connectors/custom.youtube-data-api/CONNECTOR.md` + `bin/youtube_channel.py` y `bin/youtube_comments.py`; estándar de edición `~/workspace/segundo-cerebro-taller-del-creador/outputs/2026-10-22-sistema-edicion-la-chiva-v1.md`; `~/workspace/nostalgia_colombia/feedback_canal_propio.md`; `~/workspace/nostalgia_colombia/video_tragedias/descripcion_youtube_borrador.md`.

## Conflictos ya resueltos (manda lo nuevo, no lo viejo)

1. **Duración:** el libro de marca fija el formato insignia en 25–35 min y el narrativo en 8–15 min. **Orden de Luis Carlos del 2026-11-02 (vigente): los videos nuevos duran 17–20 min.** Esa orden manda. NO es retroactiva: no se regenera nada ya hecho (Marcas, Bebidas v5, Platos v2, Novelas v1, Viajes v4).
2. **Demos / puerta piloto:** el repo y el skill piden un demo de 1 minuto o una parada piloto para aprobación antes del video completo. **Desde el 2026-10-27 Luis ya no quiere demos: se entrega directamente el video completo, verificado.** La puerta que sigue vigente es la del guion: parar en el guion y esperar su aprobación antes de voz o producción.
3. **Música de fondo:** el libro de marca contempla música instrumental discreta de fondo. **En la práctica del canal los videos son SOLO VOZ, sin música ni efectos de sonido** (salvo efectos sintetizados del repo). Esa es la regla operativa.
4. **Créditos:** el repo original decía "sin créditos" en pantalla. La práctica vigente: **sin créditos ni marcas de agua EN PANTALLA; los créditos de material con licencia libre VAN en la descripción y en las notas del EDL** (precedente: Música). Las fuentes se guardan internamente en `fuentes.tsv`.
5. **Descripciones:** la plantilla A2 del libro es la base teórica; **el formato a replicar es el de las descripciones entregadas** (Música, §10): apertura en escena, invitación a comentar, invitación a la lista de reproducción, lista 12→1, capítulos reales, créditos.

---

## 1. Quién es el usuario y qué es el canal

### El usuario

- **Luis Carlos Ayala**, Cali, Colombia (barrio Alfonso López). Contador Público titulado (Universidad del Valle, tarjeta profesional Junta Central de Contadores). ~4,5 años de experiencia como Auxiliar Contable/Administrativo en pymes. Empleo actual: Hacienda Lisboa (desde marzo de 2025).
- Trabaja en mensajes cortos y decisivos en español, con errores de tipeo a interpretar con caridad («minaitura» = miniatura, «gmeini» = Gemini, «pai» = API, «ase» = haz, «traigamos» = traigamos, «cula» = cuál, «peoximo» = próximo, «enotces» = entonces, «infor» = info, «ocmetarios» = comentarios, «tneer» = tener, «volvmaos» = volvamos, «MENSOS» = menos, «bine» = bien).
- Tono que premia: **ejecutor profesional, directo, breve, con estados verificables** (archivos, cifras, duraciones, marcas de tiempo). Delega flujos de trabajo completos de una vez y corrige en seco en el mismo turno cuando la voz, el orden o una regla se desvían de lo que quiso decir.
- Cuando ordena cambiar una sola cosa, se toca solo esa cosa. Cuando dice «dale», es luz verde para el paso siguiente. Los candidatos se mantienen visiblemente separados de los oficiales aprobados; trabajar junto a un candidato («sigamos con esa») no es aprobación explícita.
- **Nada se publica sin su palabra explícita.** (Hecho: él mismo publicó los 12 videos del canal, a diario, entre el 25 de octubre y el 5 de noviembre de 2026, pese a los fallos declarados de verificación en varios.)

### El canal

- **Nombre: «La Chiva del Pasado».** Respaldo oficial: «La Colombia Que Fue». Descriptor obligatorio, siempre junto al nombre: **«Nostalgia colombiana · Hechos reales»**.
- **Canal de YouTube:** `@LaChivadelPasado`, ID `UCHdDXyM8cVi-SxWcFWh4mdA`, creado el 2025-03-08, país CO. **Estado verificado por API el 2026-11-05: 12 videos publicados (25 oct–5 nov 2026), 631 suscriptores, 159.435 vistas totales.**
- **Logotipo oficial de perfil:** el SUYO original, aportado por él el 2026-10-15 («me gusta la mía original»): circular, chiva fotorrealista con «COLOMBIA» sobre el parabrisas, pueblo andino con iglesia y bandera, sombrero vueltiao, lettering tipo brocha («La Chiva» en blanco, «del Pasado» en amarillo, pincelada tricolor bajo el texto). Archivo: `~/workspace/user/media_library/image/80/80248e00aa3634ec3f1c1cf81deac816f9ecb1bc3a98730800d3feaadc21f257.jpg` (1254 × 1254 px). Se usa tal cual como foto de perfil; no se redibuja, no se recolorea, no se le añade texto, no se sustituye por alternativas generadas. Nota: a 40 px (tamaño del avatar en comentarios) no se lee; se sube tal cual de todos modos. Recomendación documentada para más adelante: versión simplificada solo con el frente de la chiva y «La Chiva» en dos líneas, sin paisaje (no reemplaza al oficial sin registrarse como nueva versión del libro).
- **Banner oficial:** 2560 × 1440 px en `~/workspace/nostalgia_colombia/banner/`, zona segura central 1546 × 423 px. Detrás del panel central lleva dichos y agüeros en letra manuscrita semitransparente como capa decorativa (se ven en TV y PC; en móvil quedan fuera de la zona segura y no hacen falta: ningún dicho o agüero del banner es información esencial).
- **Canal de referencia (suministrado por él el 2026-10-15): «Cuando México Fabricaba de Todo»** (`@CuandoMexicoFabricabadeTodo`, ID `UCtWtk6_Ph2EoHamCiI00lSg`). Al 2026-11-04: 51 videos, 5.890 suscriptores; TODOS de cosas; NINGUNO de música, famosos, electrodomésticos, viajes ni novelas; su video más visto: productos de los 80 que fracasaron (690.714 vistas). **Se copia el FORMATO, nunca el contenido** (ni textos, ni guiones, ni miniaturas, ni el orden de ítems).
- **Mentor:** Samu Hernandez («El Taller del Creador»). Veredicto 2026-11-01: La Chiva ya entró al algoritmo (8 videos publicados, 10.000 impresiones). **Órdenes de Samu: publicar TODOS los días sin huecos; ~17 min (menciona 22 para los siguientes); 10 o 12 ítems; CTR bueno 8–10 %; contenido para verse en TV.** Un video puede tardar 20–21 días en despegar; el viral empuja el catálogo. **Lista de reproducción (Samu, audio 2026-11-02): al final de cada video, invitar a seguir en La Chiva con la lista; todos los videos en la misma lista para que un viral retroalimente al resto.**
- **Segundo cerebro:** `~/workspace/segundo-cerebro-taller-del-creador/` — 40 lecciones de Skool transcritas en local (consulta: `wiki/00` → página → `raw/` solo si hace falta). Regla: todo material que él envíe por chat entra a `raw/` y se destila sin que lo pida. Su Notion NO está conectado; no afirmar que su lista de Notion está verificada.
- **Advertencia del curso (El Taller del Creador):** prohíbe construir canales SOBRE famosos (imagen y peor voz clonada = robo de identidad; «van a desaparecer»). Matiz registrado: lo nuestro es UN video en un canal de nostalgia, sin voces clonadas ni frases inventadas, solo hechos públicos verificados y tono respetuoso; riesgo residual registrado.

### Enfoque, audiencia y época

- **Principio rector (libro v1.4): NOSTALGIA DE LA VIDA DE ANTES de los colombianos, en sentido amplio.** Cada video debe evocar un **recuerdo VIVIDO** por los colombianos de esa época: en familia (la casa de los abuelos, la cocina de la abuela, los domingos), pero también en el barrio y la cuadra, en el colegio y el recreo, en la calle, en el pueblo, en el paseo y en la fiesta. La prueba obligatoria antes de aprobar cualquier tema: ¿evoca este tema un recuerdo vivido por los colombianos de esa época —en familia, en el barrio, en el colegio, en la calle o en el pueblo—? Si la respuesta es no, el tema no entra. El filtro solo descarta lo que no evoca ningún recuerdo vivido: lo industrial, lo abstracto y el dato frío. **Que un tema ocurra fuera de la casa familiar NO es motivo para descartarlo.**
- **La familia es el CENTRO DE GRAVEDAD EMOCIONAL y el TONO del canal, no un filtro literal que excluya temas** (corrección suya, «no así tan literal»). La narración vuelve siempre que puede a la escena vivida y a la voz de la casa, pero un tema de barrio, de colegio, de calle o de pueblo vale por sí mismo, sin necesidad de «justificarse» como familiar.
- **Territorios oficiales (v1.4, con sus palabras):** dulces de antes; modas; juguetes; paseos (el paseo de olla, el paseo al río, viajar en chiva y en bus); festividades; la Navidad (aguinaldos, novenas, regalos); los regalos y las celebraciones; las tradiciones; los bailes; las costumbres; los medios de transporte de antes; los juegos de barrio y de la calle; el colegio (el recreo, la tienda del colegio, los útiles); las novelas colombianas de antes (las telenovelas que reunían a la familia y al barrio frente al televisor); las películas colombianas de antes; y lo familiar: los dichos y agüeros que decían los abuelos, la casa de los abuelos, las comidas de antes, las marcas y productos de la vida cotidiana. Además: barrios, ciudades y lugares que cambiaron o desaparecieron; televisión, radio, prensa y vida pública de época, siempre desde un hecho concreto; empresas, tiendas, transporte y oficios que transformaron la vida cotidiana; escuela, juegos, costumbres y vida doméstica documentables; deporte, música y celebraciones cuando hay un hecho histórico detrás, no solo una efeméride. **Fuera de territorio:** política partidista actual, farándula sin hecho histórico, y cualquier tema que no pueda verificarse.
- **Audiencia principal (libro v1.5, una sola y unificada):** colombianos que vivieron la Colombia de los 80 a los 2000 (hoy, en su mayoría, de 35 a 65 años o más), en Colombia o en el exterior. Llegan también, sin ser el objetivo, los hijos que heredaron las historias y los jóvenes curiosos que entran por los Shorts; no se produce para ellos a costa de la audiencia principal. **Rango de época: años 70 a 2000 inclusive.**
- **Lo que la audiencia no tolera:** un error de fecha, de nombre o de lugar en algo que vivió (un solo error así cuesta más suscriptores que diez videos correctos ganan); sensacionalismo con su propia historia; que le inventen un recuerdo (presentar como hecho algo que solo circuló como rumor).
- **Promesa principal (textual):** «Cada vídeo te devuelve un hecho real de la Colombia que fue, con su fecha, su lugar y la fuente que lo comprueba. Si no lo podemos demostrar, te lo decimos.» Se cumple con: hecho central identificable en el título y en los primeros 30 segundos; fecha y lugar en pantalla antes del minuto 2, con ficha de archivo; al menos dos fuentes independientes para el hecho central, citadas en la descripción; un momento de contraste ayer / hoy; cierre con estado actual (qué queda, qué desapareció, qué sigue en disputa o sin confirmar); un recuerdo VIVIDO evocado en la narración.
- **Diferencial frente a la competencia:** no solo recordar productos, reconstruir hechos. Hechos verificados con fuentes citadas en pantalla y en la descripción, fechas exactas o rangos declarados, contexto histórico. Separación visible entre hecho, testimonio y leyenda urbana. Archivo antes que opinión.
- **Mural de ideas (2026-11-02): 11 familias como mapa de rotación (no repetir familia seguida):** Costumbres, Dichos, Cuentos, Alimentos, Juegos, Novelas, Películas, Música, Moda, Televisión y Hogar. Mapa actual: Juguetes→Juegos, Dulces y Platos→Alimentos, Navidad→Costumbres, Comerciales→Televisión, Novelas→Novelas, Electrodomésticos→Hogar, Famosos abarca Música/Televisión/redes. Sin tocar al 2026-11-02: Dichos, Cuentos, Películas, Moda (Música ya producida).

---

## 2. Reglas duras (todas, numeradas, con fecha y origen cuando conste)

1. **Anti-invención (permanente).** Nunca añadir, inferir ni completar un dato ausente de su CV o de una fuente verificada sin su confirmación explícita; lo no confirmado queda «sin confirmar». Letras de jingles y años en disputa se verifican en fuentes fiables antes de locutar, nunca de memoria.
2. **Regla de fuentes (orden de Luis Carlos, 2026-11-03).** La PRIMERA fuente es todo lo ya aprendido de él (su voz, sus reglas, sus criterios y el segundo cerebro de El Taller del Creador); también se puede ver la competencia, pero SIEMPRE prima lo aprendido de él. En conflicto, manda lo suyo, no lo del competidor.
3. **Regla de duración (orden 2026-11-02, vigente DESDE HOY, NO retroactiva).** Videos nuevos: **17–20 min.** No se regenera lo ya hecho: Marcas, Bebidas v5 (13:36), Platos v2 (15:39), Novelas v1 (10:48), Viajes v4 (14:14). Meta de guion: 3.570–4.200 palabras a 210 ppm, o ~3.100–3.800 al ritmo real de Cruz (~182–190 ppm). Para garantizar 17–20 en todo el rango: guion de ~3.417–3.600 palabras.
4. **Regla Colombia siempre (2026-10-24).** TODAS las imágenes y videos/clips deben ser de Colombia y clavar justo con lo narrado en cada parada y frase (no sustitutos extranjeros ni genéricos); sin material colombiano exacto: foto colombiana que clave justo, ficha sola o hueco, nunca video extranjero. MEZCLA: videos solo donde haya uno adecuado que clave justo, menos videos que imágenes.
5. **Regla de contexto (corrección de Luis Carlos, 2026-10-25, sobre el demo v6).** Un clip/foto de ambiente solo vale si corresponde a LA ESCENA que la voz describe, no a una palabra suelta. Sin imagen contextual exacta, se sostiene el plano anterior o se reporta hueco, nunca un video que cambie el sentido. Vale para todo el video.
6. **Regla de autoanálisis y arreglo (orden de Luis Carlos, 2026-10-25, para v9 y siguientes).** Después de corregir, califícate con las reglas del repo (REGLAS_DURAS, CATÁLOGO, AUTENTICIDAD, NOVEDADES, verificar.py, revisar_fotos.py); SI NO CUMPLE, ARREGLA ESO en ciclo hasta APROBADO o hasta demostrar con búsqueda seria que ese material no existe; solo entonces se entrega con la falla declarada, su causa y lo intentado, sin inventar nada para pasar.
7. **Regla de extensión / descargas (orden de Luis Carlos, 2026-10-25).** Si no es necesario descargar en su PC, NO se descarga en su PC; material para video y archivos para mostrar en el chat se bajan directo en la VM/workspace, y a su carpeta Descargas solo cuando él lo pida o sea realmente necesario.
8. **Audio continuo (regla fijada 2026-10-22 como estándar del canal).** La narración debe quedar CONTINUA: cortar TODOS los espacios/silencios del audio (entre frases, bloques y paradas); nada de huecos muertos. Refinada el 2026-10-27: solo los silencios de más de 0,8 s quedan en 0,5 s; las pausas normales entre frases no se tocan.
9. **Regla permanente de investigación (orden 2026-10-25).** Para CADA tema de La Chiva del Pasado, usar SIEMPRE los mismos 3 prompts de Gemini Deep Research adaptados al tema (investigación, audiencia, anécdotas), con las reglas de honestidad intactas. La investigación propia corre en paralelo y se cruza con los informes, nunca los reemplaza.
10. **Nada se publica sin su palabra explícita.** Ni en YouTube, ni en Drive, ni en remote-storage.
11. **Subida a remote-storage DECLINADA por él el 2026-11-03.** No reintentar sin que lo pida.
12. **Drive (cuenta conectada y verificada 2026-10-24: triviatk4@gmail.com, 5 TB).** Regla general: cerebro de trabajo, video de Marcas y su miniatura oficial NO están en Drive; solo se sube si él lo pide. Excepciones autorizadas: Viajes v3 y Famosos v3.
13. **Credencial Google (observado 2026-11-04 22:33).** La contraseña guardada de luisayaka87@gmail.com parecía DESACTUALIZADA («Tu contraseña se ha cambiado hace 25 horas»); nunca pedirle la contraseña en chat; el arreglo es que él complete el acceso en el navegador en vivo o la actualice por flujo seguro. El 2026-11-04 22:36 él completó el login en vivo («ya») y la voz de Música se generó sin problema.
14. **Parar en el guion.** Parar en el guion y esperar aprobación antes de voz/producción. Sin aprobación del guion no se genera nada.
15. **Modelos (orden permanente 2026-11-01).** Usar SIEMPRE los mejores modelos disponibles. Puente: gpt-oss-120b (OVH por defecto; Groq como alternativa) y openrouter/free en OpenRouter; en local, qwen3.5:4b (único práctico en esta VM; qwen3:8b descargado pero no corre por RAM).
16. **Voz de narración.** Luis Carlos quiere acento colombiano de Cali.
17. **«Desapareció» que no desapareció.** La audiencia no lo perdona: Only sigue existiendo; algunos dulces todavía se venden; un Tía en Chapinero (calle 59 con 13) existía hace ~5 años. Verificar que algo desapareció de verdad antes de afirmarlo.
18. **Matiz de clase (Navidad, feedback de la audiencia).** «No todos tuvimos la oportunidad de ir al centro a comprar el estren»: los futuros guiones de costumbres deben nombrar que no todas las familias vivían igual la fecha.
19. **Famosos reales (2026-11-03).** Fotos reales de cada famoso, no sustitutos, no genéricos, no IA como real. Jamás un vivo en miniatura como fallecido (Marlon Moreno está VIVO y NO entra). En la parte que le toca a cada famoso, él debe salir prácticamente siempre (regla 2026-11-03 23:40).
20. **Regla de la lista de reproducción (Samu, 2026-11-02).** Al final de cada video, invitar a seguir en La Chiva con la lista; todos los videos en la misma lista para que un viral retroalimente al resto.
21. **Corrección de voz (2026-10-21, para todos los guiones).** Luis Carlos rechazó un guion por «informar» la nostalgia en vez de contarla: exige voz de CONTADOR DE HISTORIAS HUMANO (escenas desde adentro, primera persona, emoción por delante, datos escondidos en el recuerdo). Reforzada el 2026-10-31 (rechazó texto por sonar «muy IA») y el 2026-11-05 13:19 sobre Tragedias («MAS HUMANO Y MENOS REPETITIVO Y IA»).
22. **Títulos: nunca años literales.** Matiz confirmado 2026-11-04: para canciones NO usar «Ya Nadie las Recuerda» (falso: la gente sí las recuerda, solo ya no suenan).
23. **Material de foros/redes.** Por defecto con todos los derechos reservados: solo sirve para localizar el original o pedir permiso, nunca entra sin licencia libre verificada o permiso. Una foto pixelada mejorada con IA no se presenta como foto original de archivo.
24. **Exige confirmación antes de agregar cualquier dato no presente en su CV original** (regla estricta anti-invención, también para textos de empleo; aquí rige igual para datos del canal no verificados).
25. **Densidad visual: más imágenes y más videos que lo habitual (orden de Luis Carlos, 2026-11-06, video de Dichos).** El video lleva MÁS videos y MÁS imágenes de lo habitual, cuadrando cada plano con lo que va diciendo la voz. Metas: **≥250 fotos distintas, ≥45 clips, cortes cada ~4–5 s (≈230–270 cortes en 18 min)**. Referencia Dichos (2026-11-07): 408 fotos distintas + 33 clips (los clips quedaron al límite del mínimo de verificar.py: 34 para 18:38, 33 para 18:12). Esta regla actualiza la MEZCLA de la regla 4: más videos que antes, pero las fotos siguen siendo mayoría. Si no hay clips exactos suficientes, se recortan segmentos adicionales distintos de documentales largos ya conseguidos (Tragedias hizo lo mismo); Pixabay por navegador en vivo si hace falta.
26. **Cada imagen y cada video tiene que ser exactamente de lo que se narra (2026-11-06).** No basta con que sea colombiano ni con que clave con una palabra suelta: la foto o el clip tiene que ser exactamente la cosa, la persona o la escena que la voz está contando en ese segundo (el contexto manda sobre la palabra suelta, regla 5). Sin material exacto: se sostiene el plano anterior o se declara hueco; jamás relleno extranjero ni genérico para subir la densidad.
27. **Texto en pantalla con animación de escribir: tiene que salir el título COMPLETO (observación de Luis Carlos, 2026-11-07, para los videos después de Dichos).** En Tragedias el texto a máquina se cortaba rápido y no se llegaba a leer el título entero. Desde el video siguiente a Dichos: toda nota a máquina muestra el texto completo, con duración suficiente para leerlo entero; verificarlo en la revisión de fotogramas antes de entregar.
28. **Imágenes reales vía Google en el navegador en vivo (observación de Luis Carlos, 2026-11-07, para los videos después de Dichos).** Buscar las imágenes reales en Google directamente con el navegador en vivo (como con Gemini), cuando se hable de personas y de todo. La búsqueda sirve para LOCALIZAR la foto real; la foto solo entra con licencia libre verificada o permiso (la regla 23 sigue intacta: material de foros/redes, por defecto con todos los derechos reservados).
29. **TEXTOS QUE SE PISAN — PROHIBIDO EN NINGÚN VIDEO (orden de Luis Carlos, 2026-11-07, video de Dichos).** Ninguna capa de texto puede pisarse con otra: ni ficha con palabra gigante, ni ficha con nota, ni número con palabra, ni ninguna combinación, ni siquiera una fracción de segundo. La v1 de Dichos salió APROBADA con 8 cruces (la palabra gigante ABUELOS encima de la ficha del título «12 dichos que nos decían los abuelos») porque `verificar.py` NO lo medía — el README decía «el script lo avisa» y era falso. Desde 2026-11-07 `verificar.py` lo mide y el video NO se aprueba si hay aunque sea un cruce; la corrección es mover la capa para que empiece cuando termina la anterior. Vale para TODOS los videos, sin excepción.

---

## 3. Libro de marca condensado (v1.5, 15 de octubre de 2026)

Documento rector: `~/workspace/your_files/libro-marca-nostalgia-colombia/Libro de Marca - La Chiva del Pasado.docx`. Toda decisión de guion, imagen, miniatura, título, narración y publicación se contrasta con este libro. Si algo no está aquí, no se improvisa en producción: se propone, se aprueba y se incorpora como nueva versión. **Antes de producir:** leer las secciones 1, 4, 13 y 16. **Durante la producción:** aplicar las secciones 7 a 12 tal como están escritas (no cambiar colores, tipografías ni estructura de miniatura por episodio). **Antes de publicar:** pasar el checklist de la sección 18; si un ítem falla, el video no se publica, se corrige. **Cuando algo deba cambiar:** anotarlo en el control de versiones al final y subir la versión (1.1, 1.2…); nunca editar una regla solo dentro de un video.

### Nombre y verificación (sección 1)

- Nombre principal: «La Chiva del Pasado» (idea original del creador, confirmada el 2026-10-15 al presentar su logotipo). Respaldo oficial: «La Colombia Que Fue» (nombre propuesto en la v1.0). Alternativas en orden: 1) La Colombia Que Fue, 2) Archivo Vivo Colombia, 3) Colombia Inolvidable (más emocional; solo si se ajusta también el descriptor). La variante «La Chiva del Pasado TV» sirve como handle (@LaChivaDelPasadoTV) antes que como cambio de nombre. Regla: las alternativas no se usan como nombres paralelos; si se activa una, reemplaza al nombre en todo el sistema (canal, banner, miniaturas, intro, descripción y libro) en una nueva versión.
- Verificación 2026-10-15: «Sin colisión exacta detectada el 15/10/2026 para 'La Chiva del Pasado' — disponibilidad del handle @LaChivaDelPasado NO garantizada». Prohibido escribir «nombre disponible» en cualquier documento, descripción o comunicación hasta completar la comprobación final. Checklist antes de crear el canal: comprobar en YouTube Studio, en este orden, @LaChivaDelPasado → @LaChivaDelPasadoTV → @LaChivaDelPasadoOficial; si los tres están ocupados, detener la creación y volver al libro; comprobar el mismo nombre/handle en las redes donde se reutilicen los Shorts; si se monetiza como marca, revisar el registro ante la SIC antes de invertir en diseño definitivo; registrar fecha, handle obtenido y resultado de la SIC en el control de versiones.
- Nombres descartados por colisión: Colombia en la Memoria / Colombia en Mi Memoria (ya existe un canal con ese nombre publicando el mismo tipo de contenido); Memoria Viva Colombia (colisiona con varios canales «Memoria Viva»); Nostalgia Colombia (genérico, ya usado en TikTok y YouTube, entre ellas @colombianostalgica); Ecos del Ayer (muy usado en música).
- El término «La Chiva» está concurrido fuera del nicho (antiguo periódico de Medellín, una banda musical, uso periodístico de «chiva» como primicia), pero nada de eso bloquea el nombre en este nicho.

### Posicionamiento, promesa, personalidad (secciones 2, 4, 5)

- Posicionamiento: el canal documental en español que recorre la Colombia que ya no existe como quien viaja en una chiva: parada a parada, a partir de hechos reales comprobables (fecha, lugar, fuente y contexto), narrados con la calidez de quien la vivió y el rigor de quien la verificó. Su corazón no es el dato: es la nostalgia de la vida de antes.
- Promesa (textual, §4): «Cada vídeo te devuelve un hecho real de la Colombia que fue, con su fecha, su lugar y la fuente que lo comprueba. Si no lo podemos demostrar, te lo decimos.» Frases derivadas permitidas: para banner y descripción, «Hechos reales de la Colombia que fue, contados con fuentes.»; para intro (máximo 7 segundos), «Súbete, que nos vamos al pasado»; para cierre, «Esto fue un hecho real. La fuente está en la descripción.» y enseguida la despedida de La Ruta (invitar a bajarse en la próxima parada, es decir, en el próximo vídeo). Ninguna otra frase se usa como eslogan sin incorporarla primero al libro.
- Personalidad: el archivista del barrio que además es buen contador de historias, y el conductor de esta chiva. Rasgos: riguroso (fuentes, fechas, correcciones visibles; nunca pedantería ni tono académico frío), cálido (narración cercana, segunda persona moderada; nunca melodrama ni nostalgia llorona), colombiano sin caricatura (nombres, lugares y expresiones con precisión; nunca folclorismo, acentos imitados ni chistes regionales), curioso (preguntas reales; nunca especulación presentada como respuesta), prudente (distingue hecho, testimonio y leyenda; admite lo no confirmado; cuando el hecho está probado, se afirma). Arquetipos: principal Sabio/Archivista; secundario Colombiano común (Everyman).

### Tono y vocabulario (sección 6)

- Tono: documental cálido, nunca sensacionalista. Ritmo 130–150 palabras por minuto (en la práctica del canal la voz Cruz real va a 183–201 ppm; el rango del libro es el del tono, no el de la voz sintetizada). Emoción contenida; humor leve solo si nace del archivo o la costumbre, nunca de las personas; afirmar lo probado y dudar en voz alta lo no probado; cercanía con «En esa época…», «si usted creció en…» con moderación.
- Fórmulas de voz familiar bienvenidas: «en la casa de los abuelos…», «la abuela decía…», «uno llegaba de la escuela y…», «los domingos en familia…», «en la tienda donde fiaban…». Se usan con naturalidad, sin forzar una en cada párrafo.
- La narración habla como quien recuerda en familia, no como un documental de datos. Los hechos verificados se presentan DENTRO de la escena familiar, no como ficha fría: primero la escena, luego el dato que la sostiene, con su fuente en pantalla.
- Vocabulario — usar: «En [año]…», «según [fuente]…», «el registro muestra…»; barrio, tienda, bus, colegio, emisora, canal, plaza (con nombre propio cuando se pueda); «Testimonio», «leyenda urbana», «versión no confirmada» etiquetando; pesos de la época aclarando el año («costaba X pesos en 1985»). Evitar: «Dicen que…», «todo el mundo sabe que…»; «Los viejos tiempos», «la época de antes» como único anclaje; presentar un testimonio como hecho cerrado; convertir precios antiguos a valores de hoy sin explicar el cálculo. Palabras bienvenidas, con moderación: recordar, archivo, época, barrio, costumbre, registro, testimonio, «así era», «así cambió», y el vocabulario de La Ruta: ruta, parada, destino y «súbete» (solo en la apertura oficial y en sus ecos puntuales, no como muletilla).
- Prohibidas en títulos, miniaturas y guiones: «¡increíble!», «¡no lo vas a creer!», «el secreto que nadie te contó», «prohibido», «impactante» y cualquier promesa que el vídeo no demuestre.
- Fechas siempre completas la primera vez: día/mes/año si se conocen; si solo se conoce el año o la década, se dice así («a comienzos de los años 80»), sin inventar el año exacto.
- Guía de voz para narración en off y TTS: voz adulta, serena, timbre medio, sin imitar a ningún locutor real identificable. Si se usa voz sintética, debe declararse según la política vigente de YouTube sobre contenido alterado/sintético y mantenerse la misma voz en toda la serie. Pronunciación: nombres propios colombianos verificados antes de grabar. Pausas marcadas en el guion con [pausa] tras fechas, cifras y giros. La automatización no debe eliminarlas.

### Identidad visual: colores y tipografías (sección 7)

Paleta fija, códigos hex exactos. Proporción orientativa por pieza: 60 % papel/neutros, 25 % sepia y acentos tierra, 15 % color puntual. Nunca los tres acentos fuertes al mismo nivel en la misma pieza. Texto sobre Papel envejecido #F2E8D5 siempre en Café tinta #3B2F2F o Negro carbón #141414. Texto blanco solo sobre 3B2F2F, 1F3A4D, 2E5E4E, B03A2E o 141414, verificando contraste. Prohibido: degradados arcoíris, dorados brillantes tipo premio y rosas/morados neón. El tricolor literal amarillo-azul-rojo en franjas iguales sigue prohibido como fondo o recurso gráfico; su única aparición permitida es la que ya trae el logotipo oficial (pincelada tricolor bajo el texto y bandera al fondo de su escena).

| Color | Hex | Uso |
|---|---|---|
| Papel envejecido | #F2E8D5 | Fondo base, fichas, banner, fondos de gráficos |
| Sepia archivo | #8A6D3B | Filetes, sellos secundarios, fechas, líneas de tiempo |
| Café tinta | #3B2F2F | Texto principal, titulares, cuerpo de ficha |
| Rojo ladrillo colombiano | #B03A2E | Palabra clave en miniatura, sello HECHO REAL, alertas de dato |
| Amarillo mostaza | #D9A441 | Acento cálido: cifras, años destacados, subrayados cortos |
| Verde botella | #2E5E4E | Acento por territorio / naturaleza / transporte; gráficos secundarios |
| Azul petróleo archivo | #1F3A4D | Mapas, noche, televisión/radio, fondos profundos |
| Negro carbón | #141414 | Fondos de cierre, barras de vídeo, contraste máximo |
| Amarillo chiva | #F5B921 | Acento oficial del logotipo (aro, «del Pasado», detalles de la chiva, intro, gráficos de parada). Nunca fondo dominante |
| Azul chiva | #1B4F9C | Acento oficial del logotipo (carrocería, intro, gráficos de La Ruta, mapas). Nunca fondo dominante |
| Rojo chiva | #D22630 | Acento oficial del logotipo (detalles puntuales). No sustituye al Rojo ladrillo #B03A2E en el sello HECHO REAL ni en la palabra clave documental |

Tipografías, roles cerrados (si una no está disponible en la herramienta, se usa la alternativa de la misma fila, nunca una fuente «parecida» elegida por el generador):

| Rol | Tipografía | Uso y regla |
|---|---|---|
| Titulares | Playfair Display Bold | Títulos en gráficos, portadas internas, banner y citas destacadas |
| Miniaturas (alternativa) | Archivo Black | Solo miniaturas y palabras clave cortas. Nunca en cuerpo ni en fichas largas |
| Cuerpo | Inter / Source Sans 3 | Subtítulos, fichas, descripciones, créditos y textos en pantalla. Una sola de las dos por pieza, no mezclarlas |
| Acentos de archivo | Special Elite / Courier Prime | Fechas, sellos, números de ficha, «EXPEDIENTE», líneas de tiempo y datos tipo máquina de escribir. Solo en fragmentos cortos |
| Manuscrita de dichos y agüeros | Caveat (o similar manuscrita legible) | Solo para «El dicho de la ruta», «El agüero de la parada» y la capa decorativa del banner: texto en crema #F2E8D5 sobre fondo oscuro. Nunca en fichas, títulos ni datos verificados |

Nota de producción: en el motor del repo (Documental Expediente) las tipografías operativas son **Bebas Neue** (grande) y **Special Elite** (máquina), en `fuentes/` del repo, con licencia OFL/Apache. Bebas se ve más pequeña, así que los tamaños se subieron: número 360, palabra 400, nombre de apertura 150.

### Estilo de ilustración y fotografía (sección 8)

1. Primero, foto real de época (fotografía, prensa, documento o captura de época con derechos o uso permitido): esa es la imagen principal. Se restaura con prudencia: limpiar polvo y mejorar contraste sin recolorizar inventando colores ni «mejorar» rostros con IA.
2. Segundo, documento: recortes de prensa, avisos, carátulas, etiquetas y mapas de época valen más que una ilustración bonita: son la prueba.
3. Tercero, recreación etiquetada: cuando no hay foto, ilustración editorial en la paleta del canal (sepia, papel, café tinta) y se etiqueta en pantalla como «Recreación» durante todo el tiempo que aparece. Nunca se presenta una imagen generada como si fuera una foto real.
- Estilo permitido: ilustración editorial documental, acuarela/grabado suave o foto-ilustración con grano, textura de papel y bordes de archivo. Prohibido: 3D brillante, anime, caricatura infantil, collage caótico de stickers, imágenes de stock genéricas de otros países haciéndose pasar por Colombia.
- Personas: ropa, peinados y objetos coherentes con la década exacta del hecho. Si no se puede garantizar esa coherencia, se muestra el lugar o el objeto, no personas inventadas.
- Restauración: se permite ajustar niveles y recorte. No se permite añadir o quitar personas, cambiar letreros, ni completar partes faltantes de un documento sin etiquetarlo como recreación.

### Reglas de composición (sección 9)

- Un foco por plano: cada imagen responde a una sola afirmación de la narración.
- Retícula de archivo: imagen principal a la izquierda o a sangre completa con ficha en el tercio inferior; nunca texto centrado sobre una foto ocupada sin fondo de papel detrás.
- Margen de papel: toda foto de época sobre fondo Papel envejecido #F2E8D5 o Negro carbón #141414, con filete Sepia archivo #8A6D3B de 2–4 px. Nada de fotos flotando sobre degradados.
- Regla de tercios y aire: al menos un 20 % de la composición sin información. La densidad alta se reserva a la miniatura del formato insignia, no al interior del vídeo.
- Mapas y líneas de tiempo ocupan la pantalla completa cuando aparecen.
- Lower thirds: fondo Café tinta, texto en Papel envejecido, nombre y rol/fecha en Special Elite. Máximo 6 segundos.
- Transiciones: fundido, corte seco o paso de página de archivo. Prohibidos giros 3D, zooms agresivos tipo meme y transiciones de destello.

### Sistema de gráficos (sección 10)

| Pieza | Composición fija | Cuándo aparece |
|---|---|---|
| Ficha de archivo | Tarjeta Papel envejecido, filete sepia, fecha y lugar en Special Elite, hecho en 1 línea en Inter | Al abrir cada hecho o bloque numerado |
| Sello HECHO REAL | Sello circular/rectangular irregular en Rojo ladrillo #B03A2E: «HECHO REAL» + año | Sobre la foto principal y en la miniatura; solo si el hecho está verificado con 2 fuentes |
| Sello TESTIMONIO | Sello en Sepia archivo: «TESTIMONIO» | Cuando la fuente es memoria oral o un relato personal |
| Sello LEYENDA URBANA | Sello en Azul petróleo: «LEYENDA URBANA — NO CONFIRMADO» | Cuando se menciona un rumor para desmentirlo o contextualizarlo, nunca como afirmación |
| Sello CREENCIA POPULAR | Sello en Azul petróleo archivo #1F3A4D: «CREENCIA POPULAR» | Obligatorio en todo agüero. Nunca junto a un dato afirmado como hecho |
| Mapa de época / actual | Base en Azul petróleo / Verde botella, punto en Rojo ladrillo, rótulo en papel | Cuando el lugar es parte del hecho; siempre con norte y fuente del mapa |
| Línea de tiempo | Eje Sepia sobre papel, hitos en Café tinta, año destacado en Amarillo mostaza | En procesos largos: cierres, transformaciones, trayectorias |
| Cifra destacada | Número grande en Playfair Display, unidad y año debajo en Special Elite | Precios, años, cantidades — siempre con año y fuente en la misma pantalla |
| Numeración de listado — marcador de parada (La Ruta) | Tiquete / placa de ruta sobre Papel envejecido: «PARADA n.º» con el número grande en Archivo Black y un solo acento chiva (#F5B921, #1B4F9C o #D22630) | En cada ítem del formato insignia numerado, junto a la ficha de archivo del ítem |
| Ruta del episodio | Recorrido completo estilo ruta de chiva: destino (el tema) y paradas numeradas, sobre papel, con la chiva del logotipo como marcador de avance | Al abrir el vídeo (tras la ficha inicial) y, en versión breve, antes del cierre |
| Tarjeta de dicho / agüero | Tarjeta sobre fondo oscuro (#141414 o #1F3A4D): el dicho o agüero en letra manuscrita Caveat o similar, en crema #F2E8D5, con el sello que le corresponde (TESTIMONIO para el dicho; CREENCIA POPULAR para el agüero). Sin fecha ni región atribuidas salvo que haya fuente | Al cierre de la parada elegida, en «El dicho de la ruta» / «El agüero de la parada» |
| Banner oficial | 2560 × 1440 px, logotipo, nombre y descriptor dentro de la zona segura central de 1546 × 423 px; dichos y agüeros manuscritos semitransparentes en el fondo | Cabecera del canal |

- Todos los gráficos se exportan desde una misma plantilla. La automatización solo cambia textos, fechas e imágenes dentro de los campos previstos; no recoloca ni recolorea piezas.
- Fuente en pantalla: toda ficha, cifra y mapa lleva su fuente en letra pequeña (mínimo legible en móvil) en la misma pantalla, no solo al final del vídeo.

### Recursos recurrentes (sección 11)

- **Intro y apertura La Ruta — 5 a 7 segundos:** logotipo oficial sobre fondo Negro carbón o Papel envejecido, con la chiva como vehículo y una sola línea de audio compuesta para el canal. Apertura oficial, textual, en la narración: **«Súbete, que nos vamos al pasado»**. Sin montaje de clips.
- **Cortinilla de parada:** marcador «PARADA n.º» que entra con el sonido de archivo. Máximo 1,5 segundos. En el formato narrativo, paso de ficha de archivo con el año.
- **Música de fondo:** (ver conflicto resuelto n.º 3: los videos producidos son solo voz; la línea del libro —instrumental cálida y discreta, sin letra, -18 a -24 dB bajo la narración, nunca una canción reconocible de época como fondo sin licencia— NO se aplica en la práctica del canal.)
- **Sonido de archivo:** toque breve de papel / sello al entrar una ficha o un sello. Siempre el mismo archivo de sonido.
- **Cierre fijo:** pantalla Negro carbón con el logotipo oficial, frase de cierre («Esto fue un hecho real. La fuente está en la descripción.»), invitación concreta a comentar un dato verificable («¿En qué año lo conoció usted?») y despedida de La Ruta (invitar a bajarse en la próxima parada, es decir, en el próximo vídeo, anunciándolo solo si ya está producido). En la práctica vigente el cierre además invita a la lista de reproducción (regla Samu 2026-11-02).
- **Descripción tipo:** primer párrafo: hecho, fecha y lugar. Segundo: fuentes con enlaces. Tercero: capítulos. Cierre: descriptor del canal y aviso de recreaciones, si las hubo. Plantilla en el Anexo A. (El formato entregado real se detalla en §10.)
- **Hashtags / etiquetas base:** #LaChivaDelPasado #NostalgiaColombia #HistoriaDeColombia + 2–3 etiquetas del hecho concreto. Nunca más de 5 hashtags en la descripción visible.
- **Sistema La Ruta (transversal):** cada vídeo es una ruta de la chiva: el tema es el destino, cada ítem numerado es una parada con su número en pantalla («Parada 7»), la apertura es «Súbete, que nos vamos al pasado» y el cierre invita a bajarse en la próxima parada / próximo vídeo. La metáfora ordena la narración; nunca sustituye datos, fechas ni fuentes.
- **El dicho de la ruta (recurso emocional INSIGNIA del canal, v1.3):** en cada vídeo largo, al menos una parada se cierra con un dicho popular de la época relacionado con el tema de esa parada. Tarjeta manuscrita (sección 10) con sello TESTIMONIO. El narrador lo lee con la fórmula «como decían las abuelas…» o «como se decía en el pueblo…». La voz de los abuelos es la voz emocional del canal, aunque el tema del vídeo sea otro.
- **El agüero de la parada:** cuando el tema de una parada lo permite (costumbres, casa, Año Nuevo, vida cotidiana), la parada puede cerrarse con un agüero de la época en la misma tarjeta manuscrita, siempre con el sello CREENCIA POPULAR y la misma fórmula de presentación. Un agüero NUNCA se presenta como HECHO REAL.
- **Banco inicial de dichos (sello TESTIMONIO / cultura popular; sin origen, fecha ni región atribuidos):** «El que madruga, Dios le ayuda» · «Más sabe el diablo por viejo que por diablo» · «Al que le van a dar, le guardan» · «No hay mal que por bien no venga» · «Camarón que se duerme, se lo lleva la corriente» · «El que mucho abarca, poco aprieta».
- **Banco inicial de agüeros (sello CREENCIA POPULAR; se cuentan como lo que se creía y se practicaba, nunca como efecto real):** la sal no se pasa de mano en mano, porque trae pelea · nada de barrer de noche · mariposa negra en la casa: anuncia visita · abrir la sombrilla dentro de la casa trae mala suerte · dejar la cartera en el suelo hace que se vaya el dinero · las 12 uvas a medianoche (Año Nuevo) · la ropa interior amarilla (Año Nuevo) · la vuelta a la manzana con la maleta (Año Nuevo) · las lentejas en el bolsillo (Año Nuevo).
- **Regla de uso del banco:** estos dichos y agüeros se presentan tal cual, sin atribuirles origen, fecha ni región. Si en un vídeo concreto se quiere afirmar un origen, ese origen entra en la ficha de fuentes (Anexo A) con su fuente, como cualquier otro dato; sin fuente, se dice solo «se decía». El banco crece vídeo a vídeo, siempre con la misma regla.
- **Estructura fija del vídeo largo documental (formato narrativo):** gancho con prueba 0:00–0:30 (el hecho y su prueba más fuerte; nada de saludos largos); ficha y contexto 0:30–2:00 (ficha de archivo, mapa o línea de tiempo); desarrollo 2:00–80 % del vídeo (el hecho en orden cronológico o por ítems numerados, cada uno como parada de La Ruta); contraste ayer / hoy (penúltimo bloque); cierre y fuentes (últimos 60–90 s: conclusión, qué no se pudo confirmar si aplica, fuentes en pantalla, cierre fijo y despedida de La Ruta).

### Pautas de miniatura del libro (sección 12)

- Regla base: contraste alto, 3 a 5 palabras en mayúsculas, foto real de época restaurada, franja inferior sepia con sello «HECHO REAL» + año; combinada, en el formato insignia, con la franja superior de la sección 19.
- Composición estándar (narrativo): fondo foto real de época restaurada (al menos el 70 % de la superficie, sujeto reconocible a tamaño grande); texto 3–5 palabras en mayúsculas, Archivo Black, en Café tinta o blanco según el fondo, palabra clave en Rojo ladrillo #B03A2E; legible al 10 % del tamaño en un celular; franja inferior sepia: sello «HECHO REAL» en Rojo ladrillo + año del hecho en Special Elite (firma del canal, no se omite); un solo número o año grande está permitido como elemento principal («1985», «25») si es el gancho real del vídeo.
- Composición del formato insignia (listados): franja superior blanca del 15–18 % de la altura, texto en condensada negra en mayúsculas de 2 a 5 palabras, en varias la última palabra gancho va en rojo; escena densa y cálida, sepia, llena de objetos/productos reconocibles colombianos de la época y, cuando aplique, personas con ropa de época y expresión emocional; se mantiene la franja inferior sepia con «HECHO REAL» + año/rango como diferencial propio; detalle chiva permitido: un solo acento chiva en el marcador de parada o en un borde corto, nunca como fondo dominante, nunca reemplazando la palabra clave en Rojo ladrillo ni la franja inferior; el texto de la miniatura NO repite el título: lo comprime en una frase emocional de 2 a 5 palabras (patrón verificado: «SE FUERON CALLADITO», «¡YA NADIE LAS HACE!», «TODOS LOS TUVIMOS»); SIN número en la miniatura (el número vive solo en el título) y SIN logotipo ni nombre del canal; variación propia: el sello HECHO REAL + año va pequeño en la esquina inferior, sin tocar la franja superior; escena generada con IA: permitida como ilustración de miniatura, nunca presentada dentro del vídeo como foto real; si un objeto se ve falso, con texto deformado o de otro país, la miniatura se rehace.
- Prohibido en miniaturas: flechas rojas genéricas, círculos de «shock», bocas abiertas exageradas, antes/después falsos y textos que prometen lo que el vídeo no demuestra; más de 5 palabras; logos de marcas actuales como gancho; banderas como fondo completo; usar la foto de una persona real en una situación que no vivió, ni un montaje que altere un documento histórico.
- Prueba antes de publicar: 1) ver la miniatura a 120 px de ancho (¿se leen las palabras y se reconoce el sujeto?); 2) ¿la palabra en rojo es realmente la clave del hecho?; 3) ¿el año de la franja coincide con la ficha y con el guion? Si no, no se publica.

### Veracidad, derechos y correcciones (sección 13)

- **Regla de oro:** prohibido inventar datos. Toda afirmación relevante lleva fuente. Si una fuente no alcanza, se etiqueta, se matiza o se elimina; nunca se completa con imaginación.
- Separación obligatoria: **HECHO** (al menos 2 fuentes independientes, o 1 fuente primaria/documental sólida; se afirma, con sello HECHO REAL y fuente en pantalla y en la descripción); **TESTIMONIO** (relato de una persona, memoria familiar, comentario o fuente única no documental; se atribuye «según el testimonio de…», con sello TESTIMONIO, sin convertirlo en dato cerrado); **LEYENDA URBANA** (historia muy repetida sin prueba, o contradicha por el registro; se nombra solo para contextualizar o desmentir, con sello LEYENDA URBANA — NO CONFIRMADO); **CREENCIA POPULAR** (agüero o creencia tradicional; es un dato sobre lo que la gente creía, no sobre el mundo; se presenta SOLO como creencia, con el sello CREENCIA POPULAR y la fórmula «como decían las abuelas…» / «como se decía en el pueblo…»; NUNCA como HECHO REAL).
- Dichos, regla cerrada: un dicho es SABIDURÍA POPULAR y se etiqueta TESTIMONIO / cultura popular, con su tarjeta manuscrita y el sello TESTIMONIO. No necesita dos fuentes como un hecho, porque no se afirma un dato: se comparte lo que se decía. Prohibido inventarle pedigrí: nada de atribuirle origen, fecha, región o autor sin fuente.
- Agüeros, regla cerrada: un agüero es CREENCIA POPULAR. Se puede contar que se practicaba, quiénes lo recuerdan y en qué momentos salía, pero jamás se afirma que funcione, que traiga suerte o que anuncie nada de verdad. Si la narración necesita el verbo, es siempre en clave de creencia: «se creía que…», «decían que…».
- Origen de dichos y agüeros, prohibido inventarlo: si se afirma el origen, la fecha o la región, esa afirmación es un dato más del vídeo y debe ir con fuente en la ficha; sin fuente, se presenta solo como «se decía».
- Estándar de fuentes (jerarquía): 1) documentos y archivos oficiales, hemeroteca y prensa de época; 2) libros e investigaciones con referencias; 3) prensa actual seria que cite fuentes; 4) testimonios identificados. Un blog sin fuentes, un comentario u otro vídeo de YouTube nunca son fuente única. Cada vídeo guarda una ficha de fuentes (Anexo A) con: afirmación, fuente, fecha de consulta y categoría (hecho/testimonio/leyenda/creencia popular). Sin ficha completa, el guion no pasa a grabación. Fechas, cifras, nombres de empresas/personas y lugares se verifican en dos pasos: en la fuente y contra una segunda referencia. Los errores más dañinos son los «casi correctos».
- Derechos y uso de archivo: usar material de archivo solo con licencia, dominio público, permiso o un uso que el responsable haya revisado. Ante la duda de derechos, se describe y se ilustra con recreación etiquetada, no se toma el material. No subir vídeos completos de programas, comerciales ni canciones de época como contenido principal. Crédito en pantalla o en la descripción para archivos y fotografías cuyo titular lo exija o sea identificable.
- Correcciones: si la audiencia demuestra un error, se responde, se fija un comentario de corrección y, si el error afecta al hecho central, se corrige la descripción y se valora reeditar o retirar el vídeo. **Ocultar un error demostrado está prohibido**: la confianza es el activo del canal.
- Checklist de calidad de guion (resumen): ¿el hecho central se puede escribir en una frase con fecha y lugar? ¿Cada ítem del listado existe y está verificado para Colombia, no copiado de otro país? ¿Ninguna cifra quedó sin año? ¿Ningún testimonio quedó disfrazado de hecho?

### Referencias visuales conceptuales (sección 14)

Tres referencias creadas para el libro (definen ambiente, paleta, textura y composición; NO son fotografías históricas y nunca deben publicarse como si lo fueran): 1) El archivo (mesa de archivo sobre Papel envejecido, cajas en Verde botella y Rojo ladrillo desaturado, ventana con luz lateral; fondos de fichas, intros, vídeos sobre prensa/empresas/documentos; evitar convertirlo en oficina moderna); 2) La calle y el barrio (calle de barrio de los años 80: tienda, bus de época y juego en la acera, cielo amplio para titular; escena cálida y sepia; referencia para la densidad controlada de objetos; evitar calles genéricas de otro país, señalización en otro idioma o vehículos de una década distinta); 3) El interior doméstico (televisor de perillas, radio, álbum de fotos y retratos; Amarillo mostaza y Verde botella en mobiliario, fotos en blanco y negro; priorizar objetos sobre personas cuando la recreación no sea precisa; evitar interiores de catálogo actual, pantallas planas, objetos anacrónicos).

### Qué NO debe producirse (sección 16)

- Contenido: hechos inventados, fechas «aproximadas» presentadas como exactas, diálogos recreados como si fueran citas reales, listas copiadas de otro país cambiando solo el nombre; contenido copiado del canal de referencia o de cualquier canal (ni textos, ni guiones, ni miniaturas, ni el orden de ítems); nostalgia industrial abstracta como tema principal sin anclaje tangible y doméstico (si un tema industrial se aborda, entra por un objeto, una tienda o una costumbre concreta); cualquier tema que NO evoque ningún recuerdo vivido, aunque el dato sea interesante o esté de moda; sensacionalismo con tragedias, delitos o víctimas (nada de morbo, reconstrucciones gráficas, ni títulos que exploten el dolor; un hecho doloroso solo se aborda si aporta comprensión histórica y con trato sobrio, sin imágenes gráficas); política partidista actual, propaganda, teorías de conspiración presentadas como hechos, contenido que afirme como real una leyenda urbana; farándula, vida privada actual de personas y «dónde están ahora» sin hecho histórico y sin fuente pública sólida.
- Producción: imágenes generadas presentadas como fotos reales; rostros de personas reales generados o alterados; documentos «completados» con IA sin etiqueta de recreación; música, vídeos o fotos de época reutilizados sin revisar derechos; canciones reconocibles como fondo «porque son de la época»; voces sintéticas que imiten a una persona real identificable, viva o fallecida; clickbait (preguntas falsas en el título, promesas que el vídeo no cumple, miniaturas con hechos que no salen en el vídeo); publicar sin ficha de fuentes, sin revisar nombres/fechas contra la segunda referencia, o con la miniatura sin pasar la prueba de los 120 px; contenido en cadena sin revisión humana (la automatización prepara, un responsable aprueba guion, fuentes y miniatura antes de publicar; «automático» nunca significa «sin verificar»).

### Constantes y variables (sección 17) y flujo (sección 18)

- Constantes (nunca cambian sin nueva versión del libro): nombre, descriptor y logotipo oficial; paleta completa con hex y proporciones; tipografías y sus roles; ficha, sellos y su diseño; intro, cortinilla, sonido de sello y cierre fijo; sistema de miniatura; estructura de bloques y plantilla de descripción; criterios de veracidad, ficha de fuentes y lista de prohibiciones; voz de narración y su ritmo base; formato insignia numerado y sus reglas de título; sistema La Ruta; «El dicho de la ruta» y «El agüero de la parada».
- Variables: el hecho central y su territorio; el acento de color dominante dentro de la paleta; el texto concreto de fichas, títulos y miniaturas; qué sellos aparecen; la pregunta concreta de cierre a comentarios; la foto/ilustración, palabra clave y año de cada miniatura; la duración exacta dentro del rango del formato; las fuentes, el mapa y la línea de tiempo de cada hecho; el énfasis y las pausas según el guion; el número de ítems (siempre igual al número real de ítems verificados); la ruta concreta de cada episodio; el dicho o agüero concreto de cada episodio.
- Pipeline por episodio: 1) tema (desde los territorios, priorizando lo tangible; filtro previo obligatorio: prueba del recuerdo VIVIDO); 2) investigación (ficha de fuentes completa ANTES de escribir una línea de guion; mínimo 2 fuentes independientes para el hecho central y para cada ítem); 3) guion (plantilla fija por formato, con [pausa], pronunciaciones verificadas y categoría de cada dato marcada al margen: H / T / L); 4) activos visuales (foto/documento real primero; recreación etiquetada después; todo activo registrado con su fuente y su estado de derechos en la ficha); 5) voz y montaje (misma voz, misma plantilla gráfica, Short derivado del mismo máster); 6) miniatura y metadatos (desde plantilla, prueba de 120 px, plantilla de descripción); 7) revisión humana y publicación (checklist completo; sin checklist no hay publicación).
- Cadencia: el canal de referencia hace casi un vídeo largo al día, pero para un creador que inicia esa cadencia solo se adopta si el pipeline la sostiene sin bajar la verificación: es preferible publicar menos y correcto que diario y con errores. Cadencia inicial recomendada: 2–3 largos por semana, con su Short derivado, y subir solo cuando la ficha de fuentes se mantenga completa en todos. (En la práctica vigente, por orden de Samu: publicar TODOS los días sin huecos.)
- Checklist de publicación (sección 18, marcar cada casilla): principio rector (recuerdo VIVIDO; al menos una parada se cierra con «El dicho de la ruta»); nombre/handle y descriptor coinciden con la sección 1; hecho central con fecha, lugar y 2 fuentes en la ficha; cada ítem numerado verificado para Colombia; ningún testimonio ni leyenda aparece como hecho; sellos en pantalla coinciden con la categoría de cada dato; ningún agüero como HECHO REAL; título con formato correcto, sin clickbait, sin palabras prohibidas, promete solo lo que el vídeo cumple; en el formato insignia, fórmula verificada (número + categoría tangible + ancla + cláusula de pérdida, sin «?» ni «:»); miniatura (contraste alto, palabras dentro del límite, palabra clave en Rojo ladrillo, franjas y sello + año correctos, prueba de 120 px; en insignia: franja superior 15–18 %, texto emocional que no repite el título, sin número ni logotipo); visuales (ninguna recreación sin etiqueta; ningún activo sin estado de derechos; ningún anacronismo); audio (voz clara, pausas respetadas, ninguna canción de época sin licencia como fondo); descripción (plantilla completa, fuentes con enlaces, capítulos, aviso de recreaciones y de voz sintética si aplica); Short derivado listo y enlazado al largo; revisión humana final hecha por una persona distinta al flujo automático, o en una segunda pasada separada en el tiempo.

### Análisis del canal de referencia (sección 19)

- Datos reales (API, 15/10/2026): creado 27 de julio de 2026; primer vídeo 19 de septiembre de 2026; 29 vídeos en 26 días (22 largos en 27 días: casi un largo al día); 1.910 suscriptores; 1.268.393 visualizaciones; media más de 43.000 vistas por vídeo con menos de 2.000 suscriptores. Lectura: el tráfico viene de vídeos sugeridos y exploración, no de suscriptores.
- Formato único, repetido al 100 %: listados numerados como único formato (30 en 14 vídeos, 25 en 7, 37 en 1); 19 de los 22 largos contienen alguna forma de DESAPARECER (los demás usan sinónimos: «Ya Nadie Prepara», «Dejaron de Funcionar»); nunca signos de interrogación ni dos puntos en el título; longitud del título 55–99 caracteres, mediana 84; largos de 25:49 a 39:06, mediana ~33 minutos; Shorts de 26 a 54 segundos que son avances del largo, con el mismo título (vistas bajas, 500–3.200: embudo, no motor de crecimiento).
- Fórmula rectora del título insignia: **[NÚMERO] + [CATEGORÍA tangible] + [ancla de país/época/familia] + [cláusula de pérdida]**. Mayúsculas selectivas: solo 1–3 palabras gancho en mayúsculas; el resto en formato frase; nunca el título entero en mayúsculas. 5 de los 22 usan puntos suspensivos «…» antes de la cláusula final (recurso permitido, no obligatorio). Sufijo «(Parte 2)» solo para secuelas reales de un tema que ya funcionó.
- El vídeo que explotó: el tercer vídeo publicado concentra cerca del 40 % de todas sus vistas (25 marcas fabricadas en México, 32:22, 514.951 vistas); su «Parte 2» alcanzó 113.572 vistas. Regla: una serie con «Parte 2» funciona cuando el original explota; no se produce una Parte 2 por rutina.
- Temas que rinden: marcas, productos, juguetes, comidas y tiendas concretas y reconocibles; lo que se tocaba, se comía, se compraba o se veía en casa; nostalgia doméstica y de consumo cotidiano. Temas que no rinden: industria pesada y conceptos abstractos (acerías y minería de hierro, 683 vistas; fábricas que empleaban pueblos, 3.490; tecnologías de los hogares como concepto abstracto, 4.534). **Regla: nostalgia tangible y doméstica gana; nostalgia industrial abstracta pierde. Todo tema debe poder nombrarse como un objeto, un lugar, una tienda, un programa o una costumbre concreta.**
- Miniaturas del referente (patrón verificado en sus vídeos top): debajo de la franja, escena fotorrealista generada con IA, cálida y sepia, muy densa (familia multigeneracional con emoción visible y primer plano lleno de productos/objetos reconocibles de la época, con ropa de época); franja superior blanca del 15–18 % de la altura, texto en condensada negra en mayúsculas de 2 a 5 palabras, en varias la última palabra gancho va en rojo; el texto NO repite el título, lo comprime en una frase emocional (ejemplos reales citados solo como patrón: «SE FUERON CALLADITO», «¡YA NADIE LAS HACE!», «TODOS LOS TUVIMOS»); SIN número en la miniatura; SIN logotipo ni nombre del canal.
- Adaptación obligatoria a Colombia — SE MANTIENE (formato): listado numerado como formato insignia; número al inicio del título; duración larga (25–35 min en el libro; ver conflicto resuelto n.º 1: hoy 17–20 min); cadencia alta sostenida por automatización con revisión humana; miniatura con franja superior blanca y palabra clave en rojo (Rojo ladrillo #B03A2E); gancho de desaparición. SE CAMBIA (diferencial propio): hechos reales verificados con fuentes y fechas en pantalla y en la descripción (el referente no documenta fuentes); no depender solo de productos (tiendas, programas de TV, costumbres y lugares, siempre tangibles); datos colombianos verificados con fuentes propias; identidad propia (paleta, sellos y franja inferior «HECHO REAL» + año); textos, guiones y escenas siempre originales para Colombia.
- Dato sobre dichos (re-revisión 15/10/2026): el largo de dichos del referente («30 DICHOS…») sumó 6.595 vistas, por debajo de su media. Conclusión del libro: los dichos rinden mejor como recurso recurrente dentro de los vídeos que como tema principal de arranque; el vídeo de dichos queda como vídeo posterior, NO de lanzamiento. (Nota: la investigación posterior por comentarios —§5— matiza esto: Dichos es la apuesta de lista más segura, cero derechos; ver ranking vigente.)
- Ejemplos de títulos adaptados (plantillas de formato; solo se publican si el número coincide con los ítems realmente verificados y cada ítem tiene su entrada en la ficha de fuentes): «25 marcas colombianas en las que confiaban las familias y desaparecieron» · «30 productos de los 80 en Colombia que fueron un desastre y desaparecieron» · «25 juguetes hechos en Colombia que todos tuvimos y desaparecieron» · «25 dichos de las abuelas que ya nadie dice» · «20 agüeros de Año Nuevo que toda Colombia conocía».

### Plantillas del Anexo A (listas para copiar)

- **A1. Ficha de fuentes (una por vídeo):** título provisional / formato; hecho central en una frase (con fecha y lugar); afirmación / ítem n.º; categoría HECHO / TESTIMONIO / LEYENDA / CREENCIA POPULAR (para dichos: TESTIMONIO / cultura popular; si se afirma su origen, fuente obligatoria); fuente 1 (nombre + enlace o referencia completa); fuente 2 / fuente primaria; fecha de consulta; activo visual (foto/documento/recreación) + estado de derechos; ¿pasa a guion? SÍ / NO y por qué.
- **A2. Descripción de YouTube (plantilla):** párrafo 1: [Hecho] ocurrió en [lugar] en [fecha]. En este vídeo lo reconstruimos con [tipo de fuentes]. Párrafo 2 — Fuentes: lista con enlaces, en el mismo orden en que aparecen en el vídeo. Párrafo 3 — Capítulos: 00:00 Gancho · [marcas de tiempo por bloque/ítem]. Párrafo 4 — Avisos: recreaciones utilizadas (minuto), voz sintética si aplica, correcciones si las hubo. Cierre: «La Chiva del Pasado — Nostalgia colombiana · Hechos reales. Si no lo podemos demostrar, te lo decimos.»
- **A3. Título (plantilla por formato):** insignia: «[NÚMERO] + [categoría tangible] + [ancla de país/época/familia] + [cláusula de pérdida]» — número inicial obligatorio, 55–99 caracteres (mediana 84), mayúsculas solo en 1–3 palabras gancho, resto en formato frase, sin interrogación ni dos puntos nunca; «…» opcional antes de la cláusula final; sufijo «(Parte 2)» solo en secuelas reales. Narrativo: «[Nombre propio / lugar]: [hecho] en [año]» — sin adjetivos no demostrados.
- **A4. Guion (encabezado de cada bloque):** BLOQUE / PARADA n.º: [nombre] · Categoría: H/T/L/CP (hecho, testimonio, leyenda, creencia popular) · Ficha en pantalla: [fecha, lugar] · Activo visual: [archivo/recreación] · Fuente en pantalla: [fuente corta] · Dicho/agüero de cierre, si aplica: [texto, sin origen atribuido sin fuente].
- **Control de versiones:** v1.0 (15/10/2026, creación, nombre propuesto «La Colombia Que Fue»); v1.1 (15/10/2026, nombre principal pasa a «La Chiva del Pasado», «La Colombia Que Fue» respaldo, descriptor, logotipo oficial, acentos chiva, sistema La Ruta); v1.2 (15/10/2026, dichos y agüeros como recurso oficial, cuarto sello CREENCIA POPULAR, banco inicial 6 dichos + 9 agüeros, banner 2560×1440, re-revisión del referente con API); v1.3 (15/10/2026, principio rector nostalgia emocional y familiar, dichos como recurso INSIGNIA); v1.4 (15/10/2026, corrección «no así tan literal»: nostalgia de la vida de antes en sentido amplio, familia como centro de gravedad y tono, prueba del recuerdo VIVIDO, lista oficial de territorios, se suman novelas y películas colombianas); v1.5 (15/10/2026, audiencia unificada en un solo párrafo, se elimina la tabla de segmentos).

---

## 4. La voz propia de Luis Carlos (la voz que manda en los guiones)

Fuente: `~/workspace/nostalgia_colombia/muestras_voz_luis_carlos.md`. Dos muestras ESCRITAS A MANO por él el 2026-10-21 «para que entiendas mi forma de escribir natural humana y lo que se desea transmitir». **Texto VERBATIM, con su ortografía y ritmo originales: NO corregir.** Son material de entrenamiento de voz (método de Samu: entrenar a la IA con el lenguaje del creador desde su texto escrito a mano). Sirven para el prompt de Claude (bloque «ASÍ HABLO YO») y para reescribir guiones con su voz.

### Muestra 1 — Juguetes (trompo y cometa) — VERBATIM

Título de referencia: «12 Juguetes HECHOS EN COLOMBIA que TODOS Tuvimos en la Casa… y Desaparecieron»

> Quien no recuerda esos tiempo de pelao jugando en el barrio o junto a tus primos o tus hermanos con un trompo de madera, con un pita o cabuya ya negra de tanto uso, que uno le daba varias vueltas en el trompo con cuidado y apretaba bien duro los dedos y se preparaba para el mejor lanzamiento del siglo y lo lanzavbas con bastante fuerte mientras para que cayera en medio de un circulo dibujado con tiza blanca en suelo. todos tus primos se preparaba también para hacer un inccreible batalla entre todos. Aveces lo tirabas mal y no quedaba bailando en la punto y tus primos se reian, a pero si lograbas hacer que tu trompo cayera bien y durara mas tiempo girando , te parazabas con los brazos cruzado como el mayor de los orgullos, ya con tus amigos o compañeros d ecolegio las cosas eran mas serias se apostaba cual quier cosa m tapas, canicas los mas arriesgados hasta la lonchera que les habían empacado sus mama. El que perdia perdia y se iba con la cabeza baja pero regresaba al otro para pedir la revancha, recuerdas que siempre había uno o dos amigos que eran los mas hbailidos que sabían hacer trucos porse el trompo en la mano pararlo en puente en cabuya del trompo hacerle una vuelta al mundo en la mano, y todos tus cañero reunidos en circulo viendo el espectáculo.
>
> Quien no recuerd atembien la cometa hecha en casa para julio y agosoto, que uno iba a comprar papelillo a la tienda de la esquina se compraba sus 3 pales d tu equipo de futbol favorito, y te iba con tus amigos por todo el barrio a busca varilla de guada para hace tu cometa, y uno emepzava con los panas a partir en trozos para hacer la cometa mas grande que pudieras que habina unos que se hacias una tajada o un plato los mas ocncoedores se hacían un ovni, que ya como adepsues de 3 horas todos juntaban dinero entre todos y se iban a comprar un pacito y una coca cola para tomar. Ya cuando tenias tu cometa forrada faltaba lo ma simportante la cola, esa cola que era siempre un dile, si era corta empezaba a dar vueltas en cielo y tu cometa se caiam si era muy larga y pessba la cometa no podía subir. Tenia su medida excata que solo la cojias llendo a probarla una y otra vez, hasta que una migo tuyo que te la tenia la cometa en en uno 10 o 15 metros de distancia para que nos cayera al suelo y ya estaba cansado de tanto ir y volver. Y de repente llegaba un ráfaga de viento y tu corrias para que se levara y cuando te daba vuelta tu cometa ya se estaba alzando vuelo y todas la personas del lugar se quedbaan mirando al cielo como elevaba la cometa, y ya cuando agrraba altura eso era una elagncia y uno se llenaba de una alegría que que no le había en el pecho

### Muestra 2 — Dulces (la tienda del colegio y los Motitas) — VERBATIM

Título de referencia: «30 Dulces COLOMBIANOS de la TIENDA DEL COLEGIO que Comprábamos con Monedas… y Desaparecieron»

> Sonaba la campana del recreo y salíamos disparados, porque la fila de la tienda se llenaba en segundos y el que llegaba tarde se quedaba sin lo bueno. La señora de la tienda ya nos conocía a todos sabía quién pedía fiado, quién pagaba con la moneda grande y quién llegaba con las monedas contadasuna por una en la palma de la mano. Esas monedas nos las daba la mamá en la mañana, antes de salir, a veces amarradas en la puntica del pañuelo o sueltas en el bolsillo del uniforme. Había que cuidarlas como un tesoro, porque si se perdían en el camino, ese día el recreo se mira pero no se comía. Y casi siempre pedíamos lo mismoun Motitas, el chicle grande del empaque con el leopardo. El de banano era el primero que se acababa, y si alcanzábamos uno, sentíamos que el día ya había valido la pena. Ese chicle no era para uno solo se partía en pedazos sobre la tapa del pupitre y se repartía entre los de siempre. El que compraba repartía, y el que recibía quedaba en deuda dulce para el día siguiente.

### Rasgos de su voz (extraídos de las muestras)

- Apertura con escena en movimiento o con «Quién no recuerda…»: nunca con un dato.
- Frases largas en cadena de acciones («y uno… y después… y de repente…»): la memoria fluye sin cortes de presentador.
- Segunda persona cómplice: «recuerdas que siempre había uno o dos amigos que…».
- Micro-detalles físicos que solo conoce quien estuvo: la pita ya negra de tanto uso, el círculo de tiza, las monedas amarradas en la puntica del pañuelo, partir el chicle sobre la tapa del pupitre.
- Emociones chiquitas y verdaderas: el orgullo con los brazos cruzados, la cabeza baja del que pierde, «una alegría que no le cabía en el pecho».
- Economía de pelaos: apuestas (tapas, canicas, hasta la lonchera), el fiado, la «deuda dulce» para el día siguiente; juntar entre todos para el panecito y la Coca-Cola.
- Nada de fechas ni de datos fríos: si aparecen, van dentro de la acción, nunca como información.

### Lo que rechazó (y por qué)

- **2026-10-21:** rechazó el primer guion de Marcas por «informar» la nostalgia en vez de contarla. Exige voz de **CONTADOR DE HISTORIAS HUMANO**: escenas desde adentro, primera persona, emoción por delante, datos escondidos en el recuerdo.
- **2026-10-31:** reforzó el rechazo: texto que sonaba «muy IA».
- **2026-11-05 13:19 (Tragedias v1):** «MAS HUMANO Y MENOS REPETITIVO Y IA». El defecto concreto: las 12 paradas abrían «Quién no recuerda» y 11 cerraban «Y por eso nadie puede olvidar» (molde repetitivo = suena a IA). La reescritura v2 varía cada apertura y cada cierre: «Quién no recuerda» 12→2, «nadie puede olvidar» 12→5, «lo que más dolía» 0.
- **Regla de oro del guion:** cada parada se construye sobre microdetalles vividos de uso (cómo se gastaba un juguete, quién lo heredaba, dónde lo guardaba un niño), no sobre datos de fábrica ni ángulo industrial frío. Las marcas y los productos solo aparecen dentro del uso cotidiano y de la confianza que las familias les tenían.

---

## 5. Sistema de investigación

### 5.1 Regla permanente (orden de Luis Carlos, 2026-10-25)

Para CADA tema de La Chiva del Pasado, usar SIEMPRE los mismos 3 prompts de Gemini Deep Research adaptados al tema — (1) investigación, (2) audiencia (comentarios públicos) y (3) anécdotas (primera persona, cita textual + fuente) — con las reglas de honestidad intactas (nada inventado, «sin confirmar» lo no verificado, enlaces). La investigación propia corre en paralelo y se cruza con los informes, nunca los reemplaza. Skill: `~/workspace/custom-skills/gemini_deep_research_prompts/SKILL.md`.

Cómo adaptar cada prompt: reemplazar el título del video, el número de ítems, la lista inicial de ítems y la ventana de época por los del tema nuevo; reemplazar los momentos buscados en el prompt de anécdotas por los momentos propios de cada ítem nuevo; conservar intactos los lugares donde escuchar, las tareas numeradas, el formato de entrega y las reglas de honestidad; conservar la variable principal del prompt de investigación (la fuerza del recuerdo vivido, no la historia empresarial); mantener el idioma en español y la exigencia de enlaces en todas las afirmaciones importantes.

Reglas que nunca cambian: adapta el tema y conserva la estructura; exige fuentes con enlaces y marca «sin confirmar» lo no verificado; separa lo que dicen los medios de lo que dice la gente; entrega los informes en español y guárdalos junto al tema en la carpeta del video.

### 5.2 Prompt 1: Investigación — VERBATIM

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

### 5.3 Prompt 2: Audiencia — VERBATIM

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

### 5.4 Prompt 3: Anécdotas — VERBATIM

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

### 5.5 Investigación propia con la API de YouTube (corre en paralelo y se cruza)

- **Conector:** `custom.youtube-data-api` (YouTube Data API v3, API key registrada; solo lectura de datos públicos; hosts `www.googleapis.com`, `youtube.googleapis.com`; nunca poner la clave en un documento, helper, argumento, variable de entorno o log; nunca pedirle una clave al usuario en chat). Helpers en `~/workspace/custom-connectors/custom.youtube-data-api/bin/`, ejecutar con `python3` (el ejecutable directo da Permission denied).
- **`youtube_channel.py`:** resuelve un canal por handle (`channels.list` con `forHandle`), lee sus estadísticas públicas y trae sus videos subidos (título, fecha, duración, vistas, likes, comentarios, URL de miniatura). Uso: `python3 ~/workspace/custom-connectors/custom.youtube-data-api/bin/youtube_channel.py --handle @CuandoMexicoFabricabadeTodo --max-videos 200 --out <ruta.json>`. Paginación con `nextPageToken` en páginas de 50; detalles de video en lotes de 50 ids. Verificado 2026-10-15 contra `@CuandoMexicoFabricabadeTodo` (ID `UCtWtk6_Ph2EoHamCiI00lSg`, 29 videos). Un `items` vacío en la búsqueda del canal = el handle no resolvió: revisar la ortografía antes de reintentar. Un 403 con motivo de cuota = cuota diaria del proyecto de Google Cloud agotada: parar y esperar el reseteo, no reintentar en bucle.
- **`youtube_comments.py`:** `search.list` (100 unidades de cuota cada una) para encontrar videos, luego `commentThreads.list` (1 unidad cada una) para los comentarios de primer nivel por relevancia. Argumentos: `--query` (repetible), `--max-videos-per-query` (por defecto 5), `--max-comments-per-video` (por defecto 15), `--out` (JSON). Búsquedas con `regionCode=CO` y `relevanceLanguage=es`. El JSON guarda por video: videoId, título, canal, fecha, `foundBy` (qué búsquedas lo encontraron), comentarios (autor, texto, fecha, likes, respuestas) y `commentsError` si falló. Preferir lecturas por playlist antes que búsquedas (una búsqueda cuesta 100 unidades; listar un canal y sus videos cuesta pocas unidades por llamada).
- **Cuota:** la API v3 tiene cuota diaria en unidades. En los barridos reales se gastaron ~630 unidades (6 búsquedas + 28 commentThreads + enriquecimiento), ~1.052 (10 + 49), ~1.064 (10 + 60) y ~2.653 (25 + 150). Sin errores 429 en las rondas documentadas.

### 5.6 Criterio final de elección de temas (fijado por Luis Carlos, prioridad máxima)

**Mandan los COMENTARIOS del público colombiano, anclados a su video; las vistas solo ponderan, sin filtro de tamaño de canal.** El ranking se ordena por lo que el público pide en los comentarios: peticiones explícitas («hagan un video de…», «falta un video de…», «nadie habla de…», «¿por qué no hacen…?»), los «faltó…» (qué echan en falta en las listas), temas que la audiencia colombiana pide una y otra vez en videos distintos, y recuerdos que comparten pidiendo que se rescaten. Las vistas solo ponderan, no ordenan: un tema con muchas vistas pero sin comentarios pidiendo nada pesa MENOS que un tema con menos vistas pero con comentarios colombianos pidiendo ese contenido. Sin filtro de tamaño: canales grandes y pequeños cuentan por igual, siempre que la audiencia sea colombiana adulta (35–65+), verificada por lo que dicen los comentarios, no por el canal. Un video con muchas vistas pero audiencia de otro país NO cuenta como demanda colombiana.

**Ranking vigente por demanda de comentarios** (informe `~/workspace/nostalgia_colombia/informe_temas_virales_colombia.md`; acumulado: 51 búsquedas, 279 videos únicos, ~3.390 lecturas de comentarios; datos crudos en `~/workspace/nostalgia_colombia/barrido_amplio/`):

1. **MÚSICA** — hecho (video publicado 2026-11-05). Sin reproducir canciones, sin repetir a Darío Gómez como ítem; jingles Bienestar Familiar y Olímpica por verificar contra Comerciales.
2. **CIUDADES QUE DESAPARECIERON**, primero BOGOTÁ («12 COSAS de BOGOTÁ que Desaparecieron con el Tiempo», «¡ASÍ ERA BOGOTÁ!») — **RECHAZADO por Luis Carlos el 2026-11-05: «no vamos a hacer ciudades».** No se produce, pese a la evidencia de demanda.
3. **DICHOS** — apuesta más segura, cero derechos. Título: «12 DICHOS Colombianos que Decían Nuestros Abuelos y Quedaron en el Olvido», miniatura «¡ASÍ DECÍA MI ABUELO!».
4. **RADIO** — sin reproducir audio con derechos. Título propuesto: «12 VOCES Y EMISORAS Colombianas que Todos Oíamos en la Radio y Quedaron en el Olvido», miniatura «¡ASÍ SONABA LA RADIO!».
5. **TV programadoras e IDs** — no duplica Series ni Comerciales. Título propuesto: «12 IDS Y PROGRAMADORAS de la Televisión Colombiana que Todos Veíamos y Quedaron en el Olvido», miniatura «¡ASÍ EMPEZABA LA TV!».
6. **PELÍCULAS** — solo ventana 1970–2000. Título propuesto: «12 PELÍCULAS Colombianas que Veíamos Todos en Familia y Quedaron en el Olvido», miniatura «¡TODOS LAS VIMOS!».
7. **REMEDIOS** — anclar a Colombia, ángulo recuerdo, no consejo médico. Título propuesto: «12 REMEDIOS de la Abuela que Nos Curaban Todo y Quedaron en el Olvido», miniatura «¡ASÍ NOS CURABA LA ABUELA!».
8. **FÚTBOL 90** — señal reforzada, no recomendación (emoción enorme, cero peticiones explícitas de video-lista).
9. **REINADO** — señal con conflicto de regla: choca con «nada de listas de famosos» vigente tras Famosos; no es recomendación limpia salvo decisión expresa de Luis Carlos o enfoque en el ritual (no en un ranking de mujeres).

Temas descartados con motivo (no reabrir sin evidencia nueva): comerciales (ya hecho); actrices de los 80/90 (lista de famosos, prohibida); cuentos / Rafael Pombo (gigante toycantando dominando, comentarios desactivados, audiencia infantil); moda de los 80 (genérica internacional, sin señal colombiana); programas concurso de TV (familia Televisión ya tocada, queda en reserva); Bogotá de los 80 en general (geográfico, no lista de 10–12; queda como evidencia de nostalgia urbana); merengue clásico 80/90 (audiencia venezolana/dominicana, no colombiana); juegos de barrio (se solapa con Juguetes); objetos de los 80 (mismo territorio que Electrodomésticos y Marcas); comida callejera actual (no es «de antes»); programas infantiles (gigantes infantiles, TV peruana); fiestas de pueblo (sin señal).

### 5.7 Prompt de búsqueda de anécdotas vividas (API de YouTube) — VERBATIM

Fuente: `~/workspace/nostalgia_colombia/prompt_busqueda_comentarios_nostalgicos.md`. Aprobado y ejecutado dos veces.

```
# Prompt — Búsqueda mejorada de comentarios nostálgicos en YouTube (La Chiva del Pasado)

Úsalo para buscar en la mayor cantidad posible de videos, con la API de YouTube, comentarios nostálgicos sobre el tema de cada video.

## Objetivo

Encontrar comentarios que sean recuerdos vividos reales: emocionales, humanos, con anécdotas que solo alguien que vivió esa Colombia puede contar. No buscamos opiniones sobre nostalgia en general: buscamos escenas de vida.

## Muestra

Lo más amplia posible. Búsquedas por década (70, 80, 90), por ciudad (Cali, Medellín, Bogotá, Barranquilla, Eje Cafetero, Cartagena, Bucaramanga), por ámbito de vida (colegio, barrio, familia, cocina, transporte, trabajo, iglesia, fiestas, radio, TV, música, deportes, humor, mercado, campo) y por formato (te acuerdas, así era, cosas que ya no existen, antes vs ahora, cuando éramos niños en Colombia). Sin filtro de tamaño de canal: valen canales grandes y pequeños. En cada video, lee los comentarios principales por relevancia y profundiza en los videos con más conversación.

## Qué seleccionar: la prueba de la anécdota vivida

Un comentario vale si cumple al menos tres de estas señales:

- Primera persona y escena en movimiento: cuenta algo que PASÓ (yo, mi mamá, en mi casa, mi abuelo), no solo opina que antes era mejor.
- Detalles concretos y sensoriales que solo un testigo tendría: olores, sonidos, sabores, texturas, el barrio o la ciudad exacta, la tienda, la emisora, el objeto con su marca o modelo, la rutina (la hora del día, el día de la semana), precios o monedas de la época, frases que se decían en la casa.
- Emoción humana pequeña y concreta: risa, llanto, vergüenza, orgullo, miedo, ternura. Nada de discurso grandilocuente.
- Anclaje colombiano y de época (1970–2000): el detalle solo tiene sentido en la Colombia de antes.
- Que el comentario responda al tema del video: el recuerdo debe ser sobre lo que el video muestra, no un tema suelto.

## Qué excluir, sin excepción

- Genéricos sin escena: qué nostalgia, tiempos aquellos, todo era mejor, like si eres de esa época, solo emojis.
- Opiniones sobre el video, el canal o el youtuber.
- Peleas, política, autopromoción, spam y comentarios que suenan a bot.
- Anécdotas de otros países sin ancla colombiana.
- Datos fríos sin escena (fechas y cifras copiadas, sin recuerdo vivido).
- Nada de narcos, nada de listas de famosos, nada de política como tema.

## Qué extraer por cada comentario

- Cita textual exacta, sin pulir ni inventar nada, con sus likes.
- Video donde apareció: título, ID y tema del video.
- El detalle vivido que lo valida (qué micro-detalle demuestra que quien escribe lo vivió).
- A qué posible parada o tema del canal alimenta ese recuerdo.

## Cómo organizar el resultado

- Por tema de video: qué temas provocan más anécdotas y qué piden en cada uno.
- Ranking de temas por cantidad y calidad de anécdotas, no por vistas.
- Lista de las mejores anécdotas, cada una anclada a su video.
- Si un comentario parece inventado o dudoso, marcarlo como dudoso, nunca presentarlo como recuerdo verificado.
- No atribuir a Colombia lo que no tiene ancla colombiana.
```

### 5.8 Regla de fuentes de la investigación

La PRIMERA fuente es todo lo ya aprendido de Luis Carlos (su voz, sus reglas, sus criterios y el segundo cerebro de El Taller del Creador); también se puede ver la competencia, pero SIEMPRE prima lo aprendido de él. En conflicto, manda lo suyo, no lo del competidor. La investigación propia (API) corre en paralelo con los 3 informes de Gemini y se cruza con ellos en un informe de cruce (`informe_cruce_api_gemini.md` junto a cada tema); nunca reemplaza a los informes. Guardar los informes en español junto al tema en la carpeta del video. Los informes de Gemini quedan enlazados (sesión Pro; Deep Research puede bloquearse por cuota — en Tragedias se bloqueó durante el Prompt 3 y se desbloqueaba el 2026-11-05 14:39).

### 5.9 Transcripción de podcasts y videos de YouTube para humanizar los guiones (método 2026-11-06)

Para los guiones también se transcriben videos de YouTube de podcasts nostálgicos colombianos (audio descargado y transcrito en local). **Spotify NO permite bajar el audio directamente** (cifrado), aunque la mayoría de esos podcasts también está en YouTube.

- **Descarga del audio:** `yt-dlp` cae en el bot check de YouTube; se pasa con `--extractor-args "youtube:player_client=android"`. Comando tipo: `yt-dlp --extractor-args "youtube:player_client=android" -x --audio-format mp3 --audio-quality 0 <url>`. Las descargas pueden caer al formato 18 (360p, SABR) y ser lentas, pero completan.
- **Transcripción (método por defecto desde 2026-11-06): Groq Whisper large-v3** vía el conector `custom.groq`, helper `~/workspace/custom-connectors/custom.groq/bin/transcribe.py`: `python3 transcribe.py INPUT --out palabras.json --model whisper-large-v3 --language es`. Parte audio >25 MB en chunks WAV 16 kHz mono de 480 s con ffmpeg; exige User-Agent estilo navegador (Groq devuelve 403 sin él; no quitar el header). **~46 min de audio ≈ 1 minuto** (vs ~11 min para 18 min de audio en CPU local con faster-whisper).
- **Uso:** los transcripts se minan para humanizar los guiones (lenguaje, ritmo, escenas, dispositivos orales) y para sacar anécdotas; NADA de lo minado toca la lista de ítems (la lista manda por comentarios, §5.6). Archivos por podcast en `video_<tema>/podcasts/` (mp3 + `*_palabras.json` + `*_transcripcion.txt` + minas). Referencia Dichos (2026-11-06): Triste Realidad cap. 14 «LA NOSTALGIA» (8.847 palabras) y cap. 13 «LA COMIDA» (9.170 palabras); 4 podcasts de dichos (12.671 palabras); 3 podcasts grandes solo para humanización (24.869 palabras: Monólogos sin Propina, LOS40 +DE 40 cap. 13, TODELAR). Los remedios peligrosos mencionados se registran solo como memoria, nunca como consejo; las groserías y el humor de pareja NO se copian (el canal es familiar); TODELAR es documental narrado, no registro oral.
- **Lección de verificación (2026-11-06):** una frase puede venir de un COMENTARIO y no del audio del podcast: «come hijita hasta que brille el pupo» NO está en el cap. 13 ni en el 14 (verificado palabra por palabra en ambas transcripciones); el informe API lo citaba de un comentario. Verificar siempre si la cita es del audio o de un comentario antes de atribuirla.

---

## 6. Sistema de guion

### 6.1 Formato aprobado

- **Formato general: 10 ítems.** Excepciones aprobadas con 12 ítems: Marcas, Dulces, Navidad, Bebidas, Viajes, Música, Famosos, Tragedias. (El formato general es 10; el 12 se aprueba caso por caso.)
- **Cada parada = exactamente 11 párrafos cortos.** Nunca líneas sueltas numeradas. Contar los párrafos por parada y en total con `muse.exec` antes de entregar (un guion de 12 paradas tiene 132 párrafos de parada más apertura, LLAMADO y cierre).
- **Voz:** primera persona del plural, la voz de la audiencia recordando, con nombres y expresiones de la época. Escenas desde adentro, primera persona, emoción por delante, datos escondidos en el recuerdo. Nada de fechas ni de datos fríos: si aparecen, van dentro de la acción, nunca como información.
- **Estructura:** apertura oficial «Súbete, que nos vamos al pasado» (salvo orden contraria por guion, como en Comerciales y Viajes, que no la llevan); paradas en cuenta regresiva (la parada N es la primera que se muestra, de reconocimiento inmediato para enganchar en el primer minuto; la parada 1 es la de mayor carga nostálgica nacional); **sección LLAMADO tras la parada 7** (el "suscríbete" a mitad del video, sección propia para que no se mezcle con la parada anterior); cierre con invitación a la lista de reproducción y a comentar.
- **Cada parada se construye sobre microdetalles vividos de uso** (cómo se gastaba un juguete, quién lo heredaba, dónde lo guardaba un niño, quién lo fiaba), no sobre datos de fábrica ni ángulo industrial frío. Las marcas y los productos solo aparecen dentro del uso cotidiano y de la confianza que las familias les tenían.
- **Dichos y agüeros:** presentarlos solo como color recurrente, a través de «El dicho de la ruta» y «El agüero de la parada», y etiquetar los agüeros con el sello CREENCIA POPULAR para que nunca se presenten como hecho verificado ni se les invente un origen.
- **Guion = la plantilla del formato.** Encabezado de cada bloque (Anexo A4 del libro): BLOQUE / PARADA n.º: [nombre] · Categoría: H/T/L/CP (hecho, testimonio, leyenda, creencia popular) · Ficha en pantalla: [fecha, lugar] · Activo visual: [archivo/recreación] · Fuente en pantalla: [fuente corta] · Dicho/agüero de cierre, si aplica: [texto, sin origen atribuido sin fuente].
- **Parar en el guion y esperar aprobación antes de voz o producción.** Si el formato es nuevo, entregar UNA parada como muestra en el formato exacto aprobado antes de escribir el guion completo, para que una corrección de formato cueste un ítem y no el documento entero.
- **La voz NO lee los títulos** INTRO, PARADA o CIERRE: solo sirven para marcar secciones (alineación con difflib; el 97 % de las palabras queda alineado).
- **Cuando Luis Carlos entrega su propio guion verbatim** (Series, Viajes), no se toca: se usa tal cual. Sus datos pendientes de verificar se verifican antes de cualquier reedición, no se corrigen por cuenta propia.
- **Guion sin citas (observación de Luis Carlos, 2026-11-07, para los guiones después de Dichos).** El guion va muy humanizado pero SIN citar nada: sin «según…», sin fuentes ni referencias en el texto. Las anécdotas de la audiencia se tejen como «tal persona cuenta que…», que está bien. Las citas con fuente quedan en los informes de investigación (§5), no en el guion. La descripción de YouTube sí lleva sus créditos, por licencia.

### 6.2 Fórmula de títulos (verificada, sección 19 del libro)

**[NÚMERO] + [CATEGORÍA] + [COLOMBIANO/A(S)] + [que + verbo en pasado] + [cierre de pérdida: con el Tiempo / en el Olvido / Desaparecieron / Quedaron / Se Fueron para Siempre]**

- Nunca años literales. Nunca «?» ni «:» en el título. Longitud 55–99 caracteres, mediana 84. Mayúsculas selectivas: solo 1–3 palabras gancho en mayúsculas; el resto en formato frase; nunca el título entero en mayúsculas. Puntos suspensivos «…» antes de la cláusula final: recurso permitido, no obligatorio. Sufijo «(Parte 2)» solo para secuelas reales de un tema que ya funcionó.
- Matiz confirmado 2026-11-04: para canciones NO usar «Ya Nadie las Recuerda» (falso: la gente sí las recuerda, solo ya no suenan).
- Títulos u opciones para copiar se entregan SIN comillas (preferencia de formato 2026-11-04).

### 6.3 Datos verificados por video (no afirmar lo contrario)

- **Marcas:** «Ley» nunca «El Ley»; Telecom liquidada 2003, no quebró («Nunca estuvo quebrado, era una empresa rentable», lo confirma la audiencia); Chupi Plum es de Quala; Tía cerró 23-11-2017; Conavi 1974, fusión Bancolombia 2005; La 14 nació 1964, liquidación 2021. Por verificar antes de cualquier reedición (feedback de la audiencia): el minuto de Telecom (el video dice $2.000, la audiencia dice $200); Caravana NO fue solo de Medellín (estuvo en Bogotá, San Victorino); Ley pertenecía a Cadenalco (fusión con Éxito 1999/2001); BBVA–Ganadero DUDOSO.
- **Dulces:** Motitas = Cadbury Cali, nunca Canel's; Sapito = importado Arcor Argentina (narrar el matiz); Galletas Cómics: fabricante en conflicto, no afirmar Dosquebradas.
- **Bebidas:** Chubby y Kapo = importados (narrar el matiz); **Frule sin confirmar** (posible confusión con «Frulé» Alpina 2014); Frizz de Alpina FUERA por decisión suya.
- **Platos:** natilla de maíz NO entra (ya fue parada en Navidad); la voz dice «hogado» por error, Hogao estaba bien.
- **Series:** dos datos de Luis Carlos pendientes de verificar antes de cualquier reedición: Café grabada en Filandia, Quindío; conductores de bus en Bogotá subiendo el volumen al radio.
- **Viajes:** pista Herrera = Palonegro VERIFICADA; «último viaje» 13-05-1992 SIN CONFIRMAR (liquidación Decreto 1586 de 1989; fin jurídico 17-07-1992).
- **Electrodomésticos:** único año narrado permitido: 2003; el guion NO afirma ranking de ventas; los que se fabrican hoy en versión moderna se narran como «dejaron de fabricarse ASÍ».
- **Música:** Esperanza = Nelson Ibarra; A Quien Engañas Abuelo = Arnulfo Briceño; Pueblito Viejo = José A. Morales 1954; Soy Colombiano = Rafael Godoy; Cenizas al Viento y Yo También Tuve 20 Años = José A. Morales; Vientos de Navidad = Wilfran Castillo, Los Diablitos 1998; No Quiero Envejecer = Pedro Pablo Peña, Lucho y Rafa 1991; Amo = Arnulfo Briceño. **La Lancha CORRECCIÓN: NO es de Camilo García (solo arreglista); música de Fra Diavolo de Auber (1830), letra emparentada con tango 1928; narrar «versión del Dueto de Antaño, arreglo de Camilo García, melodía de mucho antes». La Enredadera: autor SOLO como atribución («se les atribuye a Luis Ernesto González Correa y a Gonzalo Arias Quiceno»), nunca cerrado. El Regreso: SIN año (disputa 1953 vs década del 60). Amo: SIN año (antes de jun. 1989; ya sonaba en 1991; «1996» NO es año).** Omisiones pedidas en comentarios: El Camino de la Vida, Las Acacias, Espumas.
- **Famosos:** Don Chinche lo interpretó **Héctor Ulloa** (1982–1989), NO Benjumea (el ancla falsa venía de Gemini); la parada 9 se reescribió sin Don Chinche (anclas reales: El taxista millonario, Sabariedades con Pacheco, Yo y tú).
- **Tragedias:** la teoría de Gaviria y el avión de Avianca es teoría en disputa SIN confirmar: tratarla como pregunta abierta, nunca como hecho (el guion la lleva como pregunta en la parada 1); igual la pregunta de Diana Turbay («¿quién ordenó el operativo?»); no glorificar a Escobar (la audiencia lo castiga); separar la serie «El Patrón del Mal» de la realidad (Cano, Galán); no errar datos verificables (la audiencia corrige direcciones: Centro 93 = calle 93 con carrera 15); nada de política actual; respeto, nada morboso. NO meter eventos no narcos (Palacio de Justicia, Mitú, Armero, Jaime Garzón) aunque la audiencia los mezcle. Tensión del título registrada (no veto): «nadie puede olvidar» / «nadie lo olvida» = 0 menciones en 467 comentarios; «inolvidable» = 0. La gente dice «jamás se me olvidará», «no se debe olvidar», «no los olvidamos»; y como queja «Parece que olvidamos esa época» (63 likes). El título se mantiene aprobado; el guion usa las frases reales dentro.

---

## 7. Sistema de voz

### 7.1 Flujo completo (tal como se ejecuta)

1. **Guion aprobado → archivo de bloques.** Se crea `video_<tema>/bloques_voz_<tema>.md` con los bloques VERBATIM del guion, en orden de locución. **15 bloques:** 01 Apertura, 02–07 Paradas 12–7, 08 LLAMADO, 09–14 Paradas 6–1, 15 Cierre. Los títulos de bloque («## Bloque 01 — Apertura», etc.) y el encabezado del archivo NO se locutan: son etiquetas y metadatos, no texto de narración. No cambiar ni una palabra ni una coma del guion.
2. **Generación en Google AI Studio, sesión luisayaka87@gmail.com** (si pide login, él lo completa en vivo; la contraseña guardada puede estar desactualizada — ver regla 13 de §2; nunca pedirle la contraseña en chat). Un WAV por bloque, en orden.
3. **Voz y ajustes (IDÉNTICOS en los 15 bloques):**
   - Voz: **Cruz** (Speaker 1, de Favoritos).
   - Style (verbatim, igual en cada bloque): **«acento colombiano del Valle del Cauca/Cali muy marcado, entonación cantarina y musical, vocales ligeramente alargadas, ritmo relajado y cálido, como un tío caleño contando en familia. Nada de acento neutro de doblaje, ni mexicano, ni paisa, ni costeño.»**
   - Expression: vacío.
   - Temperatura: 1.
   - Modelo: Gemini 3.8 Flash TTS (en AI Studio).
4. **Nombres de archivo (patrón por video):** `01_apertura.wav`, `02_parada12_<item>.wav`, `03_parada11_<item>.wav`, `04_parada10_<item>.wav`, `05_parada09_<item>.wav`, `06_parada08_<item>.wav`, `07_parada07_<item>.wav`, `08_llamado.wav`, `09_parada06_<item>.wav`, `10_parada05_<item>.wav`, `11_parada04_<item>.wav`, `12_parada03_<item>.wav`, `13_parada02_<item>.wav`, `14_parada01_<item>.wav`, `15_cierre.wav`. Carpeta: `video_<tema>/voz/`.
5. **Unión:** `ffmpeg -f concat -safe 0 -i concat_list.txt -c copy voz_<tema>.wav` (lista `file '<nombre>.wav'` por bloque, en orden). Verificar la duración de cada bloque con `ffprobe` y la suma total; no fiarse de los segundos redondeados del reproductor de AI Studio.
6. **Procesamiento (línea procesada oficial — de aquí derivan TODAS las temporizaciones SRT/EDL, nunca del audio crudo):** se ejecuta el procedimiento de `src/voz.ps1` (ver §7.2). En Linux los `.ps1` no corren, pero los `.py` sí: replicar los mismos pasos en bash (pausas.py + resample + loudnorm de dos pasadas).
7. **Medir y verificar la línea procesada:** duración total (debe quedar 17–20 min), loudness (medir con loudnorm: objetivo −14/−15 LUFS, LRA ~3), pausas >0,9 s (deben ser 0; detectar con `silencedetect=n=-40dB:d=0.9`), ritmo en palabras/s (meta 2,9–3,8; con pausas naturales sale ~3,1). Si queda una pausa >0,9 s (suele ser una pausa de frontera entre bloques que en el crudo estaba justo bajo el umbral), volver a pasar `pausas.py` sobre la línea final y repetir el loudnorm.
8. **Aprobación de la voz por Luis Carlos** antes de producir el video (en Música: «PERFECTO»). Sin su aprobación no se produce el video. Si pide re-grabar un bloque, se re-graba solo ese bloque (mismos ajustes) y se repite la unión y el procesamiento.
9. **Archivo final:** `video_<tema>/voz/voz_<tema>_final.wav` (48 kHz, mono, 16-bit). Guardar también los 15 bloques y el WAV unido sin procesar (`voz_<tema>.wav`) en la misma carpeta.

### 7.2 Procesamiento exacto (src/pausas.py + src/voz.ps1)

**`src/pausas.py`** (Python, numpy; entrada mono 16-bit): acorta SOLO las pausas largas. Detecta silencios con `ffmpeg silencedetect=n=-40dB:d=<LARGA>`; cada silencio de más de LARGA segundos queda en DEJAR segundos; los demás no se tocan. Uso: `python src/pausas.py audio/original.wav audio/sin_silencios.wav [LARGA] [DEJAR]`. **Parámetros vigentes: LARGA = 0.8, DEJAR = 0.5** (desde el 2026-10-27; antes se quitaba toda pausa de más de 0,15 s y la voz quedaba atropellada). Imprime: `N pausas acortadas: X s -> Y s`. Ejemplo real (Tragedias): 52 pausas acortadas, 1.083,0 s → 1.057,0 s.

**`src/voz.ps1`** (PowerShell; en Linux replicar en bash paso a paso):
1. Copia la entrada a `audio/original.wav`.
2. `python src/pausas.py original.wav pausas.wav 0.8 0.5`
3. `ffmpeg -v error -y -i pausas.wav -ar 48000 sin_silencios.wav`
4. Loudnorm de dos pasadas con el filtro: `acompressor=threshold=-24dB:ratio=3:attack=5:release=80:makeup=2,loudnorm=I=-14:TP=-1.5:LRA=4`
   - Primera pasada: `ffmpeg -hide_banner -i sin_silencios.wav -af "<filtro>:print_format=json" -f null -` → extraer del JSON los valores `input_i`, `input_tp`, `input_lra`, `input_thresh`, `target_offset`.
   - Segunda pasada: `ffmpeg -v error -y -i sin_silencios.wav -af "<filtro>:measured_I=...:measured_TP=...:measured_LRA=...:measured_thresh=...:offset=...:linear=true" -ar 48000 voz_final.wav`
5. `ffprobe` de la duración de `voz_final.wav`.

**Metas de la voz (REGLAS_DURAS):** −16 a −13 LUFS, ninguna pausa >0,9 s (las de más de 0,8 s se dejan en 0,5 s); velocidad 2,9–3,8 palabras/s. **PROHIBIDO acelerar el audio** (atempo o similar): se usa la voz tal como sale del procesamiento, que solo acorta los silencios largos. (El v6 aceleró la voz un 13 % — 12:16 en vez de 13:52 — y fue rechazado.)

### 7.3 Duración y ritmo (números medidos)

- Ritmo nominal de guion: 210 ppm. Ritmo real de la voz Cruz procesada: **183–201 ppm** (medido por video: Famosos 190,5; Platos 183,9; Electrodomésticos 185,2; Música 185,0; Tragedias 196). Por eso la meta de guion para 17–20 min es ~3.417–3.600 palabras.
- Ejemplos reales: Música 3.556 palabras → voz unida 1.153,08 s = 19:13, video 18:53; Tragedias narración 3.454 palabras → voz cruda unida 1.083,0 s = 18:03 → procesada 1.056,0 s = 17:36, −14,17 LUFS, TP −0,85, LRA 2,40, 0 pausas >0,9 s.
- La duración del video es la duración de la voz procesada. La condición de Luis Carlos («siempre que complete los 17 a 20 minutos») se verifica con la duración REAL de la voz unida y procesada, no con la estimación.

---

## 8. Sistema de video (pipeline canónico)

### 8.1 Repo y orden de lectura obligatorio

- **Repo:** `~/workspace/nostalgia_colombia/documental-expediente/` (remoto GitHub `luiscarlosayalasilva2-rgb/documental-expediente.git`). **Antes de trabajar: `git pull`.** Después leer `docs/NOVEDADES.md` de arriba hacia abajo hasta la última versión ya aplicada (cada entrada dice qué cambió y qué hay que corregir en un video en curso). Nunca MP4 a GitHub. Nunca constructores ad hoc.
- **Orden de lectura antes de tocar nada:** 1) `docs/REGLAS_DURAS.md` (obligatorio: metas medibles, fotos de referencia, lo PROHIBIDO) y `docs/CATALOGO_DETALLES.md` (TODOS los detalles de la edición con su animación, frecuencia y cómo ponerlos en el EDL); 2) `README.md` (receta paso a paso y reglas de edición); 3) `docs/IMAGENES_Y_SINCRONIA.md` (cómo elegir cada imagen según lo que se narra y pegarla al segundo del audio); 4) `docs/PROCESO_COMPLETO.md` (errores ya cometidos y cómo se resolvieron); 5) `docs/AUTENTICIDAD_FOTOS.md` (país y marca correctos, sin homónimos, sin dibujos ni comerciales, sin repetir) y `docs/ESTILO_DOCUMENTAL_EXPEDIENTE.md`.
- **PROHIBIDO escribir un editor propio o rediseñar las plantillas.** Se usa `src/render.py` + `src/estilo.py` tal cual; solo cambia el EDL. **PROHIBIDO poner la narración escrita en tarjetas de papel** como relleno (la voz ya la dice; en la versión rechazada eso ocupó el 69 % del video). **PROHIBIDO dejar una imagen o tarjeta quieta** durante muchos segundos. **PROHIBIDO usar frames de comerciales de TV** (Content ID los detecta). **PROHIBIDO imágenes generadas con IA** (dentro del video).
- **Formato:** horizontal 16:9, 1920×1080, 30 fps. Solo voz (sin música). Voz muy comprimida, −14/−15 LUFS, rango de unos 3 LU. Arranca sin portada: el segundo 0 ya es imagen con voz. Cierra seco sobre un plano de abandono, sin pantalla final. **Letrero en los primeros 5 s** (Luis lo pidió para que el espectador sepa de qué va el video): ficha a máquina en el segundo 0,6 que dura 4,6 s, con `"titulo": true` para que el verificador no la cuente como parada (ejemplo: `{"tipo":"file","t":0.6,"dur":4.6,"texto":"Así era la Navidad en Colombia","etiqueta":"Expediente diciembre","titulo":true}`).

### 8.2 Estilo «Documental Expediente» (medido del referente)

- **Ritmo:** un plano cada ~6 s de promedio (entre 3 y 8 s); 96 % cortes secos. Nunca una imagen quieta: video con cámara en mano suave o paneo lento; foto fija con zoom lento hacia adelante o hacia atrás con un pequeño desplazamiento, del 5 al 10 % en todo el plano. Los textos entran exactamente cuando la voz retoma después de una pausa. Los textos **siguen en pantalla aunque cambie el plano de abajo**.
- **Estructura de cada parada (50 s a 1:40):** 1) ficha FILE con el nombre; 2) imágenes del producto o del lugar; 3) fotos de archivo sobre papel, en carrusel o en polaroid; 4) número rojo con un dato; 5) palabra que dice cómo era (CONFIANZA, RITUAL, ORGULLO); 6) la causa de la caída, con planos de competidores o dinero; 7) palabra con la causa (BANCARROTA, ADQUISICIÓN, DEUDAS, FRANQUICIA, el país comprador); 8) plano de abandono (cortina cerrada, anaqueles vacíos, ruinas); 9) tira escrita a máquina con la frase de cierre. Bloque de arranque (~50 s): 6–8 planos de objetos con un número y una palabra que presentan el tema.
- **Paleta y tipografías del motor:** crema del papel #EDE6D6 con cuadrícula tenue #D9D0BC; gris carbón del velo: negro al 60–70 %; rojo de acento #C8302A (números, líneas, chinchetas, franjas); amarillo solo para cinta adhesiva y resaltado #E8C766. Tipografía grande: Bebas Neue u Oswald Bold, condensada y muy gruesa. Tipografía de máquina: Special Elite o Courier Prime. Etiquetas: la misma de máquina en tamaño pequeño, en mayúsculas y con ~4 px de espacio entre letras. El video casi no lleva corrección de color. Las fotos de archivo van en blanco y negro o sepia. Nada de viñeta ni grano.
- **Biblioteca de textos en pantalla (tiempos medidos):** A) **Ficha FILE** (tarjeta crema arriba a la izquierda, cinta amarilla, «FILE» diminuta, nombre a máquina; aparece un 10 % más grande e inclinada y se asienta en 0,12 s; el nombre se escribe a ~22 caracteres por segundo; línea roja se dibuja en 0,5 s; 3–5 s, una por bloque). B) **Número rojo** centrado con etiqueta debajo («AÑO DE COMPRA»); la imagen se oscurece en 0,17 s; 2–3 s, unas 25 veces en 32 min. C) **Palabra gigante** blanca con la frase completa debajo a máquina y línea roja vertical; ~3 s, cada ~60 s. D) **Tira a máquina** abajo al centro, con resaltado amarillo en las palabras clave; se escribe letra por letra; 2–3 s, unas 6 veces. E) **Notas EXHIBIT A/B/C** con chincheta roja; 4–6 s, 2 veces. F1) **Foto sobre papel cuadriculado** con esquinas redondeadas, sombra y pie a máquina; 3–5 s. F2) **Carrusel horizontal**; 3 s por foto. F3) **Polaroids** (caen inclinadas, franja roja con texto); 6–8 s. F4) **Logo con marco punteado**; 3 s. F5) **Comparativa VS**; 4 s. G) Infografía (mapa, línea del metro); ocasional.
- **Transiciones:** corte seco, casi siempre. La hoja de papel entra empujando el video hacia arriba desde abajo y sale también empujada hacia arriba (0,5 s). La imagen se oscurece rápido para dar paso a un número o una palabra. El collage con glitch RGB se usa una sola vez, en una apertura. Algún fundido encadenado muy de vez en cuando. Nada de flashes. Solo hubo un negro de 0,8 s.
- **Errores del original que NO se copian:** frases que se salen del cuadro o quedan cortadas; timecodes quemados del material original; marcas de agua de stock.
- **Estándar de producción del canal (2026-10-22, sistema de edición La Chiva v1):** pulso ~9,4 planos/min en el referente; plano típico ~6 s (71 % entre 5 y 10 s); ítem típico ~57 s; el n.º 1 dura el doble (2:18) como clímax. En La Chiva las paradas van a ~90 s: se mantiene el pulso de plano, no se recorta su forma de contar. Transiciones 91 % corte seco. Material: las fotos cargan el video (73,7 % foto de archivo fija o con Ken Burns discreto; clips y comerciales de época son minoría). Audio del referente: −15 LUFS, LRA 3 LU, ningún silencio ≥0,9 s en 32 min. **Mejoras acordadas con Luis Carlos el 2026-10-22:** ritmo con intención (pulso base ~6 s/plano, planos de 4–5 s en revelaciones y UN plano largo sostenido de 8–12 s por parada sobre la foto más emotiva, dejando caer el epitafio encima); Ken Burns que sigue a la narración (zoom hacia lo que se cuenta; paneo de cara en cara en fotos de grupo); respiro visual corto antes del epitafio; sonido de época con cuentagotas (2–3 por parada, nunca por corte); el 4:3 se viste sobre el papel del sistema, nunca se estira ni se recorta; unificación de color mínima (un solo preset suave y cálido sobre el archivo, sin «restaurar» la pátina); el tipeo con personalidad.

### 8.3 Pipeline paso a paso (receta del README)

| # | Paso | Script / comando |
|---|---|---|
| 1 | Quitar silencios de la voz y normalizar a −14 LUFS | `src/voz.ps1` (ver §7.2; en Linux replicar en bash) |
| 2 | Transcribir con tiempos por palabra | `python src/transcribir.py audio/voz_final.wav audio/palabras.json` (faster-whisper small; se decodifica el audio con ffmpeg y se le pasa a Whisper como array de numpy, porque PyAV no acepta `metadata_errors`) |
| 3 | Alinear el guion con la voz (los títulos INTRO, PARADA N y CIERRE marcan secciones) | `python src/alinear.py guion.txt audio/palabras.json audio/frases.json` (difflib; 97 % de las palabras alineadas). Para una palabra concreta: `src/palabras_en.py` |
| 4 | Bajar material: Pixabay (fotos y video) y Wikimedia Commons | `python src/pixabay.py <carpeta> foto\|video <n> "consulta"…` · `python src/commons.py "consulta"` (clave Pixabay en la variable de entorno `PIXABAY_API_KEY`; se guarda con `src/guardar_clave_pixabay.ps1`) |
| 5 | Bajar fotos de Google Imágenes en tamaño original | `src/receptor.py` (servidor en 127.0.0.1:8765) + `src/lote_google.js` en Chrome (ver §8.4) |
| 6 | Hojas de contacto para elegir | `python src/hoja.py <carpeta> <salida.jpg> "patrón"` — revisar TODAS las fotos con los ojos y elegir solo las que muestran lo que se narra |
| 7 | EDL: planos por frase + capas de texto | `python src/nuevo_video.py plan audio/frases.json audio/palabras.json final/edl_NUEVO.json --etiqueta Parada` → rellenar PENDIENTE y REVISAR → `python src/nuevo_video.py validar final/edl_NUEVO.json` hasta que diga LISTO. No se arma el EDL desde cero ni con otra estructura. Para ajustes finos usar `src/edl_completo.py` como ejemplo de un EDL hecho a mano |
| 8 | Mejorar las fotos de menos de 1000 px | `python src/mejorar_fotos.py final/edl_hd.json media/hd_esrgan` (Real-ESRGAN; ver §8.4) |
| 9 | Encontrar la misma foto en HD (dHash) | `python src/emparejar_hd.py final/edl_completo.json final/mapa_hd.json` |
| 10 | Recortar logos, firmas y marcos | `src/limpiar.py` (diccionario `RECORTES`) |
| 11 | Render 1920×1080 a 30 fps (4 procesos, ~15 min para 14 min de video) | `python src/render.py final/edl_v3.json salida.mp4 --workers 4` |
| 12 | Render + efectos de sonido sintetizados + mezcla con la voz | `powershell -File src\mezclar.ps1 -Edl final\edl_X.json -Salida final\X_FINAL.mp4` (en Linux, ver §8.5) |
| 13 | Miniatura | `python src/miniatura.py` (en la práctica vigente la miniatura oficial se genera en ChatGPT con el prompt maestro, §9) |
| 14 | Subtítulos .srt para YouTube (no van en la imagen) | `python src/generar_srt.py audio/frases.json final/X.srt` |
| 15 | Verificación obligatoria (con EDL) | `python src/verificar.py final/X.mp4 final/edl.json` |

**Antes de armar el EDL, revisar que el audio esté completo:** transcribir los últimos 20 s del original. En el video de Navidad el audio venía cortado y faltaba el cierre. **Antes de renderizar el video completo, revisar el audio contra el guion:** la voz puede saltarse una frase; si falta, se quita del `guion.txt` antes de alinear (pasó con una frase del Renault 4 en Comerciales).

**Formato del EDL (json):**
```json
{"dur": 832.24, "audio": "audio/voz_final.wav",
 "planos": [{"t0":0,"t1":2.8,"tipo":"imagen","src":"…","mov":{"z0":1,"z1":1.07},"bw":false},
            {"t0":…,"tipo":"video","src":"….mp4","ss":1.0},
            {"t0":…,"tipo":"papel","papel":{"modo":"polaroid","fotos":[{"src":"…","pie":"…"}]}}],
 "capas":  [{"tipo":"numero","t":25.0,"dur":2.3,"num":"12","label":"Helados Baloncito","grande":true},
            {"tipo":"file","t":27.35,"dur":4,"texto":"Helados Baloncito","etiqueta":"Parada 12"},
            {"tipo":"palabra","t":…,"dur":2.9,"palabra":"Heredaba","sub":"frase completa"},
            {"tipo":"nota","t":…,"dur":3,"texto":"…","resaltar":["…"]}]}
```

**Reglas de edición (EDL):** un plano por idea narrada; duración media 3,7 s, mínimo 0,6 s, casi nunca más de 7 s; las enumeraciones van en cortes rápidos, uno por cosa, cortando en el segundo de cada palabra; la imagen muestra lo que se dice en ese momento (si se habla de una cifra o una fecha, se ve el lugar o el objeto de la marca); el zoom lento alterna entre acercarse y alejarse (1,0 → 1,07 y 1,07 → 1,0); pasado y pérdida en blanco y negro (`#bw`): cierres, quiebras, «ya no está», «la silla del abuelo quedó vacía»; mezcla de material: alrededor de **1 clip de video cada 6 planos**, unos 35 clips en 14 min (ambientes y acciones); **sin repetir fotos**, salvo en el carrusel de repaso del cierre. **Estructura de cada parada:** 1) `abre(t, N, 'Marca')`: número rojo grande de 2,3 s con el nombre debajo en letras grandes (`grande=True`); luego la ficha FILE «PARADA N», 2,35 s después; 2) fotos de la marca y del contexto, siguiendo la narración; 3) **número rojo** (`numero`, 2,0–2,4 s) en cada año o cifra clave (fundación, cierre, precios, cantidades), en el segundo exacto en que se dice la cifra; 4) **palabra gigante** (`palabra`, 1,7–3,4 s) en la frase emocional más fuerte (más o menos una cada 60 s, y siempre en la frase final de la parada), en mayúsculas, con la frase completa debajo; 5) **nota a máquina** (`nota`) solo para lemas y frases célebres entre comillas («Siempre te da más», «Listo Medellín, cabina 8»), resaltando de 1 a 3 palabras; 6) **escena de papel** (polaroid, foto única o VS), de 6 a 8 s, una o dos por parada (polaroid para comparaciones o tres marcas juntas, VS para rivalidades). **Intro:** cortes rápidos con objetos cotidianos, la palabra clave del tema y un número con el total de ítems. **Cierre:** el número del total, un carrusel con una foto de cada marca y su número, y la palabra final hasta el último segundo. **Textos que se pisan:** dos números o palabras no pueden encimarse; el script lo avisa; si pasa, se acorta el `dur`. **Audio:** voz sin pausas y los efectos sintetizados que genera `src/efectos.py` según las capas del EDL. Sin música.

**Efectos de sonido (src/efectos.py):** sintetiza cada sonido con numpy, sin grabaciones (sin derechos): tecleo de máquina de escribir en las fichas y notas; golpe grave en los números, más profundo en las aperturas; whoosh en las palabras y al entrar el papel; obturador de cámara en las polaroids; especiales: el ¡PLUM! del Chupi Plum, el timbre de teléfono, el clac de la cinta VHS y las monedas. Desde el EDL: `"especiales": [{"t": seg, "sonido": "plum|timbre|vhs|moneda"}]`; sin esa clave usa los del video de referencia. Niveles medidos con `src/niveles.py`: todos los efectos quedan por debajo de la voz, entre −2 y −24 dB.

### 8.4 Material visual: búsqueda, autenticidad y HD

- **Regla de búsqueda:** una búsqueda por cada cosa concreta que se narra (unas 10 fotos por ítem), con el nombre de la marca más el objeto, el lugar o la época. **Antes de buscar, escribir la tabla de homónimos de las marcas del guion** (Casa Ley de México, Tía de Ecuador, CONAVI de México, etc.).
- **Fuentes, en orden:** 1) Wikimedia Commons (fotos libres; en Marcas solo había fotos libres de 6 de las 12 marcas); 2) Pixabay (sirve para lo genérico; no tiene las marcas colombianas; fotos y clips); 3) Flickr (licencias libres verificadas); 4) Google Imágenes en tamaño original (ver abajo); 5) redes sociales y foros — **por defecto con todos los derechos reservados: solo sirven para localizar el original o pedir permiso, nunca entran sin licencia libre verificada o permiso**. Nada de agencias, marcas de agua ni comerciales de TV. Las fotos van transformadas, en ficha o polaroid. Créditos: no se ponen en pantalla; solo se guardan internamente en `fuentes.tsv` (y en la descripción según §10).
- **Autenticidad (docs/AUTENTICIDAD_FOTOS.md, 6 filtros):** país correcto; marca correcta (sin homónimos); nada de dibujos ni juguetes; nada de comerciales ni afiches; que corresponda a la voz; sin repetir. **Errores reales que no se repiten (v7):** Casa Ley de México en lugar de Almacenes Ley; el Tía de Ecuador en lugar del de Bogotá; el logo de la CONAVI mexicana en lugar del banco Conavi; una abeja dibujada en lugar de la abejita de Conavi; un juguete de pato; frames de comerciales con marca de agua (Chupi Plum); el afiche de la hormiguita de Telecom; relleno sin relación (un tenis en La 14, otra cerveza «El León» en Leona); fotos repetidas de 3 a 4 veces. Fuentes de Argentina, Perú o México en fotos «genéricas» de televisores o salas también se descartan (salen con letreros como «Archivo TV Cine Piura Perú»). **Nunca Ecuador.**
- **Revisión obligatoria:** `python src/revisar_fotos.py final/edl.json` — hojas de contacto por parada, avisos automáticos (repetidas, baja resolución, fuente de otro país) y una planilla que hay que marcar foto por foto en `final/revision/REVISION.md`. **El verificador no aprueba si la planilla no está toda en OK.** Las repetidas se detectan comparando la imagen (doble dHash), aunque tengan otro nombre, estén en blanco y negro o coloreadas. No contar las repetidas por nombre de archivo: se cuentan comparando las imágenes.
- **Google Imágenes en tamaño original (Claude in Chrome):** 1) arranca el receptor: `$env:RECEPTOR_DIR='google_hd'; python src/receptor.py` (servidor local en 127.0.0.1:8765 que recibe las fotos por POST; Luis debe darle **Permitir** al aviso de red local en Chrome); 2) en Chrome, busca en Google Imágenes con `&udm=2&tbs=isz:l` (tamaño grande); 3) pega el contenido de `src/lote_google.js` en la pestaña y llama a `loteHD('prefijo', n, anchoMin, proporciónMin)` (si lo guardas en `localStorage.loteHD`, las demás pestañas de google.com lo reutilizan con `eval(localStorage.loteHD)`). Cómo funciona `loteHD`: la URL original y el tamaño de cada foto están en los `<script>` de la página, con el formato `["url",alto,ancho]` justo después del `data-docid` del resultado; Facebook e Instagram (`lookaside.*`) solo entregan la imagen si se pide como **Googlebot** (eso lo hace `receptor.py`); se pueden usar 4 o 5 pestañas en paralelo (con más, Google se pone lento). No usar vistas previas pequeñas (400–700 px): en 1080p se ven pixeladas.
- **HD:** `src/emparejar_hd.py` busca la misma foto en HD con dHash (con filtro por parada y firma fina para evitar falsos positivos); `src/aplicar_hd.py` aplica los cambios; `src/mejorar_fotos.py` (Real-ESRGAN, modelo `realesrgan-x4plus`): **siempre con `-t 64`**, porque si no la Intel UHD da imagen negra; tarda ~35 s por foto. **Fallo corregido:** cuando Real-ESRGAN fallaba con una foto, se guardaba la imagen de la foto anterior; ahora cada foto usa su propio archivo temporal y se comprueba que la salida se parezca a la original (comparar cada foto de `media/hd_esrgan/` con su original; si alguna no coincide, borrarla y volver a correr `mejorar_fotos.py`). `src/limpiar.py`: recortes para quitar créditos («FOTO: …»), títulos de publicaciones y marcas de tiendas.
- **Reglas de material del canal (Luis Carlos):** solo imágenes/videos reales de Colombia, sin derechos de autor y utilizables en YouTube, que claven exactamente con la ESCENA narrada en ese segundo (el contexto manda sobre la palabra suelta). Nunca relleno extranjero, genérico de bancos ni IA presentada como foto real. Sin material exacto: foto colombiana exacta, sostener plano anterior, ficha breve o hueco declarado. Más fotos que vídeos; los vídeos son CORTOS (si uno largo sirve, solo el fragmento importante, con minutos y segundos). Sin repetir fotos salvo carrusel final. Sin créditos ni marcas de agua en pantalla. **Aunque el tema sean comerciales, NO se usan frames de comerciales** (Luis eligió «Sin comerciales» por Content ID; se muestran empaques, productos y personas reales; en Google salen frames de Frutiño con Higuita y del granito de Águila Roja: no sirven). Si a una sección le faltan fotos, se alarga el plano anterior, pero **nunca una escena de papel** (eso dejó un papel de 23 s en la primera pasada de Comerciales) y se avisa. **Solo se usan notas a máquina en lemas entre «comillas angulares»**; si el guion usa comillas rectas, las notas se agregan a mano.

### 8.5 Render, mezcla y verificación

- **Render en tramos (regla de la VM):** renderizar en tramos de 1200 fotogramas (40 s) y unir al final, para no morir por falta de memoria a mitad del render (VM: 7,7 GB RAM, sin swap). En el repo el render usa 4 procesos con ffmpeg y `veryfast` (`python src/render.py final/edl.json salida.mp4 --workers 4`; 24 s tardaron 47 s; ~15 min para 14 min de video). Los mensajes de «Broken pipe» al cerrar los clips son normales. Siempre con el cargador conectado (la laptop se suspendió por batería a las 2:28 a. m. y el render se cayó) y con `request_keep_awake` si aplica.
- **Mezcla (mezclar.ps1; en Linux los mismos pasos):**
```bash
python src/render.py final/edl.json final/_sin_audio.mp4 --workers 4
python src/efectos.py final/edl.json audio/efectos.wav
ffmpeg -y -i final/_sin_audio.mp4 -i audio/voz_final.wav -i audio/efectos.wav -filter_complex "[1:a]aresample=48000[v];[2:a]aresample=48000[e];[v][e]amix=inputs=2:normalize=0:duration=first,alimiter=limit=0.89:level=false[a]" -map 0:v -map "[a]" -c:v copy -c:a aac -b:a 192k final/VIDEO_FINAL.mp4
python src/verificar.py final/VIDEO_FINAL.mp4 final/edl.json
```
- **Subtítulos (SRT):** en la imagen NO van subtítulos (igual que en el video de referencia). Para YouTube se entrega un `.srt` aparte, generado del guion con los tiempos de la voz: `python src/generar_srt.py audio/frases.json final/VIDEO.srt`. Las líneas tienen máximo 42 caracteres, máximo 2 por subtítulo, y cada subtítulo dura entre 1 y 7 s. Se sube en YouTube Studio → Subtítulos → Subir archivo. **Todas las temporizaciones (SRT/EDL) derivan de la línea de voz PROCESADA, nunca del audio crudo** (en Electrodomésticos la deriva fue de +30,47 s por usar los tiempos crudos).
- **Verificación obligatoria:** `python src/verificar.py final/VIDEO_FINAL.mp4 final/edl.json`. **Si el verificador dice NO APROBADO, el video no se entrega**: se corrige y se vuelve a medir. El EDL (json) se entrega SIEMPRE junto al video; sin él, el verificador no aprueba. Después de corregir: autoanálisis con las reglas del repo en ciclo hasta APROBADO o hasta demostrar con búsqueda seria que ese material no existe; solo entonces se entrega con la falla declarada, su causa y lo intentado, sin inventar nada para pasar. Revisar la hoja de fotogramas cada 8 s y buscar negros con `blackdetect`.

**Metas medidas (verificar.py) — tabla completa:**

| Medida | Meta | Video aprobado (Marcas v4) |
|---|---|---|
| Texto en papel en pantalla | ≤ 15 % | 6 % |
| Cortes por minuto | ≥ 12 | 13,7 |
| Plano más largo (EDL) | ≤ 11 s | 10,3 s |
| Tramo sin corte visible | ≤ 30 s | 28,5 s* |
| Números o palabras gigantes (fondo oscurecido) | ≥ 3 por minuto | 3,5 |
| Clips de video real | ≥ 25 por cada 14 min | 35 |
| Fotos repetidas (sin contar el carrusel del cierre) | 0 | 0 |
| Aperturas numeradas (número grande + nombre) | 1 por ítem | 12 de 12 |
| Números rojos de cifras (años, precios) | ≥ 1 por ítem | 24 |
| Palabras gigantes | ≥ 1 cada 1,5 min | 24 |
| Notas a máquina (lemas entre comillas) | ≥ 1 cada 2 ítems | 11 |
| Voz: volumen y pausas | −16 a −13 LUFS, ninguna pausa > 0,9 s | −15,4 / 0 |
| Velocidad de la voz (no acelerada) | 2,9 a 3,8 palabras/s (con pausas naturales sale ~3,1) | ~3,6 |
| Imágenes distintas por parada | ≥ 1 cada 6 s en cada parada | 10 a 18 por parada |
| Aperturas numeradas | antes de cada ficha | 12 de 12 |
| Cierre | carrusel + palabra final | sí |
| EDL entregado | obligatorio | sí |

\*Son fotos en blanco y negro muy parecidas, en las que el detector no ve el corte. La duración real de cada plano la da el EDL.

**Errores de versiones rechazadas que no se repiten:** v4 (69 % del video con la narración escrita en tarjetas y un editor propio; sin la mitad de los recursos) → REGLAS_DURAS.md y verificar.py. v6 (una sola foto por parada: la misma imagen duró 50, 70, 80 y hasta 114 s, 3 cortes por minuto; fotos que no corresponden —en la parada del Chupi Plum nunca salió un Chupi Plum; la apertura de Conavi salió sobre la foto del Ley—; aperturas numeradas incompletas, solo 5 de 12; voz acelerada un 13 %; sin video real; sin cierre; afiches y frames de comerciales; no entregó el EDL) → CATALOGO_DETALLES.md, más controles, generar_srt.py. v7 (edición bien, fotos de otro país, dibujos genéricos, frames de comerciales con marca de agua, relleno sin relación, fotos repetidas, no entregó el EDL) → AUTENTICIDAD_FOTOS.md y revisar_fotos.py. **Errores que NO se deben repetir (lista del PROCESO_COMPLETO):** 1) decir «ya está completo» sin haberlo verificado; 2) generar imágenes con IA o con Flow; 3) usar vistas previas pequeñas de Google; 4) correr Real-ESRGAN sin `-t 64`; 5) renderizar con la laptop desconectada; 6) poner los nombres de la lista en letra pequeña (van en letra grande bajo el número); 7) repetir fotos; 8) poner créditos, preguntas en la descripción o música; 9) preguntarle cosas a Luis en medio de una mejora que pidió hacer de corrido; 10) fiarse de que las fotos mejoradas con Real-ESRGAN son las correctas (compararlas con su original); 11) contar las repetidas por nombre de archivo (se cuentan comparando las imágenes).

**Lo que se entrega siempre (por video):** 1) `final/VIDEO_FINAL.mp4` (en la práctica del canal: `video_<tema>/video_completo/12_<tema>_completo_v<N>.mp4` + versión ligera 720p); 2) `final/edl.json`, el EDL con el que se renderizó; 3) `final/VIDEO_FINAL.srt`; 4) `final/miniatura.jpg` y `final/TEXTOS_YOUTUBE.txt` (en la práctica: `miniatura/` + `descripcion_youtube.md`); 5) la salida completa de `python src/verificar.py final/VIDEO_FINAL.mp4 final/edl.json`, que debe decir **APROBADO**; 6) informe de entrega (duración real, planos, fotos distintas, repetidas, autenticidad, verificación, reservas aceptadas).

**Estructura de carpetas por video (práctica vigente):** `~/workspace/nostalgia_colombia/video_<tema>/` con `guion_*.md`, `bloques_voz_<tema>.md`, `voz/` (15 bloques + `voz_<tema>.wav` + `voz_<tema>_final.wav`), `video_completo/` (v1 + ligera), `miniatura/`, `descripcion_youtube.md`, `edl_<tema>_v<N>.json`, SRT, `INFORME_ENTREGA_V<N>.md`, `verificar_v<N>.txt`, `revision/REVISION.md`, informes de investigación y cruce.

### 8.6 Densidad visual (Dichos, 2026-11-06)

Por orden de Luis Carlos, los videos llevan **más imágenes y más videos que lo habitual**, cuadrando cada plano con lo que va diciendo la voz (reglas 25 y 26). Metas: **≥250 fotos distintas, ≥45 clips, cortes cada ~4–5 s**. Referencia Dichos (2026-11-07): 408 fotos distintas + 33 clips, 5 manifiestos con origen, licencia, frase que cubre y marca SEGURA/DUDOSA. El mínimo de clips de `verificar.py` escala con la duración (34 clips para 18:38; 33 para 18:12): si los clips exactos no alcanzan, recortar segmentos adicionales distintos de los documentales largos ya conseguidos (Bogotá 2011, Silent War 1945, cumbia de Cartagena 151 s) y, si hace falta, Pixabay por navegador en vivo (Pixabay quedó bloqueado en esta VM: Cloudflare 403). Huecos sin material libre en Dichos (abuela en mecedora, mamá arreglando la camisa, molinillo en uso, abuelo mirando el cielo, el ridículo exacto en el salón): esas paradas van con fotos o con clips de ambiente vecinos solo si la escena cuadra, nunca con relleno extranjero.

---

## 9. Sistema de miniaturas

### 9.1 Reglas del skill (producción)

- Construir la miniatura sobre la misma fórmula del título, con una escena colombiana densa con **al menos 8 a 10 marcas visibles de época**, como la oficial de Marcas con su vitrina. Esto reemplaza la fórmula anterior de franja blanca.
- Validar cada miniatura contra el despiece del canal de referencia en el segundo cerebro: adaptar una miniatura de referencia validada en vez de copiarla, y comprobar el bloque rojo de urgencia y el contraste a los tamaños reales de visualización.
- **Cuando él rechaza miniaturas generadas por el asistente, entregarle el prompt de modelado en vez de otra versión.** Nombrar la miniatura de referencia validada que adapta, el entorno colombiano y el conteo mínimo de marcas, para que él genere la oficial en ChatGPT él mismo.
- Comprobar el banner o la miniatura terminados a los tamaños reales de visualización y mantener el contenido crítico dentro de la zona segura central antes de entregarla.
- Mejorar una miniatura aprobada solo por edición directa y nunca regenerando la imagen completa.
- Mantener cada producto, marca, persona, pose y composición aprobados sin cambios en un pase de calidad, y cambiar solo nitidez, claridad de rostros y el tratamiento del título.
- Mantener la fuente y el fondo del título idénticos a la versión aprobada, para que un pase de calidad no reestilice el título.
- Antes de entregar una miniatura mejorada, comprobar cada elemento de la versión aprobada contra la nueva versión e informar cualquier elemento faltante en vez de entregarla como aprobada.
- Regla de calidad (2026-10-29): al mejorar, no cambiar producto/marca/persona/pose/composición, solo nitidez, por edición directa.

### 9.2 Prompt maestro de miniaturas colombianas — VERBATIM

Fuente: `~/workspace/nostalgia_colombia/prompt_maestro_miniaturas_colombianas.md`. Uso: sirve para cualquier video de La Chiva del Pasado. Antes de pegar en ChatGPT, rellenar TODO lo que va entre [CORCHETES] y adjuntar la imagen base. No dejar ningún corchete sin rellenar.

Cómo se usa:
1. Adjunta la imagen base (la miniatura del competidor que sirve de modelo, o nuestra candidata).
2. Rellena los corchetes con los datos de ESE video.
3. Pega el prompt completo en ChatGPT.

```
Edita ESTA imagen, no la regeneres desde cero. Es la miniatura del video «[TÍTULO DEL VIDEO]», del canal de nostalgia colombiana La Chiva del Pasado. Mantén exactamente la misma composición, el mismo estilo fotográfico, la misma idea, la misma superficie principal (mesa, mostrador, sala o lo que muestre la imagen), las mismas poses de las personas que aparezcan y la misma banda superior con el texto exacto «[TEXTO EXACTO DE LA BANDA]» en letras gigantes negras y rojas.

PROHIBIDO, sin excepción:
- Cambiar, mover, quitar, agregar o rediseñar NINGUNO de los elementos colombianos de esta lista (son los del tema, exactos, y no se inventa ninguno fuera de ella):
[LISTA DE ELEMENTOS COLOMBIANOS EXACTOS, uno por línea, con su marca si aplica. Ejemplo: televisor de perilla, ventilador de metal, greca, Osterizer de vaso de vidrio…]
Mismos modelos, mismas posiciones, mismas marcas y etiquetas legibles donde las tengan. No inventes otros elementos ni cambies sus formas, colores o tamaños.
- Cambiar el texto de la banda, los colores de la banda, el formato 16:9 ni la iluminación general.
- Dejar ningún elemento extranjero del original: elimina [ELEMENTOS EXTRANJEROS A ELIMINAR, por ejemplo: cassettes de Maná, Caifanes y Juan Gabriel, cintas de Oaxaca, marcas Sony, JVC, Panasonic, papel picado, cempasúchil, o lo que traiga la imagen base]. Cero elementos mexicanos o de otro país.
- Cambiar a las personas: mismas caras, mismas poses y misma ropa en estilo.

ÚNICOS CAMBIOS AUTORIZADOS:
1. Elementos: los de la imagen base se reemplazan ÚNICAMENTE por los de la lista de arriba, puestos donde estaban los originales. Congruencia de escala obligatoria: los elementos grandes van a su escala real en el entorno (de pie, al fondo o a los lados), nunca encima de una mesa o superficie si no caben ahí; sobre la superficie solo los de tamaño coherente.
2. Entorno: volverlo colombiano sin tocar la composición. Cambia la vista del fondo por un entorno colombiano coherente con el tema ([ENTORNO COLOMBIANO PROPIO DEL TEMA, por ejemplo: pueblo andino con techos de teja de barro, casas blancas, torre de iglesia y montañas verdes; o calle de Cali, o cocina de finca vallecaucana, según el video]). Agrega detalles colombianos discretos sin tapar ningún elemento: sombrero vueltiao colgado, costal de café, buganvilias, banderita de Colombia pequeña en un punto libre, [OTROS DETALLES PROPIOS DEL TEMA].
3. Personas: las mismas, pero con detalles más colombianos y discretos, coherentes con el tema: [DETALLES DE LAS PERSONAS, por ejemplo: el hombre con sombrero vueltiao en vez de la gorra; la mujer con una flor de buganvilia en el pelo y el bordado de su delantal como flores colombianas; camisa de la Selección Colombia; ruana; según el tema]. Nada más cambia en ellos.

Si algún cambio obligara a mover, tapar o alterar un elemento de la lista, no lo hagas: deja ese detalle fuera.

Formato de salida: 16:9, 1280×720.
```

Notas para rellenarlo bien (del archivo): la lista de elementos debe ser LA LISTA APROBADA del video, no una inventada. Si existe un juego «como tal» de ese video (bebidas, platos, transportes, electrodomésticos), usa esos productos. Si un elemento no tiene foto libre real (hueco declarado, como la nevera Icasa), la miniatura lo muestra como tipo generado, pero nunca se presenta como foto real del producto. Ejemplo ya rellenado para Electrodomésticos: ver `video_electrodomesticos/miniatura/prompt_chatgpt_miniatura_electrodomesticos_v2_colombiano.md`.

### 9.3 Textos de banda por video (aprobados o propuestos)

- Marcas: «MARCAS COLOMBIANAS DESAPARECIDAS» (oficial). Juguetes: «¡TODOS LOS TUVIMOS!» (oficial v2). Dulces: «¡YA NO LOS VENDEN!». Navidad: «¡ASÍ ERA LA NAVIDAD DE ANTES!». Bebidas: «¡QUÉ SABOR!». Comerciales: «¿SE ACUERDA DE ESTOS COMERCIALES?» (miniatura aprobada «perfecta» 2026-10-28). Platos: «¡YA NADIE LOS HACE!» (miniatura v4 de ChatGPT recomendada como oficial, sin aprobación expresa registrada). Series: «LA SERIE DE LAS OCHO». Viajes: miniatura aún sin aprobar. Electrodomésticos: propuesta «¡EL QUE LO TENÍA ERA RICO!» (ninguna oficial). Música: «¡ASÍ SONABA LA CASA!» (oficial, v2 de ChatGPT aprobada 2026-11-05, «dejemos asi»). Famosos: «¡ERAN DE LA CASA!» (candidatas v2–v5, ninguna oficial; v5 = fondo sala colombiana, 4 intactos, Diomedes con foto aportada por él, Legarda con foto nueva aportada por él; las imágenes generadas parecidas a las fotos NO son fotografías reales). Tragedias: «¡NADIE LO OLVIDA!» (miniatura OFICIAL v10 aprobada 2026-11-07, «ESTA ES LA DEFINITIVA»; defecto conocido: números de preso inventados 128483–128486, el real de Escobar es 128482). Dichos: «¡YA NADIE LOS DICE!» (propuesta, sin aprobar).
- 10 temas nuevos (2026-11-02): Licores y Cervezas «¡ASÍ BRINDÁBAMOS ANTES!» · Primeros Centros Comerciales «¡ASÍ SE PASEABA ANTES!» · Útiles del colegio «¡ASÍ ERA EL COLEGIO!» · Sucesos «¡ASÍ LO VIVIMOS!» · Celulares pre-táctil «¡ASÍ LLAMÁBAMOS ANTES!» · Fiestas de Cali de antaño «¡ASÍ ERA LA FERIA!» · Oficios de antes «¡OFICIOS PERDIDOS!» · Consolas y videojuegos «¡ASÍ JUGÁBAMOS ANTES!» · Empresas de narcotraficantes «¡NADIE LO SABÍA!» · Cosas de la Cali de antes «¡ASÍ ERA CALI!».

---

## 10. Sistema de descripción y capítulos

### 10.1 Formato entregado (el que se replica)

Estructura real de las descripciones entregadas (Música v1 y Tragedias borrador aprobado):

1. **Apertura en escena** (2–3 frases que ponen al espectador en la casa / la época; nunca un resumen frío).
2. **Qué se cuenta en el video y qué NO** (en Música: «En este video no suenan las canciones: las contamos»; en Tragedias: «Este video no es para celebrar nada: es para recordar, con respeto…»).
3. **Invitación a comentar** («Cuéntanos en los comentarios cuál… y cuál faltó, porque la lista la completamos entre todos»).
4. **Invitación a la lista de reproducción:** «Sigue en La Chiva del Pasado con la lista de reproducción, que ahí están todos los temas que nos hacen recordar cierta época.»
5. **La lista 12→1** (con autores verificados cuando aplica; atribuciones con reserva marcadas como tales).
6. **Capítulos con los tiempos REALES de la línea de voz procesada** (de `audio/frases.json` / SRT; a re-verificar contra el render final si el montaje desplaza el audio).
7. **Créditos del material:** solo con las fuentes reales verificadas del video terminado (Wikimedia Commons, Pixabay, Flickr, con los fotógrafos cuando aplica). Créditos PENDIENTES hasta tener el video terminado: nunca inventar créditos.

### 10.2 Ejemplo real completo — Música v1 (formato a replicar) — VERBATIM

Fuente: `~/workspace/nostalgia_colombia/video_musica/descripcion_youtube.md`.

```
# Título y descripción de YouTube — Música v1
## «12 CANCIONES Colombianas que Todos Cantábamos en Familia y Quedaron en el Olvido»
**Video:** `video_completo/12_musica_completo_v1.mp4` (18:53, verificar.py APROBADO)
**Miniatura oficial:** `miniatura/miniatura_musica_candidata_v2_chatgpt.png` («¡ASÍ SONABA LA CASA!»)
**Capítulos:** tiempos reales de la línea de voz procesada (`audio/frases.json`).

---

## TÍTULO

12 CANCIONES Colombianas que Todos Cantábamos en Familia y Quedaron en el Olvido

---

## DESCRIPCIÓN

Antes la música no se oía con audífonos: sonaba en la casa entera, con el olor del café colado y el canto del gallo al fondo, y la familia entera la cantaba, aunque desafinara.

En este video contamos doce canciones colombianas que todos cantábamos en familia y que ya no suenan como antes. En este video no suenan las canciones: las contamos, con las historias de las casas donde sonaban, en la radio de la cocina, en la viejoteca del domingo y en diciembre con la familia reunida.

Cuéntanos en los comentarios cuál de estas doce cantaba tu familia y cuál faltó, porque la lista la completamos entre todos.

Sigue en La Chiva del Pasado con la lista de reproducción, que ahí están todos los temas que nos hacen recordar cierta época.

Las doce, de doce a uno:
12. Soy Colombiano — Rafael Godoy (Silva y Villalba)
11. El Regreso — Efraín Orozco
10. Amo — Arnulfo Briceño
9. La Lancha — Dueto de Antaño (arreglo de Camilo García, una melodía que viene de mucho antes)
8. Esperanza — Nelson Ibarra (Dueto de Ibarra y Medina)
7. Cenizas al Viento — José A. Morales (Silva y Villalba)
6. La Enredadera — atribuida a Luis Ernesto González Correa y Gonzalo Arias (Dueto de Antaño)
5. Yo También Tuve 20 Años — José A. Morales (Dueto Remembranzas)
4. A Quien Engañas Abuelo — Arnulfo Briceño (Garzón y Collazos)
3. Vientos de Navidad — Wilfran Castillo (Los Diablitos)
2. No Quiero Envejecer — Pedro Pablo Peña (Lucho y Rafa)
1. Pueblito Viejo — José A. Morales

Capítulos:
0:00 Apertura
0:36 12. Soy Colombiano
2:04 11. El Regreso
3:31 10. Amo
4:58 9. La Lancha
6:29 8. Esperanza
7:52 7. Cenizas al Viento
9:17 Llamado
9:35 6. La Enredadera
11:02 5. Yo También Tuve 20 Años
12:32 4. A Quien Engañas Abuelo
13:50 3. Vientos de Navidad
15:24 2. No Quiero Envejecer
16:52 1. Pueblito Viejo
18:28 Cierre

Créditos del material: imágenes y videos de archivo con licencia libre (Wikimedia Commons, Pixabay y Flickr), verificados uno por uno para este video; fotos de amaneceres de Alejandro Bayer (Flickr). Los coros que se ven cantando son el Coro del Colegio Alemán de Barranquilla y el Coro Sirenas de Barranquilla, en el Festival Tlaxcala Canta 2019.
```

### 10.3 Tragedias — descripción aprobada y capítulos reales

Fuente: `~/workspace/nostalgia_colombia/video_tragedias/descripcion_youtube.md` (aprobada por Luis Carlos 2026-11-05, «esta bien»; título actualizado 2026-11-07 13:42 por orden suya). Título: «12 TRAGEDIAS de los 90 Causadas por Narcotraficantes en Colombia que Nadie Puede Olvidar». La descripción abre con la escena del país en silencio frente al televisor, aclara que no es para celebrar nada sino para recordar con respeto, invita a comentar cuál de las doce recuerdan y cómo la vivieron en su casa, invita a la lista de reproducción y lista las doce de doce a uno (Ortega, Castro Gil, Lara Bonilla, Diana Turbay, Andrés Escobar, los tres carros bomba del Día de la Madre de 1990, el camión bomba a El Espectador, el Centro 93, Guillermo Cano, el edificio del DAS, Luis Carlos Galán, el avión de Avianca). Nota de honestidad (para el guion, no para publicar tal cual): la teoría sobre Gaviria y Avianca se trata en el video como pregunta abierta, nunca como hecho; la descripción no la afirma.

Capítulos (tiempos reales de la línea de voz procesada, frases.json / SRT v1; última frase 17:35, coherente con 17:36): 00:00 Apertura, 00:31 Ortega, 01:48 Castro Gil, 03:00 Lara Bonilla, 04:18 Diana Turbay, 05:22 Andrés Escobar, 06:43 Día de la Madre 1990, 08:04 Llamado, 08:38 El Espectador, 10:02 Centro 93, 11:19 Cano, 12:42 DAS, 14:06 Galán, 15:33 Avianca, 17:05 Cierre. Créditos pendientes (solo con las fuentes reales verificadas del video terminado). Miniatura OFICIAL v10 APROBADA (2026-11-07 13:33, «ESTA ES LA DEFINITIVA»): 4 narcos con letreros de preso, estación de policía en llamas, banda «¡NADIE LO OLVIDA!». NO publicar sin su palabra.

### 10.4 Reglas de descripción

- Sin preguntas en la descripción (regla del repo: no poner preguntas; la invitación a comentar es una invitación, no una pregunta). Sin mencionar IA. Con 3 emojis y la palabra clave primero (regla del README del repo; en la práctica entregada la descripción no lleva emojis visibles — seguir el formato entregado de §10.1/§10.2).
- Capítulos: siempre desde la línea de voz procesada (`audio/frases.json` / SRT), nunca desde el audio crudo ni estimados. Re-verificar contra el render final si el montaje desplaza el audio.
- La descripción deja claro lo que el video NO hace cuando aplica (las canciones no suenan, solo se cuentan; los comerciales no se ven, etc.).
- Hashtags base: #LaChivaDelPasado #NostalgiaColombia #HistoriaDeColombia + 2–3 del hecho concreto; nunca más de 5 en la descripción visible.

---

## 11. Catálogo y estado actual de cada video

### 11.1 Estado publicado del canal (verificado por API 2026-11-05)

Canal `UCHdDXyM8cVi-SxWcFWh4mdA`, @LaChivadelPasado. **12 videos publicados (25 oct–5 nov 2026), 631 suscriptores, 159.435 vistas totales.** Publicó ÉL, a diario, pese a los fallos declarados de verificar.py en varios. IDs y cifras (vistas/likes/comentarios al 2026-11-05):

| # | Video | ID | Publicado | Vistas | Likes | Comentarios |
|---|---|---|---|---|---|---|
| 1 | 12 Marcas Colombianas… | `GX_lN8-nt4U` | 25 oct | 109.393 | 714 | 60 |
| 2 | 10 Juguetes hechos en Colombia | `P6G8GdJS_Iw` | 26 oct | 11.388 | 167 | 10 |
| 3 | 12 Dulces del colegio | `lPRE4p1OuVQ` | 27 oct | 13.834 | 132 | 9 |
| 4 | 12 Costumbres de Navidad | `qusgo3duLNs` | 28 oct | 34.879 | 514 | 40 |
| 5 | 10 Comerciales | `hcIVlxMmtog` | 29 oct | 8.186 | 67 | 4 |
| 6 | 12 Bebidas de niños | `D-2HJeIpOX4` | 30 oct | 2.504 | 39 | 4 |
| 7 | 10 Platos de la abuela | `AapKwRKE6LI` | 31 oct | 2.871 | 49 | 7 |
| 8 | 10 Platos de las abuelas cada domingo | `Igov_tJzu0k` | 1 nov | 961 | 8 | 2 |
| 9 | 12 Formas de Viajar | `vZn1mzVqBPg` | 2 nov | 2.929 | 31 | 0 |
| 10 | 12 Electrodomésticos | `T34GNR0tmsY` | 3 nov | 2.941 | 32 | 3 |
| 11 | 10 Series, la serie de las ocho | `CUX_nHpMhVc` | 4 nov | 921 | 18 | 3 |
| 12 | 12 Canciones en familia (Música) | `wek2L5p_tvI` | 5 nov | 113 | 4 | 0 |

**Platos Domingo RESUELTO:** lo publicó como video APARTE (no reemplazo) el 2026-11-01, pero era el MISMO video que Platos (la audiencia lo detectó: portada «LA NOVELA DE LAS 8»; él pidió disculpas en comentarios). Peor rendimiento tras Música. El canal ya respondió 35 veces como @LaChivadelPasado (respuestas cálidas); comentaristas repetidos: @MariaOvalle-o1x (6), @Polimorfismo2085 (7), @JhonAvila-x6s.

### 11.2 Ficha por video (título, lista, estado)

**1. Marcas (12).** Título: «12 Marcas Colombianas que Había en Todas las Casas — y Desaparecieron». Miniatura oficial «MARCAS COLOMBIANAS DESAPARECIDAS» (confirmada idéntica por MD5 a la oficial). Lista 12→1: helados Baloncito (y paleta Cola de Tigre), Betatonio, Gaseosas Konga, Granahorrar, Telecom y sus cabinas, Almacenes Caravana, Cervecería Leona y Malta Leona, Almacenes La 14, Chupi Plum, Almacenes Tía, Almacenes Ley, Conavi (la abejita). Subido 2026-10-25 y programado 10:00. v9/v10 NO aprobadas (3 metas de material). El cierre anuncia Dulces aunque el video 2 decidido es Juguetes. El viral del canal (42 % de los comentarios). Guion en el repo: `guion.txt`; video aprobado de referencia del repo: `final/12_marcas_colombianas_FINAL_v4.mp4` con EDL `final/edl_v4.json` (es la v3 aprobada, sin las fotos repetidas).

**2. Juguetes (10).** Título: «10 Juguetes HECHOS EN COLOMBIA que Desaparecieron Con el Tiempo y todos Tuvimos en la Casa». Miniatura oficial v2 «¡TODOS LOS TUVIMOS!». Lista 10→1: yo-yo, coca, Tili, cometa, carros de hojalata, balineras, Búffalo, Angelino, trompo, Estralandia. Guion v2, 3.697 palabras. Época preferida 80–2000; un ítem más viejo solo con excepción decidida por él (Mi Adorable Angelino).

**3. Dulces (12, excepción aprobada solo aquí).** Título: «12 Dulces Colombianos que Todos Comprábamos en el Colegio y Desaparecieron con el Tiempo». Lista: Motitas, Chupi Plum, melcocha, gelatina de pata, cigarrillos de caramelos, dulces de aguardiente, bolis, Bumba Metro, Chiclets Adams, Galletas Cómics, Sparkies original, Sapito. Guion contador 2.899 palabras. Ver §6.3 (Motitas, Sapito, Galletas Cómics).

**4. Navidad (12).** Título: «12 costumbres COLOMBIANAS que todos hacíamos en navidad y fueron OLVIDADAS con el tiempo». Lista aprobada 12: aguinaldos, cerrar la cuadra, Niño Dios, pólvora clásica y globos de mecha sin glorificar, natilla artesanal en paila, pesebre con musgo, Año Viejo gigante, novena barrial rotativa, casa de los abuelos, tarjetas por Adpostal, árbol de chamizo, estrén en el centro; reserva: Misa de Gallo. Guion humano 2.816 palabras. Para finales de noviembre por temporada (publicado 28 oct). El más querido por la audiencia.

**5. Bebidas (12).** Título: «Bebidas Colombianas que Tomábamos de Niños... y Quedaron en el Olvido». Lista aprobada «tal cual» 12→1: Soda Wizz, Frule, Chubby, Kapo, Kol-Cana, Konga, Gaseosas Lux, Tutti Frutti en bolsa, Frutiño, Malta Leona, Capitán Frutonita, Gaseosa Link (Tai de Pera dentro de Link, pendiente verificar por separado). Voz Cruz 815,76 s = 13:36. **v5 (2026-10-30): verificar.py NO APROBADO, 14 fallos — publicada igual por él el 2026-10-30.** Juego con original: 9/12. Ver §6.3 (Chubby/Kapo importados, Frule sin confirmar, Frizz fuera).

**6. Comerciales (10).** Título: «10 Comerciales Colombianos que Nos Sabíamos de Memoria y Quedaron en el Pasado». Lista 1→10: Conavi, Águila Roja, Davivienda «El Lugar Equivocado», Frutiño con Higuita, Dolorán, La Fina, Renault 4 «Amigo fiel», Gudiz, Noel castores, Bavaria «El Orejón». Guion contador 2.959 palabras (sin «Súbete» en este guion). Miniatura aprobada «perfecta» 2026-10-28 (`video_comerciales/miniatura/miniatura_comerciales_final_alta_calidad.png`). Regla de calidad de miniaturas (2026-10-29): al mejorar, no cambiar producto/marca/persona/pose/composición, solo nitidez, por edición directa.

**7. Platos (10).** Título: «10 Platos Colombianos que Hacía la ABUELA… y Quedaron en el Olvido» (encuadre: ritual perdido, no plato extinto; natilla de maíz NO entra, ya fue parada en Navidad). Lista V2 aprobada 10→1: brevas con arequipe, arroz atollado vallecaucano, sopa de mondongo, cuchuco de trigo con espinazo, mute santandereano, sobrebarriga en salsa criolla, mazamorra/peto de maíz, sopa de ruyas, lengua en salsa, sancocho de gallina criolla en fogón de leña (reserva: ajiaco). Guion humano 2.876 palabras APROBADO; voz aprobada 946,72 s = 15:47. **v2 entregada (938,70 s = 15:39): verificar.py NO APROBADO, mismos 8 fallos; él aprobó la SINCRONÍA («perfecto»).** Corrección: la voz dice «hogado» (780,38 s), Hogao estaba bien. Miniatura v4 de ChatGPT recomendada como oficial, sin aprobación expresa registrada.

**8. Series, antes Novelas (10).** Título decidido por él 2026-11-03: «10 SERIES Colombianas que Paralizaban el País Entero a las Ocho de la Noche». Miniatura: «LA SERIE DE LAS OCHO». Lista V3 aprobada 10→1: En cuerpo ajeno, Los Reyes, Chepe Fortuna, Las Juanas, La saga, Hasta que la plata nos separe, Pedro el escamoso, Pasión de gavilanes (remake de Las aguas mansas), Café con aroma de mujer, Yo soy Betty, la fea. Guion de trabajo = SU propio guion verbatim (1.963 palabras). Voz 648,20 s = 10:48. **v1 ÚNICA versión (642,2 s): verificar.py NO APROBADO, 2 fallos (clips 0; autenticidad 194/201).** Descripción entregada. Ver §6.3 (dos datos suyos pendientes de verificar antes de cualquier reedición).

**9. Viajes (12, excepción aprobada).** Título: «12 Formas de VIAJAR en Colombia que Se Quedaron en el Pasado». Lista 12→1 aprobada: brujitas de San Cipriano, planchón/ferry del Magdalena, chalupa rápida (de madera, de antes), campero carpado, avioneta/aerotaxi (con Satena), Jeep Willys «El Yipao», chiva/bus escalera, época dorada de la aviación (Avianca clásica + ACES), Renault 4/carro familiar, flota intermunicipal clásica, autoferro, Expreso del Sol/tren. Guion = SU guion verbatim (2.513 palabras, sin «Súbete», no tocar). Voz aprobada 870,32 s = 14:30. **v4 entregada (854,32 s = 14:14): verificar.py NO APROBADO, 3 fallos estructurales; v3 aprobada en contenido y subida a Drive por orden expresa** (1080p: https://drive.google.com/file/d/11EeNTIzlY31DyQDagjh514ZpyPHoWn8j/view?usp=drivesdk ; 2K: https://drive.google.com/file/d/1F7WAqP_yTFfwbsKi4WABt2MwOAvxgdMn/view?usp=drivesdk). Miniatura aún sin aprobar. Ver §6.3 (Palonegro, «último viaje» sin confirmar).

**10. Electrodomésticos (12).** Título confirmado por él: «12 Electrodomésticos que Más se Vendían en Colombia… y Dejaron de Fabricarse». Miniatura propuesta «¡EL QUE LO TENÍA ERA RICO!» (ninguna oficial). Lista 12→1 aprobada: ventilador de pedestal de metal, greca, lavadora de dos tinas, estufa de petróleo, plancha de carbón, molino Corona/Victoria, radiola, olla Imusa Super Express, Osterizer de vidrio, televisor de perilla, Singer de pedal, Icasa (los que se fabrican hoy en versión moderna se narran como «dejaron de fabricarse ASÍ»; el guion NO afirma ranking de ventas; único año narrado permitido: 2003). Guion humano aprobado 3.591 palabras; voz 19:54. **v2 entregada 2026-11-03 (1.163,7 s = 19:24, 335 MB): verificar.py NO APROBADO — 22 OK, 1 aviso, 3 fallos con causa declarada** (cortes 10,0/min por 39 holds que sacaron fotos extranjeras; clips 1/35; revisión 20 CAMBIAR). Juego «como tal»: 11/12 con foto de producto exacto, **nevera Icasa = HUECO**; molino con marca Spong & Co (no Corona); olla antigua Umbach (no Imusa). Réplica local SRT EXACTO en `video_electrodomesticos/srt_exacto/` — **ADVERTENCIA: sus tiempos crudos están sobre el audio completo; NO aplicar sobre la voz recortada (deriva 0→+30,47 s).**

**11. Música (12).** Título: «12 CANCIONES Colombianas que Todos Cantábamos en Familia y Quedaron en el Olvido». Ángulo #1 Familia; miniatura «¡ASÍ SONABA LA CASA!». **DECISIÓN (2026-11-04): SOLO CANCIONES, sin canciones de comerciales** (fuera Bienestar Familiar, Olímpica diciembre, Mieltertos, Bretaña). Reglas: sin reproducir ni un segundo de las canciones ni letras; sin Darío Gómez como ítem; peso visual en ESCENAS (casa, radio, viejoteca), no retratos. **LISTA APROBADA (2026-11-04 18:50) 12→1:** Soy Colombiano, El Regreso, Amo, La Lancha, Esperanza, Cenizas al Viento, La Enredadera, Yo También Tuve 20 Años, A Quien Engañas Abuelo, Vientos de Navidad, No Quiero Envejecer, Pueblito Viejo. Verificación de autor/año COMPLETA en `video_musica/verificacion_autores_anos.md` (ver §6.3). **GUION FINAL v3 APROBADO (2026-11-04 22:30, «perfecto asi es»):** `video_musica/guion_12_musica_version_humana.md`, 12 paradas × 11 párrafos exactos, 3.556 palabras, apertura «Súbete…», LLAMADO tras parada 7, cierre con invitación a la lista. Bloques: `video_musica/bloques_voz_musica.md` (15 bloques verbatim). **VOZ APROBADA (2026-11-05 00:16, «PERFECTO»):** 15 WAV Cruz en `video_musica/voz/` + `voz_musica.wav` unida 1.153,08 s = 19:13 (~185 ppm). **VIDEO v1 ENTREGADO (2026-11-05 02:52) Y ACEPTADO (2026-11-05 08:25, «Acepto la v1 así»):** `video_musica/video_completo/12_musica_completo_v1.mp4`, **verificar.py APROBADO, todas las metas**; 1.133,59 s = 18:53, 1920×1080 30 fps, 541.296.219 bytes; 246 planos (202 imagen, 35 clips, 9 papel), 214 fotos distintas 0 repetidas, autenticidad 214/214 OK; voz procesada −15,0 LUFS, 0 pausas >0,9 s, 3,13 pal/s. Versión ligera 720p entregada (`12_musica_completo_v1_ligero.mp4`, 153.202.527 bytes). Entregables: EDL `edl_musica_v1.json`, SRT (297 subtítulos), `INFORME_ENTREGA_V1.md`, `verificar_v1.txt`, `revision/REVISION.md`. **RESERVA DE TLAXCALA — aceptada por él tal cual (opción A, 2026-11-05 08:25):** 7 planos del Festival Tlaxcala Canta 2019 (coros COLOMBIANOS: Colegio Alemán y Sirenas de Barranquilla); 6 con reserva por procedencia (17,82 s de 1.133,59 s = 1,6 %). Solo UN plano muestra «Tlaxcala» legible: **Esperanza 6:34.9–6:40.0**, solo en su primer ~1–2 s. Commons agotado tras ~120 consultas. **MINIATURA OFICIAL APROBADA (2026-11-05 09:09, «dejemos asi», sin variantes):** la v2 generada por ÉL en ChatGPT con el prompt entregado, en `video_musica/miniatura/miniatura_musica_candidata_v2_chatgpt.png` (1672×941; original subido por él: `~/workspace/user/media_library/image/As__sonaba_la_casa_en_Colombia.png`). Verificada: banda exacta, familia cantando, radio de tubos, tocadiscos, sombrero vueltiao, costal «CAFÉ DE COLOMBIA», banderita, buganvilias, cero mexicanos. Detalle menor aceptado: la guitarra de la derecha se ve como guitarra común, no tiple. Referencia: miniatura de «35 COSTUMBRES QUE TODO MEXICANO DE LOS 90s VIVIÓ» del canal mexicano. **TÍTULO Y DESCRIPCIÓN ENTREGADOS (2026-11-05 09:21):** `video_musica/descripcion_youtube.md` (ver §10.2). **PUBLICADO por él el 2026-11-05** (video `wek2L5p_tvI`, 113 vistas y 0 comentarios el primer día).

**12. Famosos (12, excepción aprobada 2026-11-03) — NO PUBLICADO.** Título APROBADO: «12 FAMOSOS Colombianos que Eran Parte de tu Vida… y Se Fueron para Siempre»; miniatura «¡ERAN DE LA CASA!». Concepto: famosos amplio (cantantes, actores, redes); cada parada primero el recuerdo vivido, luego la tragedia; solo hechos públicos verificados, tono respetuoso. Variante ofrecida sin respuesta: «12 FAMOSOS Colombianos que Eran INOLVIDABLES… y Ya Nadie los Recuerda» (él mismo había descartado ese cierre por falso: la audiencia escribe «aún duele»). Lista aprobada 12→1: Yeison Jiménez, Sandra Reyes, Legarda, Carlos Benjumea, Rafael Orozco, Martín Elías, Jota Mario Valencia, Fabiola Posada, Fernando González Pacheco, Darío Gómez, Jaime Garzón, Diomedes Díaz. Guion aprobado («esta perfecto») y voz aprobada (Cruz, 19:31). Investigación base: 3 rondas API (80 videos, 996 comentarios) + Gemini Deep Research Argon Alto (Investigación https://gemini.google.com/app/b8234f932d141a5e , Audiencia https://gemini.google.com/app/fbaab99e89826916 , Anécdotas https://gemini.google.com/app/8450c34fa575f986) + cruce en `video_famosos/informe_cruce_api_gemini.md` e informe de retratos `informe_mas_retratos_libres.md`. **ERROR DON CHINCHE corregido:** Don Chinche lo interpretó **Héctor Ulloa** (1982–1989), NO Benjumea; parada 9 reescrita (anclas reales: El taxista millonario, Sabariedades con Pacheco, Yo y tú), bloque 05 re-grabado (100,6 s) y APROBADO. **Don Chinche = 0 en guion, bloques, SRT y EDL.** **v3 ENTREGADA (2026-11-03 23:32):** `video_famosos/video_completo/12_famosos_completo_v3.mp4`, 1.161,12 s = 19:21, 353.458.570 bytes, solo voz; v1/v2 intactas. **verificar.py NO APROBADO, mismas 10 fallas en v1/v2/v3, causa raíz: solo 59 fotos libres verificadas para 406 huecos.** Versión ligera 720p entregada (`12_famosos_completo_v3_ligero.mp4`, 240 MB). **v3 subida a Drive por orden expresa con link público de lectura: ID `1972bia8IBNsEERYw8IeHcxt_FPOiFNEv` — https://drive.google.com/file/d/1972bia8IBNsEERYw8IeHcxt_FPOiFNEv/view?usp=drivesdk**. Descripción entregada (`video_famosos/descripcion_youtube.md`, capítulos v3). **NADA publicado.** Retratos libres: **26 verificados (25 en el video + 1 de Jota Mario fuera)**. **Benjumea 0 y Martín Elías 0 retratos libres en vida (HUECO TOTAL)**; Rafael: solo 1 dudoso (220×165, licencia dudosa); 2 retratos mejores de Rafael fueron BORRADOS de Commons el 2026-08-19 por copyvio (NO usar). Pacheco: su retrato Soho 2006 ES el archivo CC BY 2.0 de Alejandra Quintero Sinisterra (verificado byte-idéntico). **Jota Mario: retrato verificado 1200×1514 CC BY-SA 4.0 (Jefferestiw, 2017) en `video_famosos/jota_mario_valencia_2017_ccbysa4.jpg`, SIGUE SIN meterse al video.** Legarda: `legarda_enero_2017.png` 502×694 CC BY 3.0 El Antinoti (la usa el video). Advertencia: foto grupal de Jota (2015) incluye a Laura Acuña y Milena López, VIVAS: solo como equipo de «Muy Buenos Días», nunca como fallecidas. Miniatura: candidatas v2–v5 (imágenes generadas parecidas a las fotos, NO fotografías reales; ninguna oficial). v5 = fondo sala colombiana, 4 intactos (Diomedes con foto aportada por él, Legarda con foto nueva aportada por él), banda «¡ERAN DE LA CASA!». Prompt fondo colombiano: `miniatura/prompt_chatgpt_miniatura_famosos_v4_fondo_colombiano.md`.

**13. Tragedias (12) — VIDEO v2 APROBADO, NO PUBLICADO.** Título NUEVO APROBADO (2026-11-07 13:42, cambio por orden suya): «12 TRAGEDIAS de los 90 Causadas por Narcotraficantes en Colombia que Nadie Puede Olvidar»; antes «12 TRAGEDIAS Colombianas Causadas por Narcotraficantes que Nadie Puede Olvidar» (aprobado 2026-11-05 10:42, «apruebo»). Advertencia hecha y aceptada por él: tres de las doce son de 1989 (Avianca 27 nov 1989, DAS 6 dic 1989, Galán 18 ago 1989) — «de los 90» se mantiene por su decisión, no reabrir. Origen: el 2026-11-05 10:39 rechazó Ciudades; 10:40 propuso «algo con los narcotraficantes»; 10:41 propuso su título. **LISTA FINAL 12→1:** Ortega, Castro Gil, Lara Bonilla, Diana Turbay, Andrés Escobar, Día de la Madre 1990, El Espectador, Centro 93, Cano, DAS, Galán, Avianca. **CERO atribuciones en disputa.** FUERA: Jaramillo, Pizarro, Gómez, Trujillo, Mapiripán. Reserva: Puerto Alvira (1998, paramilitar, mismo problema de atribución). Investigación completa (dos patas, cruzadas en `video_tragedias/informe_cruce_api_gemini.md`): API ronda 1 (10 búsquedas, 30 videos, 467 comentarios, sin 429; 17 anécdotas verificadas A1–A17, 8 del DAS; mejores: A1 DAS mamá/hija cruzando Paloquemao 132 likes, A2 DAS niño de 8 años 116, A3 Avianca niño de 7 años en Soacha 62, A4 DAS despertada por la explosión 49, A5 Avianca despedida de José del Carmen Gaita) + Gemini Deep Research Argon Alto (Investigación https://share.gemini.google/WKWYoJ0aN1tZ , Audiencia https://share.gemini.google/usLFHSRzrcig , Anécdotas https://share.gemini.google/DMrzeDoC0VbV ; informe 1: 5 pilares insustituibles —Avianca, DAS, Galán, Cano, Centro 93— + 5 omisiones —Andrés Escobar, camión bomba a El Espectador 1989, Diana Turbay, Álvaro Ortega, Día de la Madre 1990—; saca Trujillo y Mapiripán; débiles: Gómez —FARC lo asumió ante la JEP 2020—, Jaramillo/Pizarro —paramilitares—) + ronda 2 de anécdotas (7 búsquedas, 25 videos, 292 comentarios; Andrés Escobar el ganador: B2 187 likes «Lloré esa muerte como si fuera mi hermano. Me acuerdo que ni siquiera fui a la universidad de lo afectada que estaba», B3 71, B4 64, B5 16; Ortega B1 con RESERVA —testigo en el Hotel Veracruz, 4.º piso, sicarios en moto DT blanca, 7 likes; contradice otra versión, sicario en carro—; B8 cita de Óscar Córdoba sobre el autogol, 867 likes, NO verificada contra la entrevista original → NO está en el guion; B10 El Espectador delgada, 10 likes; Lara Bonilla 0 escenas; Castro Gil, Día de la Madre 1990 y Diana Turbay: 0 anécdotas de audiencia; el material humano de Diana está en el testimonio de su propio hijo Miguel Uribe Turbay, video `9JM4Vb82S1c`, NO minado todavía). **GUION v1** (`guion_12_tragedias_version_humana.md`, 3.584 palabras, solo anécdotas A tejidas; defecto: molde repetitivo). **GUION v2** (`guion_12_tragedias_v2.md`): reescritura humana, 3.562 palabras, 12×11 párrafos exactos, 18,8–19,5 min estimados; **APROBADO (2026-11-05, «esta bien dale», con la condición de 17–20 min)**. **VOZ aceptada para producción (2026-11-05, «dale hazlo» tras enviarle la voz final 17:36):** 15 bloques Cruz, `voz/voz_tragedias_final.wav` 1.056 s = 17:36, 196 ppm, −14,17 LUFS, TP −0,85, LRA 2,40, 0 pausas >0,9 s. **DESCRIPCIÓN APROBADA (2026-11-05, «esta bien»):** título y descripción + capítulos reales (§10.3), título actualizado 2026-11-07 13:42; créditos pendientes, se llenan con las fuentes reales del video terminado; capítulos a re-verificar contra el render final. **VIDEO v2 RECONSTRUIDO Y APROBADO (2026-11-06, 17:56, verificar.py APROBADO):** 216 cortes, 202/202 fotos, 34 clips, 0 fallos; versión ligera 720p lista; descripción final con capítulos recalculados y créditos. **MINIATURA OFICIAL v10 APROBADA (2026-11-07 13:33, «ESTA ES LA DEFINITIVA»):** `video_tragedias/miniatura/miniatura_oficial_v10.jpg` — 4 narcos con letreros de preso, estación de policía en llamas, banda «¡NADIE LO OLVIDA!». **Defecto conocido:** los números de los letreros son inventados (128483–128486; el real de Escobar es 128482) — corregir o dejar así como la eligió. **NO publicado en YouTube.** Video v2 subido a Drive 2026-11-06 por orden expresa con enlace público de lectura: ID `1MFeMhwOnFShng2vMtDklaTXitkfhuomx` — https://drive.google.com/file/d/1MFeMhwOnFShng2vMtDklaTXitkfhuomx/view?usp=drivesdk. No publicar en YouTube sin su palabra.

**14. Dichos (12) — VIDEO v1 APROBADO, NO PUBLICADO.** Título APROBADO (2026-11-06, refinado por él mismo): «12 DICHOS Colombianos que Nos Decían los Abuelos y ya nadie dice»; #3 del ranking por comentarios, sigue a Música (publicado); Ciudades vetada. Miniatura propuesta «¡YA NADIE LOS DICE!» (sin aprobar). **LISTA FINAL CERRADA 12→1 (cambio aprobado 2026-11-06, «si hazlo»):** Uña y mugre, Milagro, Cuentas claras, Arrieros, Sereno, Enteca, Pájaro en mano, Madrugar, Diablo, Hacer el oso, No dar papaya, No me abra los ojos; 6 [COL] y 6 [LATAM]. Propuestas sin audiencia (Sóbese, enano y demás) no entraron. Investigación: 3 prompts Gemini + API propia con cruce (`video_dichos/cruce_lista_final.md`); el informe Gemini original llegó 2026-11-07 15:04 («Arqueología Emocional del Habla Colombiana», https://share.gemini.google/CxPMdqIS5H26, 29 sitios; estuvo ~18 h atascado por el límite de Deep Research): converge con la lista aprobada en ojos #1, pero propone sacar papaya y diablo y meter «¿Durmió conmigo anoche…?» y «Al que le van a dar, le guardan» (0 menciones en el corpus API) — NO cambia la lista aprobada, que manda por comentarios de audiencia; los dos dichos nuevos quedan para un próximo video. OJO: las infografías del informe contradicen su texto; vale el texto. **GUION HUMANIZADO v2 APROBADO (2026-11-06, «perfecto»). VOZ APROBADA (2026-11-07, «perfecto»):** Cruz, corregida 18:12 (opción B: cortada la repetición de la Apertura, INTRO una sola vez; defecto verificado con dos transcriptores + alineación). **VIDEO v1 APROBADO (2026-11-07 ~18:30, verificar.py APROBADO, todas las metas):** `video_dichos/video_completo/12_dichos_completo_v1.mp4`, 1.092,42 s = 18:12, 1920×1080 30 fps, 453.751.554 bytes; 298/298 fotos OK autenticidad, 0 repetidas, 33 clips, −14,3 LUFS, 0 pausas >0,9 s, 0 negros >0,3 s, 12 aperturas numeradas, 64 palabras gigantes. Versión ligera 720p (`12_dichos_completo_v1_720p.mp4`, 180.768.297 bytes ≈ 172 MB). Primera pasada ~16:25 NO APROBADO (3 fallos); corrección +8 números de cifra y +22 palabras gigantes, 22 tramos re-renderizados. Material: 408 fotos distintas + 33 clips, 5 manifiestos. Reserva aceptada: 7 avisos de baja resolución preexistentes y 6 fotos DUDOSA en la resolución de duplicados. Descripción con capítulos reales en `video_dichos/descripcion_youtube.md`. **NADA publicado.** Pendiente: miniatura y su palabra para publicar.

### 11.3 Feedback del canal propio (2026-11-05, 142 comentarios leídos TODOS)

Informe: `~/workspace/nostalgia_colombia/feedback_canal_propio.md` + `feedback_canal_propio_raw.json`. Luis Carlos lo recibió el 2026-11-05 12:56 y respondió «es bueno saber eso».

- **Lo que más elogian:** (1) la emoción — Navidad el más querido («Tuve un nudo en la garganta todo el vídeo», «Hasta lágrimas me saco»); elogio típico = «gracias por traernos estos recuerdos»; (2) el recuerdo propio que despierta — el comentario más votado del canal (7 likes): «Trabaje para Leona de 1995 hasta que la vendieron a Bavaria»; (3) memoria compartida: diáspora (colombiana casada con holandés) y jóvenes (nacido en 2012, 6 likes).
- **Lo que más corrigen:** datos inexactos en Marcas (ver §6.3); «Muchas mentiras este video por lo menos bogota» (@camilovargasdaza1912).
- **La queja de contenido más repetida:** Comerciales sin comerciales reales — «Yo abri el video, para volver a ver los comerciales, y no habían comerciales» (2 likes); «He sido engañado, vine por los comerciales y no hubo ningúno» — el canal respondió que no los ha encontrado en buena calidad.
- **Única crítica dura:** imágenes con IA («las imagenes con AI? … que porqueria de videos», «genéricos, sin alma») — coincide con la regla propia de material real.
- **«Desapareció» que no desapareció** (la audiencia no lo perdona): Only sigue existiendo; algunos dulces todavía se venden; un Tía en Chapinero (calle 59 con 13) existía hace ~5 años.
- **Piden ver el producto del que se habla** (Juguetes: cómo eran los carros de balineras; Bebidas: no se vieron las gaseosas).
- **Peticiones de temas (las 5):** 1) ver los comerciales reales; 2) Marcas parte 2: Bancafé, Suramericana, Mitad de Precio, Paguemenos, Yep, Only + lista de 18 marcas de Medellín de @cesarroman3857 (Jünger, La Sorpresa, La Viña, Seguro Social, helados La Fuente, Simesa, Peldar, Comfama, Proleche, Pakita, Caribe, Cristal Oro, El Mar, Drácula, El Sótano, pollos Pinky); 3) Nacoral y Gacela (Juguetes); 4) más dulces: Qpitos, margaripalos, barilete; 5) más bebidas: Fanta mandarina/durazno/salpicón, Tai. NO hay peticiones de temas nuevos completos (Dichos/Radio/Ciudades): la gente pide segundas partes de lo ya visto.
- **Matiz de clase (Navidad):** «No todos tuvimos la oportunidad de ir al centro a comprar el estren» (ver regla 18 de §2).

### 11.4 Diez temas nuevos propuestos (2026-11-02, NO aprobados; solo título y miniatura pedidos)

1. Licores y Cervezas «¡ASÍ BRINDÁBAMOS ANTES!» (Samu). 2. Primeros Centros Comerciales «¡ASÍ SE PASEABA ANTES!» (Samu). 3. Útiles del colegio «¡ASÍ ERA EL COLEGIO!». 4. **SUCESOS** «¡ASÍ LO VIVIMOS!» (Samu, alto impacto 1). 5. Celulares pre-táctil «¡ASÍ LLAMÁBAMOS ANTES!» (Samu). 6. Fiestas de Cali de antaño «¡ASÍ ERA LA FERIA!» (William; ideal diciembre). 7. Oficios de antes «¡OFICIOS PERDIDOS!». 8. Consolas y videojuegos «¡ASÍ JUGÁBAMOS ANTES!» (Jeferson). 9. **EMPRESAS de narcotraficantes** «¡NADIE LO SABÍA!» (Samu, alto impacto 2; SOLO con fuentes verificadas — prensa, procesos judiciales, extinción de dominio — antes de nombrar a alguien). 10. Cosas de la Cali de antes «¡ASÍ ERA CALI!» (William; abre serie Municipios). Reserva: primeras empresas en llegar, programas infantiles, juegos de barrio, remedios de la abuela, comidas callejeras. **Narcos (Sucesos 4, Empresas 9) en espera, no cancelados; dosificar alto impacto. Los dos temas de alto impacto van deliberadamente separados.** (Tragedias nació de esta línea el 2026-11-05, tras el rechazo de Ciudades.)

### 11.5 Decisiones pendientes de Luis Carlos

**Famosos (7):** (1) vía de fotos para cumplir la regla «sale prácticamente siempre»: aportar propias/familiares, autorizar permisos de la lista B, o aceptar foto sostenida/hueco; (2) aceptar la v3 con los 10 fallos declarados; (3) aceptación explícita de 21 baja resolución, 6 NEUTRA, licencia de Rafael, 6 tributos de Garzón; (4) si el retrato verificado de Jota Mario entra en un ciclo de corrección; (5) aprobar/ajustar/descartar miniatura candidata v5; (6) si la variante de título «INOLVIDABLES… y Ya Nadie los Recuerda» reemplaza al aprobado; (7) opcional v4 de mejoras (10→8 fallos sin cambiar el veredicto). **La v3 es la última versión entregada; una v4 más rica en fotos NO existe aún y nunca debe describirse como terminada o entregada hasta que él elija una vía de fotos.**

**Tragedias:** miniatura OFICIAL v10 aprobada 2026-11-07. Pendiente: (1) su palabra para publicar — no la ha dado; (2) defecto conocido, recordado dos veces: números de letreros inventados (128483–128486; el real de Escobar es 128482) — corregir o dejar así como la eligió. Opcional (no bloquea): minar el testimonio del hijo de Diana Turbay (video `9JM4Vb82S1c`) si se quiere reforzar la parada 9 en una futura revisión.

**Dichos:** video v1 APROBADO 2026-11-07. Pendiente: miniatura «¡YA NADIE LOS DICE!» (sin aprobar) y su palabra para publicar.

**Correcciones posibles por feedback (solo si él las ordena):** verificar el minuto de Telecom ($200 vs $2.000) antes de cualquier reedición de Marcas; Comerciales con comerciales reales (la petición #1 del canal); Marcas parte 2 (material de sobra en los comentarios).

**Viajes:** miniatura aún sin aprobar. **Platos:** miniatura v4 de ChatGPT recomendada como oficial, sin aprobación expresa registrada. **Electrodomésticos:** ninguna miniatura oficial.

---

## 12. Entorno y herramientas + checklist end-to-end de un video nuevo

### 12.1 Entorno y herramientas

- **VM:** disco persistente `/home/hatch` 150 GB; RAM 7,7 GB sin swap; el overlay del sistema (~7,5 GB) se borra al reemplazar la VM (reinstalar Ollama, zstd, `ccr`, Remotion CLI si hace falta). ffmpeg 8.1.2 en `/usr/bin/ffmpeg`; yt-dlp en `~/.local/bin/yt-dlp` (anteponer `export PATH="$HOME/.local/bin:$PATH"`).
- **Ollama:** modelos en `/home/hatch/.ollama/models` (disco persistente, seteado vía `OLLAMA_MODELS`); el servicio necesita el proxy de salida o los pulls fallan con TLS. Límite local: modelos de 4B (CPU-only); los más grandes van por puente gratuito, no en local.
- **Puente CCR (1.0.73, `/usr/bin/ccr`, reinstalar tras reemplazo de VM):** OVH gpt-oss-120b (puerto 4001, por defecto), Groq (4002), OpenRouter openrouter/free (4003), NVIDIA deepseek-ai/deepseek-v4.1-flash (4004). Relanzar con `~/workspace/ollama/relanzar-puente.sh`. **Orden permanente (2026-11-01): usar SIEMPRE los mejores modelos disponibles;** en local solo qwen3.5:4b (qwen3:8b descargado pero no corre por RAM). NVIDIA verificado de punta a punta el 2026-11-01 (una primera clave falló y se reemplazó por el flujo seguro de registro, que es la única vía para claves, nunca un pegado en chat). FreeLLMAPI detenido, sin llaves cargadas; pendiente su decisión (levantarlo con Groq o dejarlo en reserva).
- **Claude Code 2.1.316** en `~/.local/bin/claude`.
- **Repo:** `~/workspace/nostalgia_colombia/documental-expediente/` (remoto GitHub `luiscarlosayalasilva2-rgb/documental-expediente.git`); `git pull` antes de trabajar, leer `docs/NOVEDADES.md`, nunca MP4 a GitHub, nunca constructores ad hoc. Render en tramos de 1200 fotogramas y unión al final (VM sin swap).
- **Referentes mexicanos descargados para estudio de estilo:** 41/47 MP4 en `~/workspace/Editor IA/Referentes/videos-mexico/` (6 bloqueados por bot de YouTube; decisión suya 2026-11-01: «Déjalo en 41 por ahora»). Guía de estilo medida: `~/workspace/Editor IA/Referentes/guia-de-estilo-medida-mexico.md` (mediana mexicana 33:42, ~8,1 cortes/min, voz 167 ppm; tensión abierta: sprint La Chiva 17–20 min por regla 2026-11-02). Skill video largo: `~/workspace/custom-skills/editor-video-largo-la-chiva/SKILL.md`.
- **Decisión Guía Converzzo (2026-11-01):** SÍ para VIDEO LARGO — replicar el estilo de edición y editar nosotros: guía de estilo MEDIDA de ~5 referentes y plan por escenas APROBADO antes de renderizar, adaptado a La Chiva (1920×1080, repo Documental Expediente, solo voz sin música). NO su parte de shorts (ni vertical, ni Cowork, ni ElevenLabs, ni HeyGen, ni música/efectos de comercial). Modelos en /home/hatch/.ollama/models (disco persistente 150 GB).
- **Herramienta JM BOTS SRT EXACTO** subida por él (`~/workspace/user/files/jm_srt_exacto.html`, 2026-11-03, sin clave incrustada); la réplica local en Electrodomésticos la reemplaza para trabajo interno. **ADVERTENCIA:** sus tiempos crudos están sobre el audio completo; NO aplicar sobre la voz recortada (deriva 0→+30,47 s).
- **Descargas del navegador:** `~/workspace/browser_downloads/sess-<id>/`.
- **Cuentas:** Google AI Studio, sesión luisayaka87@gmail.com (voz Cruz). YouTube Data API (conector `custom.youtube-data-api`). Drive triviatk4@gmail.com, 5 TB (solo se sube si él lo pide). **No subir a remote-storage** (declinado por él 2026-11-03).

### 12.2 Checklist end-to-end de un video nuevo (en orden)

1. **Tema:** elegir desde los territorios (§1) y el ranking vigente por comentarios (§5.6), respetando el mural de 11 familias (no repetir familia seguida). Pasar la **prueba del recuerdo VIVIDO**. Si el tema es de los 10 nuevos o del ranking, confirmar que no está descartado ni en espera sin su orden.
2. **Investigación:** correr los **3 prompts de Gemini Deep Research** adaptados al tema (§5.2–5.4) y, en paralelo, la investigación propia con la API de YouTube (§5.5 + prompt de anécdotas §5.7). Cruzar ambas en `informe_cruce_api_gemini.md` junto al tema. Guardar los informes en español en la carpeta del video.
3. **Ficha de fuentes (Anexo A1):** completa ANTES de escribir una línea de guion. Mínimo 2 fuentes independientes para el hecho central y para cada ítem. Sin ficha completa, el guion no pasa a grabación.
4. **Lista:** proponer la lista 10 o 12 (con la excepción justificada) en orden de cuenta regresiva, con la parada 1 como la de mayor carga nostálgica y la parada N de reconocimiento inmediato. Obtener su aprobación de la lista (o usar la lista que él ya aprobó).
5. **Guion:** escribirlo en el formato aprobado (§6.1): 12 o 10 paradas × exactamente 11 párrafos cortos, apertura «Súbete…» (salvo orden contraria), LLAMADO tras la parada 7, cierre con invitación a la lista. Contar los párrafos con `muse.exec` antes de entregar. **PARAR y esperar su aprobación del guion.** Sin aprobación no se genera nada.
6. **Bloques de voz:** crear `video_<tema>/bloques_voz_<tema>.md` (15 bloques verbatim, §7.1).
7. **Voz:** generar los 15 WAV con Cruz en Google AI Studio (§7.1: Style verbatim, Expression vacío, temperatura 1). Unir con ffmpeg, verificar duraciones con `ffprobe`, procesar con `pausas.py` 0,8→0,5 + loudnorm dos pasadas (§7.2). Medir: duración 17–20 min, −14/−15 LUFS, 0 pausas >0,9 s. **Enviarle la voz final y esperar su aprobación** («PERFECTO» o re-grabar el bloque que pida).
8. **SRT y alineación:** `transcribir.py` (faster-whisper small) → `alinear.py` (guion ↔ palabras) → `audio/frases.json`. Verificar que el audio esté completo (transcribir los últimos 20 s) y que la voz no se haya saltado ninguna frase del guion. Generar el SRT con `generar_srt.py` (máx. 42 caracteres por línea, máx. 2 líneas, 1–7 s por subtítulo).
9. **Material visual:** una búsqueda por cada cosa concreta narrada (§8.4); tabla de homónimos antes de buscar; Commons/Pixabay/Flickr con licencia libre verificada primero; Google Imágenes en tamaño original con receptor + lote_google.js; foros/redes solo para localizar el original o pedir permiso. Revisar TODAS las fotos con los ojos (hojas de contacto). Pasar `revisar_fotos.py` y marcar la planilla `REVISION.md` toda en OK.
10. **EDL:** armarlo con `python src/nuevo_video.py plan …` (esqueleto automático), rellenar los PENDIENTE (foto/clip real de lo que se oye en ese segundo) y los REVISAR (textos), y validar con `nuevo_video.py validar` hasta que diga LISTO. Mejorar a HD (`emparejar_hd.py`, `aplicar_hd.py`, `mejorar_fotos.py` con `-t 64`, `limpiar.py`). **Nunca se arma el EDL desde cero ni con otra estructura.**
11. **Render:** `render.py` con 4 workers, en tramos de 1200 fotogramas, unión al final. Mezclar con la voz procesada y los efectos sintetizados (`efectos.py`). Revisar la hoja de fotogramas cada 8 s y buscar negros con `blackdetect`.
12. **Verificación:** `python src/verificar.py video.mp4 edl.json` en ciclo: corregir cada meta fallida con material real y volver a verificar, hasta APROBADO o hasta demostrar con búsqueda seria que ese material no existe; solo entonces entregar con la falla declarada, su causa y lo intentado. Autoanálisis con las reglas del repo (REGLAS_DURAS, CATÁLOGO, AUTENTICIDAD, NOVEDADES, verificar.py, revisar_fotos.py).
13. **Entregables:** video completo v1 (`video_completo/12_<tema>_completo_v1.mp4`) + versión ligera 720p + EDL + SRT + `INFORME_ENTREGA_V1.md` (duración real, planos, fotos distintas, repetidas, autenticidad, verificación, reservas) + `verificar_v1.txt` + `revision/REVISION.md` + descripción (`descripcion_youtube.md`, §10) con capítulos reales.
14. **Miniatura:** generar con el prompt maestro (§9.2) en ChatGPT (o entregarle el prompt a Luis Carlos para que genere la oficial). Verificar banda exacta, cero elementos mexicanos, prueba de 120 px, zona segura. **Esperar su aprobación de la miniatura** (la oficial es la que él aprueba, como Música v2 «dejemos asi»).
15. **Publicación:** SOLO con su palabra explícita. No publicar, no subir a Drive ni a remote-storage sin que lo pida. Entregarle el video, la miniatura y la descripción; él publica.

---

## 13. Lo que el nuevo chat NO debe hacer nunca

1. **Nunca inventar, inferir ni completar un dato** ausente de una fuente verificada sin confirmación explícita de Luis Carlos. Lo no confirmado queda «sin confirmar».
2. **Nunca publicar nada** (YouTube, Drive, remote-storage) sin su palabra explícita. Nunca reintentar la subida a remote-storage (declinada 2026-11-03).
3. **Nunca presentar una imagen generada con IA como foto real**, ni una foto pixelada mejorada con IA como foto original de archivo. Nunca rostros de personas reales generados o alterados. Nunca documentos «completados» con IA sin etiqueta de recreación.
4. **Nunca usar material extranjero o genérico** como si fuera colombiano: nada de Ecuador, nada de Casa Ley de México, Tía de Ecuador ni CONAVI de México, nada de dibujos genéricos, juguetes, afiches ni frames de comerciales de TV. Sin material exacto: foto colombiana que clave justo, sostener plano anterior, ficha breve o hueco declarado.
5. **Nunca poner la narración escrita en tarjetas de papel** como relleno, ni dejar una imagen quieta muchos segundos, ni escribir un editor propio: se usa `render.py` + `estilo.py` tal cual; solo cambia el EDL.
6. **Nunca acelerar la voz** (atempo o similar). Nunca cortar los silencios de más de 0,15 s (la regla vigente es solo >0,8 s → 0,5 s).
7. **Nunca afirmar como hecho un testimonio, una leyenda o una creencia popular.** Nunca presentar un agüero como HECHO REAL. Nunca inventar el origen, la fecha o la región de un dicho o un agüero. Nunca presentar la teoría Gaviria/Avianca (ni la pregunta de Diana Turbay) como hecho: siempre como pregunta abierta.
8. **Nunca reproducir ni un segundo de una canción, ni letras, ni audio de radio con derechos** (jingles, identificadores, programas) dentro de un video. Las canciones se cuentan, no suenan. La radio se cuenta, no suena.
9. **Nunca poner a un vivo en una miniatura como fallecido** (Marlon Moreno está VIVO y NO entra). Nunca un sustituto, genérico o IA como retrato real de un famoso.
10. **Nunca afirmar que algo «desapareció» sin comprobarlo** (Only sigue existiendo; algunos dulces todavía se venden). Nunca copiar contenido del canal de referencia ni de ningún canal (ni textos, ni guiones, ni miniaturas, ni el orden de ítems): se copia el formato, nunca el contenido.
11. **Nunca entregar un video con verificar.py en NO APROBADO como si estuviera aprobado.** Si no cumple, se arregla en ciclo; solo se entrega con la falla declarada, su causa y lo intentado.
12. **Nunca dar por terminado un trabajo sin verificarlo** («ya está completo» sin haberlo medido). Nunca fiarse de que las fotos mejoradas con Real-ESRGAN son las correctas sin compararlas con su original. Nunca contar las repetidas por nombre de archivo.
13. **Nunca descargar ni instalar nada en la PC de Luis Carlos** salvo que lo pida o sea realmente necesario. Nunca pedirle una contraseña o clave en chat (el flujo seguro es la única vía; el login en vivo lo completa él).
14. **Nunca hacer otra lista de famosos** tras Famosos (la regla vigente lo prohíbe; el curso además prohíbe construir canales SOBRE famosos). Nunca producir Ciudades como tema (rechazado por él el 2026-11-05: «no vamos a hacer ciudades»).
15. **Nunca usar «Ya Nadie las Recuerda» para canciones** (falso: la gente sí las recuerda). Nunca años literales en los títulos. Nunca clickbait («¡increíble!», «¡no lo vas a creer!», «el secreto que nadie te contó», «prohibido», «impactante»).
16. **Nunca glorificar a Escobar, hacer morbo con tragedias, ni meter política actual** en un video. Nunca meter eventos no narcos (Palacio de Justicia, Mitú, Armero, Jaime Garzón) en Tragedias aunque la audiencia los mezcle.
17. **Nunca describir la v4 de Famosos como terminada o entregada** (no existe aún). Nunca describir Famosos v3 como «terminada»: está entregada con 10 fallos declarados y sin publicar.
18. **Nunca aplicar los tiempos crudos del SRT sobre la voz recortada** (deriva 0→+30,47 s): todas las temporizaciones derivan de la línea de voz PROCESADA.
19. **Nunca preguntarle cosas a Luis Carlos en medio de una mejora que pidió hacer de corrido** («no me preguntes nada hasta que lo mejores»). Nunca re-preguntar una pregunta ya resuelta ni re-abrir una decisión ya tomada por él.

---

## 14. Verificación de completitud (repaso de ~/MEMORY.md línea por línea)

Se repasó `~/MEMORY.md` completo (Facts, Preferences, Commitments) y cada hecho o regla de La Chiva del Pasado quedó en este documento. Marcaje:

| Hecho / regla de MEMORY.md | Dónde quedó en este kit |
|---|---|
| Canal «La Chiva del Pasado», respaldo «La Colombia Que Fue», logotipo original suyo, libro rector, banner 2560×1440 (zona segura 1546×423), YouTube Data API conectada | §1, §3 |
| Canal de referencia Cuando México Fabricaba de Todo (ID UCtWtk6_Ph2EoHamCiI00lSg) | §1, §3 (sección 19) |
| Enfoque propio: nostalgia de la vida de antes, sentido amplio, matiz «no así tan literal» | §1, §3 |
| Audiencia unificada 35–65+, Colombia o exterior; familia como centro de gravedad y tono, no filtro literal; prueba del recuerdo VIVIDO; época 1970–2000 | §1, §3 |
| Mural de ideas: 11 familias, no repetir seguida; mapa actual de encajes | §1 |
| Corrección de voz 2026-10-21 («informar» vs contar) + refuerzos 2026-10-31 y 2026-11-05 | §2.21, §4 |
| Voz propia: 2 muestras a mano verbatim + rasgos | §4 |
| Material visual: sin derechos, utilizable en YouTube; foros/redes solo para localizar o pedir permiso; foto pixelada mejorada con IA no es foto original | §2.23, §8.4 |
| Catálogo del canal según Luis Carlos (2026-11-02): 9 videos con títulos y miniaturas | §11.2 |
| Regla de duración 17–20 min (2026-11-02, no retroactiva) + meta de guion + lista de reproducción Samu | §2.3, §6, §7.3 |
| Regla permanente prompts Gemini (2026-10-25) | §2.9, §5 |
| Regla de fuentes (2026-11-03): primero lo aprendido de él | §2.2, §5.8 |
| Temas virales (2026-11-04) + criterio comentarios + ranking | §5.6 |
| Música: lista, verificación, guion v3, voz, video v1 APROBADO, reserva Tlaxcala, miniatura oficial, publicada | §11.2 |
| Tragedias: título nuevo de los 90, lista, fuera por atribución, tensión del título, Gaviria/Avianca, guion v2, voz 17:36, video v2 APROBADO, miniatura oficial v10, Drive, descripción aprobada | §11.2, §10.3 |
| Dichos: título, lista final 12→1, guion v2, voz corregida 18:12, video v1 APROBADO, reserva de 6 fotos DUDOSA, miniatura sin aprobar | §11.2 |
| Canal publicado (12 videos, 631 subs, 159.435 vistas) + Platos Domingo duplicado | §11.1 |
| Feedback (142 comentarios): Navidad más querido, Marcas más corregido, Comerciales sin comerciales, IA criticada, 5 peticiones | §11.3 |
| Famosos: título, lista, reglas, Don Chinche, v3 con 10 fallos, retratos, Drive, miniatura v5, pendientes | §11.2, §11.5 |
| Regla Colombia siempre (2026-10-24) | §2.4, §8.4 |
| Regla de contexto (2026-10-25) | §2.5, §8.4 |
| Regla de extensión / descargas (2026-10-25) | §2.7, §12.1 |
| Regla de autoanálisis y arreglo (2026-10-25) | §2.6, §8.5 |
| Audio continuo (2026-10-22) | §2.8, §7.2 |
| Skool / segundo cerebro El Taller del Creador; Notion no conectado | §1 |
| Solo en local (cerebro, Marcas, miniatura oficial, ZIP del kit no en Drive) | §2.12 |
| Confirmación antes de agregar dato no presente en su CV | §2.24, §13.1 |
| Voz de narración: acento colombiano de Cali | §2.16, §7.1 |
| Modelos (orden permanente 2026-11-01): mejores modelos, puente OVH/Groq/OpenRouter, local qwen3.5:4b | §2.15, §12.1 |
| Decisión Guía Converzzo (2026-11-01): SÍ video largo, NO shorts/Cowork/ElevenLabs/HeyGen | §12.1 |
| Subida a remote-storage declinada (2026-11-03) | §2.11, §13.2 |
| Credencial Google desactualizada (2026-11-04), login en vivo completado | §2.13 |
| 10 temas nuevos (2026-11-02) + reservas + narcos en espera | §11.4 |
| Preferencia de formato: títulos sin comillas (2026-11-04) | §6.2 |

**Intencionalmente fuera de este documento (por alcance):** búsqueda de empleo (piso salarial $3.000.000, cargos, portales, PwC, Computrabajo), «Papás Primerizos» (Master Prompt v8.7, Fish Audio, 10 ideas, video 1), finanzas (Nu, PayPal). Si el nuevo chat necesita esos sistemas, se compilan por separado.

**Huecos declarados (nada oculto):** el libro de marca fija duraciones de formato (25–35 / 8–15 min) que la orden vigente de 17–20 min reemplaza (conflicto resuelto n.º 1); el estándar de edición del segundo cerebro (2026-10-22) se leyó pero su cola quedó truncada en la lectura — su contenido operativo está cubierto por REGLAS_DURAS y ESTILO_DOCUMENTAL_EXPEDIENTE; la lista completa de Marcas se tomó del guion del repo (`guion.txt`); los datos crudos del barrido amplio de temas están en `~/workspace/nostalgia_colombia/barrido_amplio/` y no se transcribieron íntegros aquí (el ranking y el criterio sí están, §5.6).

---

*Fin del KIT DE RÉPLICA TOTAL — La Chiva del Pasado. Compilado el 2026-11-05 desde las fuentes listadas en el encabezado. Cualquier cambio a este sistema se propone, se aprueba y se registra aquí antes de aplicarse — igual que en el libro de marca.*
