# ZoneLevelUp — Configuration / Configuración (2026-11-06)

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 2.0.0-beta29-r55 |
| Client / Cliente | 2.0.0-beta29-r55 |

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

Commands require console, OP2 or `zonelevelup.bonus.admin`; targets must be online. / Requieren consola, OP2 o permiso y destinatarios conectados.

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

[Current release / Entrega actual](RELEASE-2026-11-06.md) · [README](README.md).
