# ZoneLevelUp

## Current update / Actualización actual — 2026-10-23

Protected public builds prepared for Minecraft 1.20.1 / Forge 47.4.x / Java 17. Files become available after CurseForge approval. / Compilaciones públicas protegidas; los archivos estarán disponibles cuando CurseForge los apruebe.

Operational beta29-r28: combat-balance TOML, character mastery, rune codex discoveries, weekly expedition routes, configurable client HUD and a ritual boss template. Includes the earlier rune fusions and Spanish dialogue audio. Main protocol 42 / story protocol 3: replace BOTH sides with r28. Dedicated servers need ZoneCore 2.1.4+.

| Side / Lado | Version / Versión | File / Archivo |
|---|---|---|
| server | 2.0.0-beta29-r28 | `zonelevelup-2.0.0-beta29-r28-server-protected.jar` |
| client | 2.0.0-beta29-r28 | `zonelevelup-2.0.0-beta29-r28-client-protected.jar` |

Install only the JAR for each side; never put both side JARs in one mods folder. Back up the world and preserve existing player data and TOML files. / Instala solo el JAR correspondiente a cada lado; conserva mundo, progreso y TOML existentes.

**server dependencies / dependencias:** ZoneCore: Required Dependency ([2.1.4,3)); ZoneCrates: Optional Dependency (server wallet integration).

**client dependencies / dependencias:** ZoneCrates: Optional Dependency (server wallet integration).

Archive checks and isolated dedicated-server startup do not certify graphical gameplay, real multiplayer or the full modpack. / Las verificaciones de archivo y arranque aislado no certifican cliente gráfico, multijugador real ni modpack completo.

## Earlier reference / Referencia anterior

The following reference predates this update. Use the current versions and side instructions above when they differ. / La referencia siguiente es anterior; prevalecen las versiones y las indicaciones de lado de esta actualización.

## Update / Actualización — 2026-10-17

Selected version / Versión seleccionada: **universal 2.0.0-beta29-r10**. New file availability depends on CurseForge approval / La disponibilidad de los archivos nuevos depende de su aprobación en CurseForge.

See [changes, exact files and installation](UPDATES-2026-10-17.md) / Consulta [cambios, archivos e instalación](UPDATES-2026-10-17.md). Preserve the world and TOML files / Conserva mundo y TOML.

## English

RPG levels, classes, races, talents, party missions and bosses. Minecraft 1.20.1 / Forge 47.x. Current protected universal release: **2.0.0-beta29-r10** for client and server. Keep it separate from stable 1.5.0-r2.

### Installation

Install the same universal release JAR on client and server. Do not install development or test JARs. The server requires **ZoneCore 2.1.2+**. This beta was built and started with protected Core 2.1.3. Optional integrations with Iron's Spellbooks, Vampirism, Simply Swords, ZoneCrates and ZoneProtes need their own matching installations.

### Configuration

Edit generated TOML files while the server or game is stopped unless a documented reload command is available. Back up persistent data before updates.

| Config file | Use |
|---|---|
| `general.toml` | Verify the exact generated path and options for the selected release. |
| `clases.toml` | Verify the exact generated path and options for the selected release. |
| `razas.toml` | Verify the exact generated path and options for the selected release. |
| `talentos.toml` | Verify the exact generated path and options for the selected release. |
| `party.toml` | Verify the exact generated path and options for the selected release. |
| `misiones-party.toml` | Verify the exact generated path and options for the selected release. |
| `jefes/jefes.toml` | Verify the exact generated path and options for the selected release. |
| `compatibilidad.toml` | Verify the exact generated path and options for the selected release. |

See [configuration reference](CONFIGURATION.md) for keys detected in source and [release compatibility](RELEASES.md) for version-pair rules.

## Español

Niveles RPG, clases, razas, talentos, misiones de equipo y jefes. Minecraft 1.20.1 / Forge 47.x. Entrega universal protegida actual: **2.0.0-beta29-r10** para cliente y servidor. Mantenla separada de estable 1.5.0-r2.

### Instalación

Instala el mismo JAR universal en cliente y servidor. No instales JAR de desarrollo ni de pruebas. El servidor requiere **ZoneCore 2.1.2+**. Esta beta se compiló y arrancó con Core 2.1.3 protegido. Las integraciones opcionales con Iron's Spellbooks, Vampirism, Simply Swords, ZoneCrates y ZoneProtes requieren sus propias instalaciones compatibles.

### Configuración

Edita los TOML generados con el servidor o juego detenido, salvo que exista un comando de recarga documentado. Respalda los datos persistentes antes de actualizar.

| Archivo de configuración | Uso |
|---|---|
| `general.toml` | Comprueba la ruta y opciones generadas de la entrega elegida. |
| `clases.toml` | Comprueba la ruta y opciones generadas de la entrega elegida. |
| `razas.toml` | Comprueba la ruta y opciones generadas de la entrega elegida. |
| `talentos.toml` | Comprueba la ruta y opciones generadas de la entrega elegida. |
| `party.toml` | Comprueba la ruta y opciones generadas de la entrega elegida. |
| `misiones-party.toml` | Comprueba la ruta y opciones generadas de la entrega elegida. |
| `jefes/jefes.toml` | Comprueba la ruta y opciones generadas de la entrega elegida. |
| `compatibilidad.toml` | Comprueba la ruta y opciones generadas de la entrega elegida. |

Consulta la [referencia de configuración](CONFIGURATION.md) para claves detectadas en el código y la [compatibilidad de entregas](RELEASES.md) para las parejas de versiones.

## Ownership / Titularidad

Documentation and original ZONE visual assets © Elgochogms. This repository contains documentation and a project avatar only; it does not distribute mod source code, private mappings, server secrets or production configuration.
