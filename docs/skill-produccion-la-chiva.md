# La Chiva del Pasado Channel Production

## Start from the settled brand book and elicit what is still open

- Read the latest version of the brand book in `~/workspace/your_files/libro-marca-nostalgia-colombia/` before drafting anything and treat it as the source of truth for identity, tone and format.

- Use La Chiva del Pasado as the channel name and keep La Colombia Que Fue only as the backup name.

- Never present a channel name as available without verifying it first, and never rename the channel without the user approving the new name.

- Use the user original logo as the profile image and do not substitute generated alternatives for it.

- Keep the route framing from the book, where each item in a list video is a parada and the opening line is Súbete, que nos vamos al pasado.

- List the decisions that are still open before producing a large deliverable such as a book version, a topic ficha or a full script, and ask about them in one short numbered list.

- Cover name, focus scope, audience, epoch window and output format in that list whenever they are not already settled in the brand book.

- Ask about format in concrete terms, such as paragraphs or lines and how many of each per item, instead of assuming a layout.

- Use an asset, name or list the user supplies as the working version and offer alternatives only as support material, never as a silent replacement.

- Stop at the script and wait for the user approval before moving to voice or production, as the toys script stayed pending until he approves it.

## Test every topic and claim

- Apply the lived memory test to every topic, which asks whether Colombians of the era actually lived and remember that experience.

- Keep the focus broad across sweets, fashions, toys, outings, festivities, Christmas, gifts, traditions, dances, customs, transport, street games, school, Colombian telenovelas and Colombian films, alongside family memories such as sayings, the grandparents house and food.

- Treat family as the emotional centre and the tone of the channel, never as a literal filter that excludes a topic with a lived memory behind it.

- Keep the channel epoch from the 1970s to the 2000s and prefer the 1980s to the 2000s for toy lists, keeping an older item only when the user decides the exception, as he did with Mi Adorable Angelino.

- Address one single unified audience, Colombians who lived the Colombia of the 1980s to the 2000s and are today mostly 35 to 65 or older, in Colombia or abroad, and never split it into a table of segments.

- Verify nostalgic facts with sources before writing them and drop an item that lacks a sufficient source instead of filling the gap from memory.

- Present dichos and agüeros only as recurring colour, through El dicho de la ruta and El agüero de la parada, and label agüeros with the CREENCIA POPULAR seal so they are never presented as verified fact or given an invented origin.

## Write scripts in the approved format

- Write each parada as a small prose script of exactly 11 short paragraphs, never as numbered loose lines.

- Count the paragraphs per parada and in total with `muse.exec` before delivering, so a 25 parada script shows 275 paragraphs.

- Write in the first person plural voice of the audience remembering, with names and expressions from the era.

- Build each parada on lived microdetails of use, such as how a toy wore out, who handed it down or where a child kept it, rather than on factory data or a cold industrial angle.

- Mention brands and products only inside everyday use and the trust families placed in them.

## Package titles and thumbnails

- Build list titles with the verified formula of number plus tangible category plus anchor plus a clause of loss, and keep them near the reference median length.

- Build the thumbnail on the same title formula, with a Colombian scene crowded with at least 8 to 10 visible period brands, as the official Marcas thumbnail does with its storefront. This supersedes the earlier white strip formula.

- Validate each thumbnail against the reference-channel teardown in the second brain: adapt a validated reference thumbnail instead of copying it, and check the red urgency block and the contrast at the real display sizes.

- When he rejects assistant-generated thumbnails, hand him the modeling prompt instead of another version. Name the validated reference thumbnail it adapts, the Colombian setting and the minimum brand count, so he generates the official in ChatGPT himself.

- Check the finished banner or thumbnail at the real display sizes and keep the critical content inside the central safe zone before delivering it.

- Improve an approved thumbnail only by direct editing and never by regenerating the whole image.

- Keep every approved product, brand, person, pose and composition unchanged in a quality pass, and change only sharpness, face clarity and the title treatment.

- Keep the title font and background identical to the approved version, so a quality pass does not restyle the title.

- Before delivering an improved thumbnail, check each item in the approved version against the new version and report any missing item instead of delivering it as approved.

## Produce the edit under the pilot gate

- Read the production standard in `~/workspace/segundo-cerebro-taller-del-creador/outputs/2026-10-22-sistema-edicion-la-chiva-v1.md` before editing, and keep its pulse, hard cuts, single graphic system and credit seals.

- Search for real material of exactly what the narration names, and never fill a gap with evocative or context-only imagery. The Granahorrar manada evocativa shot was rejected for this reason.

- When no real material exists for a named item, hold the previous real shot or show the ficha alone, and report every gap to the user BEFORE editing so he decides how to handle it.

- Cut every silence from the narration, between phrases, blocks and paradas, so the voice stays continuous with no dead air.

- Rebuild graphics at the reference scale: big centered FILE card, the name typed large for 3 to 4 seconds, the data figure at 25 percent of the screen height, and huge impact words.

- Approve every graphic BY STILLS with the user before any render, and never render a full video on unapproved graphics.

- Run the pilot gate: produce ONE parada first, get his approval, and only then redo the full video. Conavi was the proposed pilot because its real 1989 commercial exists.

## Available connectors

- Use `muse.connector_search` to find other connectors and `muse.skill_search` to find related skills.

- If nothing here fits, look on the web for a maintained API or MCP server and set it up with [Custom Connectors and MCPs](/opt/muse/skills/custom-connector-setup/SKILL.md), or build a custom connector.

## Websites

- [Cuando México Fabricaba de Todo](https://www.youtube.com/@CuandoMexicoFabricabadeTodo/videos) for the reference channel format the user chose to adapt. Carry the channel handle into `browser.spawn_task` to inspect titles and thumbnails visually, and verify counts and statistics through the YouTube Data API connector instead.

## Alternatives for better results

- Deliver one parada as a sample in the exact approved format before writing a full script, so a format correction costs one item instead of the whole document.

- Reuse the current brand book version as the checklist for each new deliverable and record a user correction in the book first, then apply it to the piece in progress.
