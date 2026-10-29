# Modpack FPS / Rendimiento — Minecraft 1.21.1 Fabric

Modpack **solo de rendimiento** para Minecraft Java **1.21.1** con **Fabric**. Contiene **132 mods**
descargados desde sus páginas oficiales de Modrinth: motores de renderizado, optimización de RAM,
de red/ping, de bloques (cofres, hornos, tolvas), de entidades, de carga de chunks, de arranque,
mods de tendencia y mods "olvidados" que casi nadie incluye.

> Si buscas solo el resultado: descarga este repositorio, copia la carpeta `mods/` dentro de tu
> instalación de Fabric y listo. El resto del README explica qué hace cada cosa y qué NO debes juntar.

---

## Contenido del repositorio

| Carpeta / archivo | Qué es |
|---|---|
| `Modpack-FPS-1.21.1-Fabric.zip` | **El ZIP listo para descomprimir.** Los 110 `.jar` van en la **raíz** (sin carpeta `mods` dentro): se extrae directamente dentro de tu carpeta `mods`. |
| `opcionales.zip` | ZIP con los 22 mods opcionales, también con los `.jar` en la raíz (no los copies todos, son alternativas). |
| `mods/` | **110 mods** — el modpack principal. Copia TODO el contenido de esta carpeta a tu `mods`. |
| `opcionales/` | **22 mods** que son alternativas entre sí o que dependen de tu hardware/shaders. **No metas toda la carpeta de golpe**, lee el aviso de cada uno. |
| `LISTA-DE-MODS.md` | Tabla completa: mod, versión, archivo, lado (cliente/servidor) y para qué sirve. |
| `Modpack-FPS-1.21.1-Fabric.mrpack` | Archivo importable en **Modrinth App**, Prism Launcher o ATLauncher. |
| `descargar-mods.bat` / `descargar-mods.sh` | Scripts que vuelven a descargar todos los `.jar` desde Modrinth si prefieres no clonar el repo. |

---

## Requisitos

1. **Minecraft Java Edition 1.21.1**
2. **Fabric Loader** (https://fabricmc.net/use/installer/) — cualquier versión reciente sirve.
3. **Java 21** (obligatorio para 1.21.1).
4. **Fabric API**: ya viene incluida en `mods/`, no la descargues aparte.
5. RAM asignada recomendada: **4 GB mínimo, 6–8 GB ideal** (con FerriteCore y Chloride el juego consume mucho menos).

## Instalación (4 formas)

### Opción A — ZIP (la más rápida)
1. Descarga **`Modpack-FPS-1.21.1-Fabric.zip`** (botón *Download* en el repositorio).
2. Abre tu **carpeta `mods`** (inicia el juego una vez con el perfil de Fabric para que se cree):
   - Windows: `%appdata%\.minecraft\mods`
   - Linux: `~/.minecraft/mods`
   - macOS: `~/Library/Application Support/minecraft/mods`
3. Copia el ZIP ahí dentro y usa **"Extraer aquí"**. Los `.jar` quedan sueltos junto a los que ya tengas,
   sin subcarpetas. No borra nada de lo que ya tengas.
4. Abre el perfil de Fabric 1.21.1 con Java 21. Listo.

### Opción B — Manual
1. Instala Fabric 1.21.1 con el instalador oficial.
2. Abre la carpeta de tu perfil: `%appdata%\.minecraft\mods` (Windows) o `~/.minecraft/mods` (Linux/macOS).
3. **Copia todos los archivos `.jar` de la carpeta `mods/` de este repo** ahí dentro.
4. Inicia el perfil de Fabric. Ya está.

### Opción C — Importar el `.mrpack`
1. Abre **Modrinth App** (o Prism Launcher).
2. "Add instance" → "Import from file" → elige `Modpack-FPS-1.21.1-Fabric.mrpack`.
3. La app descargará y colocará todos los mods automáticamente.

### Opción D — Script de descarga
- Windows: doble clic en `descargar-mods.bat`.
- Linux/macOS: `bash descargar-mods.sh`.
Descarga los 110 mods a la carpeta `mods/` desde Modrinth (útil si clonaste solo el texto del repo).

> **¿Prefieres no bajar el repo entero?** En GitHub: botón verde **Code → Download ZIP** descarga todo
> el repositorio en un ZIP (incluye jars, docs y los ZIP de mods).

---

## Qué incluye el modpack (resumen por categorías)

### Núcleo: los motores que realmente suben los FPS
**Sodium** (motor de renderizado), **Lithium** (física, IA, ticks), **FerriteCore** + **Chloride** + **Palladium** (RAM),
**ModernFix**, **ImmediatelyFast**, **EntityCulling**, **More Culling**, **BadOptimizations**, **Ixeris** (input lag),
**Krypton** (red), **C2ME** (chunks multihilo), **ScalableLux** (iluminación), **Noisium** + **Fast Noise** (worldgen),
**ThreadTweak** (hilos de CPU), **Particle Core** + **AsyncParticles**, **Exordium**, **Redirected**, **Faster Random**.

### Bloques concretos (cofres, camas, hornos, tolvas, cuadros, marcos)
**Enhanced Block Entities** (cofres, camas, shulkers, carteles), **Fast Paintings**, **Fast Item Frames**,
**Better Beds**, **Boat Item View**, **FeyTweaks** (carteles con texto), **Gnetum**, **Entity View Distance**.
En `opcionales/` tienes **Better Block Entities**, **FastChest** y **OBE** (alternativas a EBE) y
**Faster Hoppers** / **Fast Furnace** (tolvas y hornos más rápidos, cambian el comportamiento vanilla).

### Objetos y entidades concretas (incluida la ballesta)
**Crossbow Optimizer** (ballestas y flechas), **Xp Bottle Optimizer**, **Consumable Optimizer**,
**Clumps** (orbes de XP), **Get It Together, Drops!** (fusión de ítems en el suelo), **Neruina** (entidades rotas que laguean),
**Achievements Optimizer**, **Advancements Screen Optimizer**, **Not Enough Recipe Book** (quita el libro de recetas).

### RAM y GPU
**FerriteCore**, **Chloride**, **Palladium**, **Put A Plug In it! (PAPI)** (fugas de memoria),
**Shut Up GL Error**, **Async Logger** (logs en otro hilo = menos tirones), **Log Cleaner**.
En `opcionales/`: **GPUBooster** (menos VRAM) y **Super Resolution** (escalado tipo FSR).

### Red, ping y servidores (lo que pediste específicamente)
| Mod | Qué arregla |
|---|---|
| **Fast IP Ping** | El ping lento de la lista de servidores: al añadir una IP se resuelve al instante en vez de quedarse "Pinging...". |
| **Server Pinger Fixer** | Pings incorrectos/atascados y el "Can't connect to server" falso de la lista. |
| **Krypton** | Reescribe la pila de red: menos lag de conexión en multijugador. |
| **Packet Fixer** | Errores de paquetes demasiado grandes (kick por "payload too large"). |
| **Bad Packets** | Ignora paquetes inválidos de servidores en vez de procesarlos. |
| **Very Many Players (VMP)** | Servidores con mucha gente sin caídas de TPS. |
| **ServerCore** | Optimizaciones del lado servidor (también ayuda en LAN). |
| `opcionales/`: **XXL Packets** / **Extra Thicc Packets** | Suben el límite de tamaño de paquetes (usa solo uno). |

### Carga, arranque y menús
**DashLoader**, **Async Pack Scan**, **ResourcePackCached**, **Remove Reloading Screen**, **Language Reload**,
**Lazy Language Loader**, **FastQuit**, **Epic Force Close Loading Screen**, **Cubes Without Borders**,
**Quick Pack**, **Borderless Fullscreen**, **Reese's Sodium Options**.

### FPS extra y utilidades
**Dynamic FPS**, **FPS Reducer**, **Sodium Extra**, **Sodium Options API**, **Mod Menu**, **Debugify**,
**Crash Assistant**, **ToolTipFix**, **Clean F3**, **spark** y **Observable** (profilers: te dicen exactamente
qué mod te baja los FPS), **Chunky** (pre-genera el mundo y elimina tirones), **Kerria** (animación de texturas).

### APIs y librerías
Fabric API, Cloth Config, YetAnotherConfigLib, MidnightLib, Architectury API, Fabric Language Kotlin,
Puzzles Lib, Collective, Forge Config API Port, Fzzy Config, Resourceful Config, ToadLib, WalksyLib,
TxniLib, Almanac, Configurable, JamLib, LibJF, Moonlight Lib, OctoLib, owo-lib, ZConfig,
Chunk Activity Tracker y Text Placeholder API. **No las borres**: sin ellas los mods no cargan.

---

## Mods de tendencia y mods "olvidados" que sí están incluidos

Mods que casi nadie mete en sus packs pero funcionan y se notan:

- **Ixeris** — entrada sin búfer y sondeo de eventos multihilo (menos input lag, tendencia en 2026).
- **Kerria** — acelera la animación de texturas (muy de tendencia y apenas conocido).
- **Chloride** — rendimiento extra sobre Sodium bajando RAM.
- **Palladium** — deduplicación de datos y memoria (optimización profunda, poco conocida).
- **PAPI (Put A Plug In it!)** — arregla fugas de memoria que el juego arrastra desde hace años.
- **Exordium** — bufferiza el HUD e inventarios (sube FPS en menús, muy olvidado).
- **FeyTweaks / Gnetum / Better Biome Reblend** — renderizado de carteles, bloques y biomas.
- **Async Logger** — los logs dejan de bloquear el hilo principal.
- **Structure Layout Optimizer / Fast Noise / Does It Tick? / Despawn Tweaks / MobsBeGone** — lado servidor.
- **Crossbow Optimizer / Xp Bottle Optimizer / Consumable Optimizer / Achievements Optimizer** — objetos concretos.
- **LazyAI / OptimizeMod / Lazy Language Loader / ResourcePackCached** — optimizaciones "de nicho".
- **Fast IP Ping + Server Pinger Fixer** — el arreglo del ping de servidores que pediste.

---

## Avisos importantes (evita crasheos)

1. **EBE, BBE, FastChest y OBE son alternativas entre sí.** En `mods/` ya viene **Enhanced Block Entities**.
   Si prefieres otro, borra EBE y pon **solo uno** de los otros tres.
2. **Culling de hojas:** `mods/` ya trae **More Culling**. En `opcionales/` están *Cull Less Leaves*, *Cull Leaves* y
   *Sodium Leaf Culling*: usa como máximo uno y solo si quieres exprimir más (pueden solaparse con More Culling).
3. **Sodium y VulkanMod son incompatibles.** VulkanMod sustituye a Sodium: si lo usas, borra Sodium, Sodium Extra,
   Reese's Sodium Options, Chloride y Sodium Extras.
5. **Iris (shaders)** está en `opcionales/`. Los shaders bajan FPS: solo instálalos si quieres shaders.
   Si los instalas, añade también **FISM** de `opcionales/` para acelerar las sombras.
6. **GPUBooster** es incompatible con VulkanMod y puede no gustar a todas las GPUs: pruébalo por separado.
7. **FPS Reducer, Dynamic FPS y FPS-Sync** hacen cosas parecidas (limitar FPS). `mods/` ya trae los dos primeros;
   `FPS-Sync` está en opcionales por si prefieres limitar a la tasa del monitor sin V-Sync.
8. **XXL Packets y Extra Thicc Packets** son alternativas: usa solo una y solo si algún mod lo pide.
9. **`opcionales/` no es para copiar entero.** Mete solo los que quieras, respetando los avisos.
10. Si el juego crashea, **Crash Assistant** te dirá qué mod lo causó; **spark** te dirá qué te come los FPS.

## Ajustes recomendados después de instalar

- Asigna **4–8 GB** de RAM en tu launcher (ni más ni menos: demasiada RAM también baja los FPS).
- Argumentos JVM sugeridos (Java 21):
  `-XX:+UseG1GC -XX:+ParallelRefProcEnabled -XX:MaxGCPauseMillis=200 -XX:+UnlockExperimentalVMOptions -XX:+DisableExplicitGC -XX:G1NewSizePercent=30 -XX:G1MaxNewSizePercent=40 -XX:G1HeapRegionSize=8M -XX:G1ReservePercent=20`
- En las opciones de **Sodium**: activa "Entity Culling" y "More Culling" en sus menús (Mod Menu).
- Con **Chunky** pre-genera tu mundo una vez: `/chunky radius 2000` y `/chunky start`. Después, los tirones al explorar desaparecen.
- Usa **spark** (`/spark profiler start` y luego `/spark profiler stop`) para ver qué mod te está bajando los FPS.

## Mods que NO están y por qué

- **Memory Leak Fix**: no tiene versión para 1.21.1 en Modrinth. En su lugar se incluye **Put A Plug In it! (PAPI)**,
  que hace lo mismo (fugas de memoria + optimización de RAM).
- **Connectivity**: ya no está publicado en Modrinth. Su función (timeouts y desconexiones) la cubren
  **Packet Fixer**, **Krypton** y **Bad Packets**.
- **Radium / FoamFix / Phosphor / LazyDFU**: abandonados o sin soporte para 1.21.1; su función ya la hacen
  Lithium, ModernFix, ScalableLux y DashLoader.

---

## Créditos y licencias

Todos los mods son propiedad de sus autores y se descargan desde sus páginas oficiales de **Modrinth**
(los enlaces están en [LISTA-DE-MODS.md](LISTA-DE-MODS.md)). Este repositorio solo los reúne para que no tengas
que buscarlos uno a uno. Respeta la licencia de cada mod si vas a redistribuirlo.

**Versión de la recopilación:** 1.21.1 · Fabric · generada el 2026-10-29.
