ZONELEVELUP beta29 r54 — GREMIOS DE GODIELAND
Minecraft 1.20.1 / Forge 47 / Java 17

1. INSTALACIÓN DE ESTA ACTUALIZACIÓN

- CLIENTE: zonelevelup-2.0.0-beta29-r54-client.jar
- CLIENTE: zoneeconomy-client-1.4.0-beta7.jar (también incluido en CLIENTE).
- SERVIDOR: zonelevelup-2.0.0-beta29-r54-server.jar
- Para contar intercambios de las pruebas de ascenso, instala también en el
  servidor zoneeconomy-server-1.4.0-beta7-gremios1.jar, sustituyendo su JAR
  anterior. No pongas ambos ZoneEconomy de servidor a la vez.
- ZoneEconomy necesita su componente de cliente para poder conectarse y
  mostrar las pantallas. Si no lo tenías, instala el JAR de cliente incluido
  en el Minecraft de cada jugador. El cliente de economía va solo en los PC;
  el servidor conserva zoneeconomy-server-1.4.0-beta7-gremios1.jar.
  El parche de servidor no cambia el protocolo de red de beta7.

ZoneLevelUp r54 exige su pareja exacta en ambos lados: protocolo principal 57,
canal Gremios 1 y Journey 1. No mezcles cliente r53/r52 con servidor r54.
Sustituye los archivos con las instancias cerradas y conserva mundo, datos de
jugadores, personajes y TOML. Hay un respaldo de las fuentes anteriores.
Esta entrega no instala ni reinicia tu servidor. La prueba beta30 de modelos
permanece separada. Se conserva PartyService.onlineMembers de r53 para las
integraciones existentes; ZoneDungeons beta9 admite r54 en su rango declarado.

2. DÓNDE ESTÁ EL GREMIO

Atlas de ZoneLevelUp > MUNDO > GREMIO.
También puedes buscar «gremio», «GODIE», «bandera» o «supremium» en el buscador.
Comando directo: /zgremio

El folio tiene seis pestañas:
GREMIO: resumen y beneficios personales.
MIEMBROS: invitaciones, cargos, expulsión y transferencia de liderazgo.
DIARIAS: lista desplazable, filtro de rango, objetivos, entrega y reclamación.
ASCENSO: pruebas individuales y botón ASCENDER.
CHAT: canal privado y canal compartido entre todos los gremios.
HERÁLDICA: nombre, color e insignia; color personal del mensaje en SUPREMIUM.

3. COLOCAR A GODIE (ADMINISTRADOR)

Sitúate donde deba quedarse el NPC y ejecuta:
  /zgremio npc crear

GODIE queda anclado a esa posición y orientación. No camina, no recibe daño,
no se empuja ni cambia de dimensión. Permanece guardado al descargar el chunk
y al reiniciar, sin mantenerlo cargado. No tiene aparición natural.

Para reubicar al GODIE más cercano (a menos de 8 bloques):
  /zgremio npc mover
Se coloca en tu posición actual.

Para retirarlo:
  /zgremio npc quitar

Puedes colocar varios NPC en lugares separados. Comparten el tablón y las
reglas del servidor: no generan una copia adicional de las recompensas.
Clic derecho con la mano principal abre el folio en DIARIAS.

Skin: copia exacta de la imagen que proporcionaste,
gold-accents-knight-24426011.png. Usa el cuerpo clásico de Steve con brazos
anchos y sus capas exteriores; no se aplica una cabeza o ropa por encima.
SHA256 de la skin:
4362e4c0025662d4b4c2ea4995d1c11a44abb48bd8eb8cc9da64b6b82b0ce45c

4. FUNDAR E INVITAR

Abre GREMIO sin pertenecer a uno, escribe un nombre de 3 a 24 caracteres,
elige uno de los 16 colores y una insignia. Pulsa FUNDAR GREMIO.
La fundación es gratuita. El nombre debe ser único y admite letras, números,
espacios, guion y guion bajo. Se rechazan códigos de formato y texto oculto.

Hay ocho insignias de estandarte: torre, espada, lobo, hoja, llama, estrella,
dragón y yunque. El líder puede cambiarlas después en HERÁLDICA.

La membresía es por cuenta UUID: cambiar de personaje no permite ocupar dos
gremios simultáneamente. El gremio persiste al desconectarse.

Máximo: cinco personas. Cargos:
  1 LÍDER: invita, expulsa, nombra oficial, transfiere, edita y disuelve.
  1 OFICIAL: invita y expulsa subordinados; no puede expulsar al líder.
  3 SUBORDINADOS: participan en misiones y chats.
Al nombrar otro oficial, el anterior vuelve a subordinado.

Invitar desde MIEMBROS o con:
  /zgremio invitar NombreJugador
El invitado usa:
  /zgremio aceptar
  /zgremio rechazar
También puede pulsar [ACEPTAR] en el chat o usar la interfaz.
La invitación dura 60 segundos por defecto. La capacidad se comprueba otra
vez al aceptar: una invitación pendiente no permite entrar como sexto miembro.

Para salir:
  /zgremio salir
El líder debe transferir antes si quedan otros miembros. Disolver y transferir
desde la interfaz exigen pulsar dos veces la misma acción en cinco segundos.
Salir o cambiar de gremio conserva el rango individual y sus reclamaciones;
los beneficios dejan de aplicarse mientras no pertenezcas a ningún gremio.

5. RANGOS INDIVIDUALES (DECISIÓN CONFIRMADA)

Cada personaje tiene sus propias pruebas. Que el líder ascienda no sube al
resto. Los avances se conservan al morir y al hacer RESET de nivel.
Un personaje nuevo empieza sus avances desde cero, dentro del mismo gremio.

Rango       XP por matar mobs  Pago por tiempo       Otros beneficios
HIERRO      +3%                base de viaje.toml
PLATA       +5%                base de viaje.toml
ORO         +7%                base de viaje.toml
DIAMANTE    +10%               base de viaje.toml
PLATINO     +10%               base de viaje.toml     Valor confirmado contigo
NETHERITA   +10%               al menos 7 GC/ciclo
SUPREMIUM   +13%               al menos 10 GC/ciclo   +3 atributos una sola vez
                                                     y color de mensajes

La XP de gremio se aplica a bajas, incluidos los jefes de ZoneLevelUp, y a tu
parte de la XP compartida por ZParty/expedición. No multiplica por sí misma
la XP de entregar misiones ni los premios administrativos.
Ejemplo: 100 XP por una baja se convierten en 103 con HIERRO, antes de los
otros bonos de raza, reset, comida u otros sistemas existentes.

El pago por tiempo usa el mismo contador de viaje.toml: por defecto cada
cinco minutos. No crea un segundo pago paralelo. Se usa el mayor importe
entre el pago base del servidor y el de tu rango. Si la base es 5, NETHERITA
paga 7 y SUPREMIUM 10. Si el inventario está lleno, las monedas físicas
siguen pendientes según el sistema existente y se entregan cuando haya espacio.

Los tres atributos de SUPREMIUM son un regalo permanente por personaje,
no un pago diario. No se repite al reconectar, cambiar de gremio o hacer reset.

6. LAS 70 MISIONES DIARIAS

Cada rango desbloquea 10 adicionales, acumulándose:
HIERRO 10 / PLATA 20 / ORO 30 / DIAMANTE 40 / PLATINO 50 /
NETHERITA 60 / SUPREMIUM 70.

En cada grupo hay cuatro cacerías, tres encargos de flores y tres de metales.
Los objetivos proceden de Cataclysm, DivineRPG, Alex's Mobs, Botania,
Mekanism y Create. Se verificaron sus 70 IDs contra los assets del modpack.
Al iniciar, el servidor también comprueba los registros reales de objetos
y entidades. Si falta el mod de un objetivo, esa misión muestra el motivo
y queda bloqueada; nunca se sustituye silenciosamente por un mob vanilla.

Cada diaria paga inicialmente 25 GodieCoins virtuales y 150 XP base.
El TOML permite cambiar los importes por misión. El pago usa la misma
billetera de ZoneCrates que ya emplea ZoneLevelUp.

CAZA: se cuenta la baja atribuida al jugador, incluidos propietarios
reconocidos de mascotas/proyectiles. Los compañeros no reciben esa baja
individual solo por estar en el gremio.

RECOLECCIÓN: lleva los objetos a GODIE, selecciona el encargo y pulsa
ENTREGAR. Se consume exactamente lo entregado, hasta cubrir lo pendiente.
Se permiten entregas parciales. Una entrega repetida no consume extras.
Después pulsa RECLAMAR para cobrar la misión completada.

Es necesario estar vivo, fuera de creativo/espectador y cerca de GODIE para
entregar o reclamar. La distancia inicial es 8 bloques, configurable.
Abrir el Atlas desde lejos permite consultar el progreso, pero no entregar.
Si falla el guardado de una entrega, se restauran materiales y progreso.
Las reclamaciones quedan registradas y no se vuelven a pagar al repetirlas.

Las diarias cambian a medianoche en America/New_York por defecto. El folio
muestra el tiempo restante y la zona horaria. Al cambiar de día se reinician
los contadores diarios, incluidas entregas parciales y reclamaciones.
No se reinician rangos ni pruebas de ascenso. Un reloj que retrocede no
reabre automáticamente un día ya registrado.

7. CÓMO ASCENDER

Solo cuentan las pruebas del siguiente rango: no se acumulan para todos
los rangos futuros a la vez. Hay siete pruebas por ascenso (42 en total).

Destino      Expediciones  Jefes  Criaturas  Metal de Botania  Estructuras  Tratos
PLATA        1             1      2          16 manacero       1            2
ORO          2             2      3          32 manacero       2            3
DIAMANTE     3             3      4          48 manacero       3            4
PLATINO      4             4      5          64 elemento       4            5
NETHERITA    5             5      6          80 elemento       5            6
SUPREMIUM    6             6      7          96 elemento       6            7

Cada ascenso exige además 1.800 segundos (30 minutos) acompañado en ZParty.

Detalles:
- Expedición: completar una expedición de ZoneLevelUp y recibir su registro
  de finalización. Entrar y salir inmediatamente no cumple la prueba.
- Jefe: victoria reconocida por el sistema de jefes de ZoneLevelUp. Usa el
  ID de la definición del jefe si configuras uno concreto, o "*" para cualquiera.
- Criaturas: observar individuos diferentes con línea de visión a 20 bloques.
  PLATA/ORO piden Deeplings; los siguientes rangos, Ignited Revenants.
  El chequeo es cada cinco segundos, con un máximo de 32 mobs por revisión.
- Estructuras: entrar en estructuras diferentes, identificadas por dimensión,
  tipo y chunk de origen. Pasear por distintas partes de la misma no la duplica.
  No se cargan estructuras lejanas para buscar objetivos.
- Entregas: consumen objetos como las diarias. Las pruebas permanentes no
  pierden sus entregas por cambiar de día.
- Intercambios: usar /intercambio Jugador (también /intercambiar o /tradear)
  y terminar la transacción con bienes o monedas. Cancelaciones, ofertas vacías
  o simplemente abrir el menú no cuentan. Se acredita como máximo un trato
  con el mismo socio por día para cada prueba.
- ZParty: ambos deben estar conectados, vivos, en la misma dimensión y a
  50 bloques o menos. Puede ser alguien de otro gremio. El tiempo es acumulado;
  no exige 30 minutos seguidos. Estar solo en el servidor no lo aumenta.

Al cumplir las siete, acércate a GODIE y pulsa ASCENDER. Se aplica el rango,
suena la confirmación y se habilitan diez diarias más.
Si falta un mod requerido en una prueba, el administrador debe corregir su
objetivo en TOML; no se concede un ascenso incompleto automáticamente.

8. CHAT

Privado: /zgremio chat Mensaje
Global de gremios: /zgremio global Mensaje
Atajos: /g Mensaje y /gg Mensaje, si esos nombres no pertenecen a otro mod.
Los comandos con /zgremio siempre son los nombres propios de este sistema.

Ejemplo del canal de gremios:
  [GREMIOS] [Vigías del Alba] Godie: Preparamos la expedición.

El privado llega solo al propio gremio. El global de gremios llega a jugadores
que pertenecen a algún gremio. El chat normal de Minecraft conserva el nombre
del jugador con el prefijo del gremio delante. Se respeta el sistema existente
de mensajes; no se simula una firma de chat del jugador.

En SUPREMIUM, HERÁLDICA permite elegir entre 16 colores para tus mensajes.
El color de la bandera es del gremio; el color del texto es personal.
El cliente conserva las últimas 60 líneas de cada canal durante la conexión.
No existe un historial privado descargable de otros gremios.
Hay un intervalo mínimo de un segundo entre mensajes de estos canales.

9. TOML Y EJEMPLOS

Carpeta del servidor: config/ZONEMODS/zonelevelup/
Archivos nuevos:
  gremios.toml          Reglas generales y beneficios de cada rango.
  gremios-misiones.toml Las 70 diarias iniciales.
  gremios-pruebas.toml  Las 42 pruebas de ascenso iniciales.

Se generan solo si no existen. Una actualización no reemplaza tus cambios.
La carpeta CONFIG-EJEMPLO de esta entrega contiene copias de los valores
iniciales para consultarlos; no es necesario reemplazar todo tu config.

Ejemplo de gremios.toml:
  habilitado = true
  max_miembros = 5
  invitacion_segundos = 60
  zona_horaria = "America/New_York"
  distancia_godie = 8

  [rangos.supremium]
  xp_mobs_porcentaje = 13
  monedas_tiempo = 10
  atributos_unicos = 3

Límites validados:
max_miembros: 2..5; invitacion_segundos: 15..300; distancia_godie: 3..16.
xp_mobs_porcentaje: 0..100; monedas_tiempo: 0..1000; atributos_unicos: 0..100.
0 en monedas_tiempo mantiene el pago base de viaje.toml.
El regalo de atributos registra el total ya concedido y solo añade una
diferencia positiva si el administrador aumenta ese regalo posteriormente.

Ejemplo de misión diaria de entrega:
  [[misiones]]
  id = "flores_del_consejo"
  nombre = "Flores para el consejo"
  tipo = "deliver"
  objetivo = "botania:white_mystical_flower"
  cantidad = 12
  rango = 0
  godiecoins = 25
  xp = 150

Ejemplo de prueba de ascenso:
  [[misiones]]
  id = "plata_expediciones"
  nombre = "Juramento de expedición"
  tipo = "expedition"
  objetivo = "*"
  cantidad = 1
  rango = 1
  godiecoins = 0
  xp = 0

Índices: 0 HIERRO, 1 PLATA, 2 ORO, 3 DIAMANTE, 4 PLATINO,
5 NETHERITA, 6 SUPREMIUM. En pruebas, rango indica el DESTINO del ascenso.
Las pruebas de ascenso empiezan en 1, porque HIERRO es el rango inicial.

Tipos: kill, deliver, boss, expedition, discover, structure, trade,
party_seconds. En party_seconds, cantidad está expresada en segundos.
En kill/deliver/discover el objetivo es una ID de registro real.
En structure puede ser una ID de estructura o "*". Los otros tipos admiten "*".
Las diarias de kill/deliver/discover no admiten objetivos minecraft:vanilla.

Cada archivo admite hasta 140 misiones. Las IDs deben ser únicas por archivo,
de hasta 40 caracteres en minúsculas, números y guion bajo. No empieces IDs
por claimed_ o seen_, que son prefijos reservados del historial.
Cantidad: 1..1.000.000; en discover/structure/trade, máximo 256 objetivos
distintos por prueba. Recompensas: 0..10.000 GC y 0..100.000 XP por misión.
Los campos godiecoins/xp de pruebas se reservan para el catálogo; el ascenso
entrega los beneficios del rango y no paga esas cantidades por cada prueba.

Recarga administrativa:
  /zgremio reload
También participa en /zonelevelup reload. Si la validación de gremios falla,
se conserva el último catálogo aceptado y se muestra el error.

Cambiar cantidades no borra el progreso histórico. Cambiar una ID de misión
crea otra identidad de misión: conserva IDs si solo quieres reajustar el balance.
No edites archivos mientras otro administrador esté realizando una recarga.

10. PERMISOS

Jugadores: zonelevelup.use y zonelevelup.guild.use.
El permiso de gremio se permite por defecto y puede restringirse con el
sistema de permisos de ZoneCore que usa el servidor.
La membresía y los cargos se comprueban además de esos permisos.

Administración: zonelevelup.admin u operador según PermissionBridge.
Autoriza /zgremio npc crear|mover|quitar y /zgremio reload.
Ser líder no concede comandos administrativos ni permiso para invocar NPC.

Ayuda: /zgremio ayuda
No necesitas estar en ZParty para crear un gremio, ver diarias o usar sus chats.
ZParty solo es necesaria para la prueba de compañerismo correspondiente.

11. DATOS, RENDIMIENTO Y PRUEBAS

Membresía, nombres, colores y cargos: mundo/data/zonelevelup_guilds.dat.
Rangos, diarias y ascensos: ZoneLevelUp.GuildProgress del personaje, incluidos
sus datos guardados/exportados por PERSONAJES CREADOS. El inventario sigue
siendo el mismo al cambiar de personaje, como en las versiones anteriores.
El NPC se guarda como entidad del chunk donde se coloque.

El servidor valida las acciones, consume objetos y concede beneficios.
El cliente dibuja el folio, desplazamiento, mensajes y efectos de interfaz.
Solo consulta el folio abierto cada cinco segundos; no se emite el catálogo
completo a todos los jugadores en cada tick ni se fuerza carga de chunks.
Los registros de criaturas/estructuras/tratos distintos están acotados.

Resultados exactos y límites de validación: auditoria/PRUEBAS.txt.
Las capturas del folio utilizan datos ficticios sobre una copia de un mundo
aislado. GODIE se renderizó con la skin proporcionada. Las pruebas Forge
usan jugadores simulados; no equivalen a cinco personas en el modpack completo
ni a una prueba de carga sostenida/TPS o caída eléctrica entre archivos.
La transacción real de dos clientes con ZoneEconomy y el modpack completo
queda como comprobación de instalación antes de pasar a producción.
