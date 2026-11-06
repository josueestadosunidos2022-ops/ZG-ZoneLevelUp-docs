# ZoneLevelUp

RPG progression, character identity, guilds and a customizable HUD. r55 adds rank benefits and an account-wide portrait collection.

Progresión RPG, identidad, gremios y HUD personalizable. r55 añade beneficios de rango y colección de retratos compartida por cuenta.

## Current release / Entrega actual — 2026-11-06

Minecraft **1.20.1**, Forge **47.x** (47.4.x for this release set), Java **17**. File availability follows CurseForge approval. / Disponibilidad de archivos según aprobación de CurseForge.

| Side / Lado | Version / Versión |
|---|---|
| Server / Servidor | 2.0.0-beta29-r55 |
| Client / Cliente | 2.0.0-beta29-r55 |

**Protocol / Protocolo:** LevelUp 58 / Identity 1 / Guilds 1 / Journey 1.

[Downloads / Descargas](https://www.curseforge.com/projects/1738050/files) · [Release guide / Guía de novedades](RELEASE-2026-11-06.md) · [Configuration / Configuración](CONFIGURATION.md)

## English — Requirements and quick start

Install r55 on BOTH sides; no r54. Server: ZoneCore 2.1.4–2.x. Optional: Ranks server 3.3.13 for automatic benefits (existing client 3.3.6 remains compatible if used), Crates for purchases and Iron’s Spellbooks for magic. Retain compatible Economy beta8 if installed.

Open HÉROE → IDENTIDAD → RETRATOS or BONOS ACTIVOS. Administrators configure the two TOML files and apply `/zlevel bonus recargar`. Automatic benefits start at zero; normal players cannot grant themselves bonuses.

### What changed

- Configurable current-rank benefits, persistent manual bonuses and one-time gifts with account/rank/version receipts.
- Thirty original portraits: 24 normal and six legendary, with shared ownership, purchase confirmation and client-animated legendary effects.
- Identity screens explain active bonuses; the midnight-blue, purple and cyan HUD shows portrait, level, server rank and benefit glyphs.

## Español — Requisitos e inicio

Instala r55 en AMBOS lados; no r54. Servidor: ZoneCore 2.1.4–2.x. Opcionales: Ranks servidor 3.3.13 para bonos automáticos (cliente 3.3.6 compatible si se usa), Crates para compras e Iron’s Spellbooks para magia. Conserva Economy beta8 compatible si está instalado.

Abre HÉROE → IDENTIDAD → RETRATOS o BONOS ACTIVOS. Administración configura ambos TOML y aplica `/zlevel bonus recargar`. Los bonos automáticos empiezan en cero; un jugador normal no puede concedérselos.

### Novedades

- Beneficios configurables del rango actual, bonos manuales persistentes y regalos únicos con recibos por cuenta/rango/versión.
- Treinta retratos originales: 24 normales y seis legendarios, propiedad compartida, confirmación de compra y efectos legendarios animados en cliente.
- Identidad explica bonos activos; el HUD azul oscuro, morado y celeste muestra retrato, nivel, rango e iconos de beneficios.

## Updating / Actualizar

Stop the affected instance, back up world/configuration, replace only the previous same-mod/same-side JAR and retain player data. Never install the dedicated and client JARs of one mod together. / Detén la instancia correspondiente, respalda mundo/configuración y sustituye solo el JAR del mismo mod y lado conservando datos. Nunca instales juntos los JAR dedicado y cliente del mismo mod.

## Validation scope / Alcance de verificación

The delivery records 44 isolated server checks, 73 guild regressions and 26 real-render laboratory screenshots. Rank API preservation was inspected. Full modpack gameplay, Iron’s Spellbooks runtime and production FPS/TPS remain unverified.

La entrega registra 44 comprobaciones de servidor aislado, 73 regresiones de gremios y 26 capturas de render real con datos de laboratorio. API de rangos inspeccionada. No verifica modpack completo, Iron’s Spellbooks en ejecución ni FPS/TPS de producción.

## Rights / Derechos

Original ZONE code and assets © Elgochogms; existing licenses and third-party notices remain applicable. This repository provides public documentation. / Código y recursos originales ZONE © Elgochogms; se conservan licencias y avisos de terceros. Este repositorio contiene documentación pública.
