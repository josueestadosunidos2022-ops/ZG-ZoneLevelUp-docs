# ZoneLevelUp

## 2.0.0-beta29-r87 · Personajes y progresión / Characters and progression

### Español

- Los personajes nuevos empiezan en nivel 1, con su propia progresión. Los personajes anteriores conservan sus razas, oficios, clases, talentos y árboles. El inventario, el gremio y la cartera siguen asociados a la cuenta. Las razas de otros personajes de la cuenta quedan reservadas.
- El Atlas incluye cinco títulos acumulativos del Pacto y sus objetivos. Reclama el título en **Héroe → Logros** y equípalo en **Héroe → Títulos**.
- La clase Vampiro convierte al personaje cuando está instalado Vampirism y la elección cumple los requisitos. Los vampiros conservan su nivel. Los cazadores no cambian de facción automáticamente.
- `/zlevelhud ocultar` y `/zlevelhud mostrar` controlan el HUD local. El addon **PASIVE TREE beta2** añade un árbol independiente.

Instala los JAR r87 de cliente y servidor que correspondan. Minecraft 1.20.1, Forge 47.4.10 o posterior de la rama 47 y Java 17. ZoneCore 2.1.4 o posterior de la rama 2 es obligatorio en servidor. Protocolos de r87: 82 / 2 / 5.

### English

- A new character starts at level 1 with independent RPG progression. Previous characters retain their races, professions, classes, talents and skill trees. Inventory, guild membership and wallet are shared. Races used by the account's other characters are reserved.
- The Atlas has five cumulative Pact titles. Claim them under **Hero → Achievements** and equip them under **Hero → Titles**.
- With Vampirism installed, eligible Vampire class selections join its faction. Existing vampires keep their level. Hunters keep their faction.
- Use `/zlevelhud ocultar` and `/zlevelhud mostrar` to hide or show the local HUD. **PASIVE TREE beta2** adds an independent tree.

Install the matching r87 client and server JARs. Minecraft 1.20.1, Forge 47.4.10 or later in the 47 series, Java 17. The server requires ZoneCore 2.1.4 or later in the 2.x series. r87 protocols: 82 / 2 / 5.

### Archivos / Files

- [Servidor / Server](https://www.curseforge.com/minecraft/mc-mods/zonelevelup/files/9730336)
- [Cliente / Client](https://www.curseforge.com/minecraft/mc-mods/zonelevelup/files/9730354)
- [Notas de la versión / Release notes](RELEASE-2026-11-21-r87.md)

## Historial / Previous releases

## 2.0.0-beta29-r76 · Corrección de Ambidiestro / Ambidextrous fix

El botón **+1** del Atlas compra el rango de Ambidiestro. La tecla de arma secundaria intenta el ataque. Actualiza cliente y servidor juntos al protocolo 77.

The Atlas **+1** button buys the Ambidextrous rank. The offhand key attempts an attack. Update client and server together to protocol 77.

- [Cliente / Client](https://www.curseforge.com/minecraft/mc-mods/zonelevelup/files/9671991)
- [Servidor / Server](https://www.curseforge.com/minecraft/mc-mods/zonelevelup/files/9672005)
- [Notas e instalación / Release notes and installation](RELEASE-2026-11-17-r76.md)

## Versión anterior / Previous release · 2.0.0-beta29-r75 · Forge 1.20.1 · Java 17

### Español

Clasificación semanal y premios de gremios, nueva progresión de atributos, habilidades dracónicas y talentos de combate y recolección. El top semanal se abre desde el directorio de gremios.

Instala la pareja exacta r75 (protocolo 76), con ZoneCore 2.1.4–2.x en servidor. Compatible con ZGrimory beta5 y ZoneDungeons beta14.

### English

Weekly guild standings and rewards, updated attribute progression, Dragonkin abilities, and new combat and gathering talents. Guild standings are available from the guild directory.

Install the exact r75 pair (protocol 76), with ZoneCore 2.1.4–2.x on the dedicated server. Compatible with ZGrimory beta5 and ZoneDungeons beta14.

## Archivos r75 / r75 files

- [Servidor / Server](https://www.curseforge.com/minecraft/mc-mods/zonelevelup/files/9671051)
- [Cliente / Client](https://www.curseforge.com/minecraft/mc-mods/zonelevelup/files/9671064)

[Notas de versión / Release notes](RELEASE-2026-11-17.md)

<details>
<summary>Documentación de versiones anteriores / Earlier release documentation</summary>

## Historical notes · Latest update / Última actualización — 2.0.0-beta29-r75

Clasificación semanal y premios de gremios, nueva progresión de atributos, habilidades dracónicas y talentos de combate y recolección. El top semanal se abre desde el directorio de gremios.

Weekly guild standings and rewards, updated attribute progression, Dragonkin abilities, and new combat and gathering talents. Guild standings are available from the guild directory.

[Release notes / Notas de versión](RELEASE-2026-11-17.md)

RPG progression, races/classes, guilds, expeditions and character identity. r58 adds a new narrated rebirth chronicle and retains the recent class-awakening and expedition-continuity improvements.

Progresión RPG, razas/clases, gremios, expediciones e identidad. r58 añade crónica narrada de renacer y conserva mejoras recientes de despertar de clases y continuidad de expediciones.

## Historical notes · Current release / Entrega actual — 2026-11-08

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 2.0.0-beta29-r58 |
| Client / Cliente | 2.0.0-beta29-r58 |

**Protocol / Protocolo:** Main 60 / Celebrations 1; update both sides / Principal 60 / Celebraciones 1; actualizar ambos lados.

[Downloads / Descargas](https://www.curseforge.com/projects/1738050/files) · [Release / Novedades](RELEASE-2026-11-08.md) · [Configuration / Configuración](CONFIGURATION.md)

## English

Minecraft 1.20.1, Java 17; Forge 47.4.10+ when paired with Dungeons beta10. Install the exact r58 pair: do not mix r57 despite its same main protocol, or older r55/r56. Server requires Core 2.1.4–2.x. Ranks, Crates and Iron’s Spellbooks provide optional integrations. The default final awakening tier needs Dungeons beta10, or its dungeon-count requirement must be disabled.

r58 adds 24 rebirth chapters with 72 Spanish narrated acts, three original instrumental themes and synchronized 3D scenes. Music ducks during narration; existing unlocks and character progress remain. It includes three class-awakening tiers, same-session expedition respawn/reconnection, `/zsalir`, and inactive default loot sections for valid custom bosses. Use HÉROE→GODIELAND or `/zcine` for unlocked chapters, and RAZAS→CLASES→DESPERTAR for awakening. Install both r58 sides, main protocol 60/celebrations 1; server Core 2.1.4–2.x remains required. Dungeons beta10 works with this release. Audio plays from packaged local assets; no online narration service is needed. Laboratory rendering/audio checks do not certify full-modpack multiplayer gameplay.

Open HÉROE → GODIELAND to replay unlocked chapters. `/zcine` opens the section; existing administrative previews can inspect a chapter. Class awakening is under RAZAS → CLASES → DESPERTAR. Keep player/world data and current TOML.

## Español

Minecraft 1.20.1, Java 17; Forge 47.4.10+ con Dungeons beta10. Instala pareja r58 exacta: no mezcles r57 aunque comparta protocolo principal, ni r55/r56. Servidor requiere Core 2.1.4–2.x. Ranks, Crates e Iron’s Spellbooks aportan integraciones opcionales. Último despertar predeterminado necesita Dungeons beta10 o desactivar su requisito de mazmorras.

r58 añade 24 capítulos de renacer con 72 actos narrados en español, tres temas originales y escenas 3D sincronizadas. La música baja durante la voz; conserva desbloqueos/progreso. Incluye tres rangos de despertar, reaparición/reconexión en la misma expedición, `/zsalir` y secciones inactivas de botín para jefes válidos. HÉROE→GODIELAND o `/zcine` abre capítulos liberados; RAZAS→CLASES→DESPERTAR muestra ascensos. Instala ambos r58, protocolo 60/celebraciones 1 y Core 2.1.4–2.x solo servidor. Compatible con Dungeons beta10. Audio local incluido, sin servicio de narración online. Pruebas de render/audio de laboratorio no certifican gameplay multijugador del pack.

Abre HÉROE → GODIELAND para capítulos liberados. `/zcine` abre el apartado; previsualización administrativa permite revisar uno. Despertar está en RAZAS → CLASES → DESPERTAR. Conserva datos y TOML.

## Updating / Actualizar

Stop the affected instance, back up world/configuration and replace only the previous same-mod/same-side JAR. Keep one JAR per mod per instance and preserve player data. / Detén la instancia correspondiente, respalda mundo/configuración y sustituye solo el JAR del mismo mod y lado. Conserva un JAR por mod e instancia y los datos de jugador.

## Validation scope / Alcance de verificación

r58 includes code/timeline checks, 17 controlled real-render screenshots and 399 audio-engine checks without opening a gameplay world. Earlier r57 evidence covers 177 encounter/awakening checks and separate Corail interaction checks. These do not certify full-modpack multiplayer, combat interruption in a real session, production FPS/TPS or complete subjective audio listening.

r58 incluye pruebas de código/tiempos, 17 capturas reales controladas y 399 comprobaciones de audio sin abrir mundo de gameplay. r57 aporta 177 pruebas de encuentros/despertar e interacción Corail aparte. No certifican modpack multijugador, interrupción en combate real, FPS/TPS ni escucha subjetiva completa.

## Rights / Derechos

Original ZONE code/assets © Elgochogms; existing third-party licenses and notices remain applicable. Public documentation repository. / Código y recursos originales ZONE © Elgochogms; se conservan licencias y avisos de terceros. Repositorio de documentación pública.


## Previous documentation / Documentación anterior

[2026-11-06 release / Entrega 2026-11-06](RELEASE-2026-11-06.md). Version examples in historical releases remain historical. / Los ejemplos de versiones de entregas anteriores son históricos.

</details>
