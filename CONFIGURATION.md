# ZoneLevelUp — Configuration / Configuración (2026-11-08)

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 2.0.0-beta29-r58 |
| Client / Cliente | 2.0.0-beta29-r58 |

## Chronicle and audio / Crónica y audio

Client file `config/zonelevelup-client.toml`, section `[celebraciones_3d]`:

```toml
voz_cinematica = true
volumen_narrador = 0.75
musica_cinematica = true
volumen_musica_cinematica = 0.22
musica_durante_narracion = 0.36
movimiento_reducido = false
```

Volumes are 0–1. The ducking fraction is not an integer percentage:0.36×0.22=0.0792 during narration. Minecraft's Music volume also applies. Reduced motion limits camera effects. / Volúmenes 0–1; fracción musical no es porcentaje entero. También se aplica volumen Música de Minecraft; movimiento reducido limita cámara.

Server `config/ZONEMODS/zonelevelup/cinematicas.toml` retains `celebraciones_activas=true`, `intervalo_niveles=5` (1–10000), `reproducir_cinematica_al_reset=true`, `duracion_cinematica_segundos=30` (18–90). Duration is a minimum, extended to fit narration/pauses without cutting lines. Existing values are retained. / Duración es mínimo y se amplía para voz/pausas; no corta frases ni sobrescribe valores.

`/zcine` opens the chronicle. Existing administrative `/zcine previsualizar 1` can preview a chapter. Escape stops scene/audio; damage, death or dimension change interrupts it. Multiplayer continues while viewing; replaying does not grant progression. / Escape detiene escena/audio; daño, muerte o dimensión interrumpen. El mundo continúa y repetir no concede progreso.

## Class awakening / Despertar de clases

Server file `config/ZONEMODS/zonelevelup/clases-despertar.toml`; base passives remain in `clases.toml`. Reload with administrative `/zonelevelup reload`; invalid data keeps the last valid catalog. Exactly three tiers per combat class: Despierto, Ascendido, Trascendente. / Tres rangos por clase, recarga validada; inválido conserva catálogo.

| Requirement / Requisito | Despierto | Ascendido | Trascendente |
|---|---:|---:|---:|
| Character level / Nivel |20|60|100|
| Class actions / Acciones |25|100|250|
| Claimed contracts / Contratos cobrados |3|10|20|
| LevelUp arena bosses / Jefes de arena |0|2|5|
| Completed expeditions / Expediciones |0|1|3|
| Completed MasmorrasZ / Mazmorras |0|0|2|
| Passive multiplier / Multiplicador de pasivas |1.25|1.5|1.8|

Counters accumulate per character/class and are not spent. Only active-class activities count; characters do not share progress. Awakening costs no money, cannot skip tiers and requires being out of combat and outside a MasmorrasZ queue/run. / Contadores por clase/personaje, acumulativos sin gastar; no se comparten. Sin coste monetario ni saltos, fuera de combate y cola/partida.

Each `[clases.<id>.rango_<1-3>]` includes `nivel_minimo`, `actividad`, `acciones_clase`, `contratos_cobrados`, `jefes_derrotados`, `expediciones_completadas`, `masmorras_completadas`, `multiplicador_pasivas`, `vida_extra`, `armadura_extra`. Zero counters disable that requirement; set `masmorras_completadas=0` where desired without Dungeons. Later requirements/benefits cannot be lower than prior tiers. / Cero desactiva requisito; sin Dungeons ajusta mazmorras. Rangos posteriores no pueden rebajar requisitos/beneficios.

Bounds: level 1–10000; counters 0–1000000; multiplier 1–3; extra health 0–100 points; armor 0–20. Only the highest achieved tier applies, not all three summed. Two health points equal one heart; increasing maximum health does not heal. / Límites indicados; solo rango más alto, sin suma. Dos puntos de vida son un corazón; aumentar máximo no cura.

`[opciones] activo=true` and `conservar_ascension_anterior=true` preserve/import completed old class trials once without repeating old XP. Rebirth retains awakening ranks/counters; passives wait until the class is active again. Save failures restore the previous rank in memory. / Conserva/importa prueba antigua una vez sin repetir XP; renacer conserva rangos y espera clase activa. Fallo de guardado revierte rango.

## Boss rewards / Premios de jefes

`config/ZONEMODS/zonelevelup/jefes/botin.toml` and `cofres.toml` now add missing sections for valid custom templates at startup or `/zonelevelup boss reload`. Sections use template ID, not necessarily mob/arena ID. New examples have zero probability and remain inactive; existing entries/comments are retained. / Completa secciones por ID de plantilla, con ejemplos inactivos y conservación de entradas/comentarios.

`botin.toml` is personal eligible-player loot; `cofres.toml` adds independent rolls or shared reserve. Activating the same reward in both creates two rolls. Probability1.0=100%,0.01=1%,0.001=0.1%. `/zonelevelup boss botin <arena>` reads the personal table; real encounters use boss activar, while boss invocar is a reward-free test. / Tablas independientes pueden duplicar tiradas deliberadamente; invocar no premia.

## Expeditions / Expediciones

Existing files under `config/ZONEMODS/zonelevelup/Expedicion/` remain. Native respawn keeps the same live session and its deadline, with five seconds of ordinary-damage protection. `/zsalir` explicitly exits; disconnecting while queued cancels entry, while disconnecting in combat retains a place only while that session lives. Restart does not reconstruct an old expedition fight; saved membership recovers the player to Overworld spawn. / Reaparición conserva sesión/plazo, cinco segundos de protección; reinicio no reconstruye combate y recupera al spawn.

Corail grave recovery keeps Corail ownership/inventory rules. External teleport restrictions do not automatically refund charges made by another mod before cancellation. Maintain safe entrance coordinates; administrative `/zlevel expedicion estado <arena>` and `cancelar <arena>` remain. / Respeta reglas Corail; cancelar viaje no revierte automáticamente cobros externos. Conserva entrada segura y comandos administrativos.


## Rank benefits / Beneficios de rango

`config/ZONEMODS/zonelevelup/bonos-rangos.toml` discovers real ZoneRanks IDs every 60 seconds or with `/zlevel bonus recargar`, preserving edited values/comments. Only the current assigned rank applies; OP and inherited permissions do not add rank bonuses. / Descubre IDs cada 60 segundos o al recargar, conservando valores/comentarios. Solo se aplica el rango actual.

All initial benefits are zero. Root `habilitado = false` disables automatic rank benefits and gifts; manual bonuses remain. Invalid reloads retain valid settings. / Todos empiezan en cero; deshabilitar afecta automáticos y regalos, no manuales. Recarga inválida conserva lo válido.

| Key / Clave | Combined limit / Límite combinado | Meaning / Uso |
|---|---|---|
| `xp_porcentaje` | 0–1000% | General LevelUp XP; excludes vanilla and administrator XP gifts / XP general RPG |
| `xp_mobs_porcentaje` | 0–1000% | Hunting/boss XP, per recipient after group split / Caza y jefes tras reparto |
| `runas_porcentaje` | 0–100% | Relative rune chance increase / Aumento relativo de probabilidad |
| `monedas_tiempo_extra` | 0–1000 GC | Extra physical coins per existing journey cycle / Monedas físicas adicionales por ciclo |
| `vida_porcentaje` | 0–200% | Maximum-health attribute; does not heal / Salud máxima; no cura |
| `defensa_porcentaje` | 0–100% | Armor attribute; not direct damage reduction / Armadura; no reducción directa |
| `dano_porcentaje` | 0–100% | Attack-damage attribute / Atributo de ataque |
| `velocidad_porcentaje` | 0–30% | Movement, not attack speed / Movimiento, no velocidad de ataque |
| `mana_porcentaje` | 0–300% | Iron’s Spellbooks maximum mana / Maná máximo de ese mod |
| `poder_magico_porcentaje` | 0–100% | Iron’s Spellbooks spell power / Poder mágico de ese mod |

Example: +8% runes changes `1/1000` to `1.08/1000`, not `8/1000` or +8 percentage points. A disabled zero chance stays zero. / +8% cambia `1/1000` a `1.08/1000`, no a `8/1000` ni suma ocho puntos porcentuales; cero sigue cero.

## One-time gifts / Regalos únicos

Each `[[rangos]]` section has its real `id` and `version_regalos = 1`. Gift maxima per grant: `regalo_xp` 1000000, `regalo_niveles` 10000, `regalo_talentos` 10000, `regalo_atributos` 10000, `regalo_godiecoins` 1000000 virtual GC. / Cada sección usa ID real y versión; esos son los máximos por entrega.

Receipts are per account + rank ID + gift version. Death, reconnecting, character switching or regaining a rank does not repeat that version. Raising the version permits all positive gifts in that section again; changing quantities alone does not. XP/levels/talents/attributes belong to the receiving active character. / Recibos por cuenta, rango y versión; no se repiten al morir, entrar, cambiar personaje o recuperar rango. Aumentar versión vuelve a habilitar todos sus regalos positivos; cambiar cantidades no. Los regalos RPG corresponden al personaje activo receptor.

Commands require console, OP 2 or `zonelevelup.bonus.admin`; targets must be online. / Requieren consola, OP 2 o permiso y destinatarios conectados.

```text
/zlevel bonus agregar xp_porcentaje 8 NombreJugador
/zlevel bonus establecer xp_porcentaje 12 NombreJugador
/zlevel bonus listar NombreJugador
/zlevel bonus quitar xp_porcentaje NombreJugador
/zlevel bonus quitar todos NombreJugador
/zlevel bonus recargar
```

`agregar` adds a manual active bonus; `establecer` replaces it. With `regalo_*`, either command grants immediately on every execution. `quitar` removes manual active bonuses only, not rank benefits or permanent gifts. / Agregar suma y establecer sustituye; para `regalo_*`, ambos entregan cada vez. Quitar solo retira bonos manuales activos.

## Portraits / Retratos

`config/ZONEMODS/zonelevelup/retratos.toml`:

```toml
habilitado = true
precio_normal = 500
precio_legendario = 1000
```

Prices are integer virtual GC, 0–1000000. Disabling purchases preserves ownership/equipping. Re-equipping an owned portrait does not charge again; USAR MI SKIN is free. / Precios enteros GC virtuales; deshabilitar conserva propiedad/equipamiento. No se vuelve a cobrar lo adquirido; usar skin es gratis.

Local HUD position/scale remain in `config/ZONEMODS/zonelevelup/client-hud.toml`. Back up player data: identity is account-level `ZoneJourneyAccount.Identity`, with attribute gifts also stored on the receiving character. / El HUD conserva su TOML; respalda datos de jugador y personaje.

[Current release / Entrega actual](RELEASE-2026-11-08.md) · [README](README.md).
