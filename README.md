<img src="Brio.ico" width="96" alt="Brío icon">

# Brío

> Formerly **xuca-optimizer (Xuca Optimizer)**: if you were searching for that name, this is the app.

Free optimizer for **Windows 10 and 11**. It's a checkbox app: tick what you want and click **Apply**. Before touching anything it reads your PC: it shows what you already have applied and greys out whatever isn't compatible. Every option explains what it does, what you gain and what you lose.

<!-- DEMO GIF: record it, save it as docs/demo.gif and delete the two comment markers on the next line -->
<!-- ![Demo](docs/demo.gif) -->

🇪🇸 [Versión en español más abajo](#-español) · Changelog: [English](lang/en-en/CHANGELOG.md) · [Español](CHANGELOG.md)

## Install

Open **PowerShell** and paste this:

```powershell
irm https://raw.githubusercontent.com/011Xuca/brio/main/install.ps1 | iex
```

It installs to `%LOCALAPPDATA%\Brio` and puts a **Brío** shortcut on your desktop. The app asks for administrator rights when it opens.

You can also download the repo as a ZIP and open `Brio.bat`.

**Windows 7 SP1 and 8.1:** first install [WMF 5.1](https://aka.ms/wmf51download) (it brings PowerShell 5.1) and use this command, which enables TLS 1.2 so it can download from GitHub:

```powershell
[Net.ServicePointManager]::SecurityProtocol = 3072; irm https://raw.githubusercontent.com/011Xuca/brio/main/install.ps1 | iex
```

There, options that need Windows 10 or 11 show up greyed out and aren't applied.

## How to use it

1. When you open the app you see the **welcome** screen with a summary of everything. Pick a section in the left bar (if you don't know where to start, go to **Profiles**).
2. Tick what you want: click anywhere on an option to tick it. Whatever you tick in Debloat and in Gaming is applied together.
3. Click **Apply**. First it offers to create a **restore point** (only once, and you can ask it not to ask again).

## What's inside

| Section | What it's for |
|---|---|
| **Profiles** | Ready-made combos (Safe, Competitive, Fully Optimized...) applied with one click. Competitive is aimed at Valorant, CS2, Fortnite, Warzone, Marvel Rivals, LoL and Deadlock, without touching security. |
| **Debloat and privacy** | Removes ads, telemetry, Windows AI, junk apps and startup apps you don't need. |
| **Gaming zone** | Mouse without acceleration, priority and affinity for your games, power plan, network, DNS and more. |
| **Clean cache** | Deletes temp files, Windows Update cache, shaders and other things that take up space. |
| **Tools** | Recommended drivers, BIOS tweaks, upgrade to Windows 11 26H2 (no black windows: it checks and fixes what blocks the update), scan and repair Windows (DISM + SFC), local account without Microsoft, sign in without a password and more. |
| **Recommended apps** | Free programs to check, look after and clean your PC (CrystalDiskInfo, HWiNFO, DDU, WizTree and more). Each one is downloaded from its official page. |
| **Recommended configs** | Game and app configs I upload to GitHub. They download to your desktop with instructions. The blue dot shows how many there are. |

- In Debloat and Gaming, options are grouped into categories sorted by impact: the biggest performance gains on top, comfort and privacy at the bottom. Each category **collapses** with a click (or the keyboard), shows how many options it has and how many you ticked, and the app remembers what you left collapsed. Searching expands the categories with results.
- Options that used to bundle different things are split up (for example, location and activity history are separate checkboxes), so you choose exactly what to touch.
- The green **Tick only safe ones** button ticks only the options without ⚠.
- Each option says whether it's already applied on your PC.
- Anything not compatible with your Windows is greyed out.

## Drivers

- Options with a **purple** border need a driver. If it's missing, the app won't let you tick it: it tells you which one is missing and takes you to **Tools > Find drivers**. A profile that needs drivers you don't have won't apply until you install them.
- **Find drivers** scans your PC and shows what's worth downloading (graphics card, chipset, whatever your motherboard is missing, your mouse, keyboard or headset software, and whether the BIOS is old). **It installs nothing**: it only opens the official page for whatever is missing.

## Before you use it

- **Options with ⚠ (yellow border) can cause problems on some PCs.** Hover over one and it tells you why.
- **Xbox, Game Pass and Minecraft:** anything that touches Xbox or the Game Bar is flagged on its card, "Tick only safe ones" doesn't tick it, and the app asks before applying it (with **No Xbox** everything else is applied without it). Gaming Services is only removed by **Remove Xbox completely**, which isn't in any profile. The Safe, Optimized and RAM profiles don't touch Xbox; the Competitive ones only remove the Game Bar (asking first).
- Almost everything can be undone: tick it and click **Reset selected**. If an option can't be undone, it tells you.
- The **Fully Optimized** profiles turn off the antivirus: the app warns you before applying them.

## More

- **Updates:** when it opens, the app checks GitHub for a new version and shows a blue banner.
- **Language:** Spanish or English, with the button at the bottom left.
- **Logs:** "Open logs folder" shows everything that was changed.
- **Zoom:** Ctrl + mouse wheel (or Ctrl + / Ctrl -) makes the app bigger or smaller. Ctrl + 0 resets it.
- Gaming optimization (`scripts/Gaming.ps1`), debloat (`scripts/Debloat.ps1`) and cleanup (`scripts/Limpieza.ps1`) run inside the app, without opening console windows. Only deleting an account and signing in without a password open a PowerShell window to ask you for data.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Issues and pull requests are welcome, in English or Spanish. [MIT license](LICENSE).

## Credits

Made by **011Xuca**. Links: https://011xuca.github.io/links/
If it helped you, you can support me on Ko-fi: https://ko-fi.com/011xuca

---

## 🇪🇸 Español

> Antes se llamaba **xuca-optimizer (Xuca Optimizer)**: si lo buscabas con ese nombre, es esta app.

Optimizador gratis para **Windows 10 y 11**. Es una app con casillas: marcás lo que querés y tocás **Aplicar**. Antes de tocar nada lee tu PC: te muestra lo que ya tenés aplicado y deja en gris lo que no es compatible. Cada opción te explica qué hace, qué ganás y qué perdés.

### Instalar

Abrí **PowerShell** y pegá esto:

```powershell
irm https://raw.githubusercontent.com/011Xuca/brio/main/install.ps1 | iex
```

Se instala en `%LOCALAPPDATA%\Brio` y te deja el acceso directo **Brío** en el escritorio. La app pide permisos de administrador al abrirse.

También podés bajar el repo como ZIP y abrir `Brio.bat`.

**Windows 7 SP1 y 8.1:** primero instalá [WMF 5.1](https://aka.ms/wmf51download) (trae PowerShell 5.1) y usá este comando, que activa TLS 1.2 para poder bajar de GitHub:

```powershell
[Net.ServicePointManager]::SecurityProtocol = 3072; irm https://raw.githubusercontent.com/011Xuca/brio/main/install.ps1 | iex
```

Ahí las opciones que necesitan Windows 10 u 11 aparecen en gris y no se aplican.

### Cómo se usa

1. Al abrir la app ves la **bienvenida**, con un resumen de todo. Elegí una sección en la barra de la izquierda (si no sabés por dónde empezar, andá a **Perfiles**).
2. Marcá lo que quieras: tocá cualquier parte de una opción para marcarla. Lo que marques en Debloat y en Gaming se aplica junto.
3. Tocá **Aplicar**. Antes te ofrece crear un **punto de restauración** (una sola vez, y podés pedirle que no vuelva a preguntar).

### Qué trae

| Sección | Para qué sirve |
|---|---|
| **Perfiles** | Combos listos (Seguro, Competitivo, Full Optimizado...) que se aplican con un toque. Competitivo está pensado para Valorant, CS2, Fortnite, Warzone, Marvel Rivals, LoL y Deadlock, sin tocar la seguridad. |
| **Debloat y privacidad** | Saca publicidad, telemetría, IA de Windows, apps basura y apps de inicio que no hacen falta. |
| **Zona gamer** | Mouse sin aceleración, prioridad y afinidad para tus juegos, plan de energía, red, DNS y más. |
| **Limpiar caché** | Borra temporales, caché de Windows Update, shaders y otras cosas que ocupan espacio. |
| **Herramientas** | Drivers recomendados, ajustes de la BIOS, actualizar a Windows 11 26H2 (sin ventanas negras: revisa y arregla lo que impide actualizar), escanear y reparar Windows (DISM + SFC), cuenta local sin Microsoft, entrar sin contraseña y más. |
| **Apps recomendadas** | Programas gratis para revisar, cuidar y limpiar tu PC (CrystalDiskInfo, HWiNFO, DDU, WizTree y más). Cada uno se baja de su página oficial. |
| **Configs recomendadas** | Configs de juegos y apps que subo a GitHub. Se bajan al escritorio con sus instrucciones. El circulito azul dice cuántas hay. |

- En Debloat y Gaming las opciones van agrupadas en categorías ordenadas por impacto: arriba lo que más rendimiento da, abajo la comodidad y la privacidad. Cada categoría se **pliega** con un toque (o con el teclado), muestra cuántas opciones tiene y cuántas marcaste, y la app se acuerda de lo que dejaste plegado. Buscar despliega las categorías con resultados.
- Las opciones que juntaban cosas distintas están separadas (por ejemplo, la ubicación y el historial de actividad son casillas aparte), así elegís exactamente qué tocar.
- El botón verde **Marcar solo seguras** marca solo las opciones sin ⚠.
- Cada opción dice si ya está aplicada en tu PC.
- Lo que no es compatible con tu Windows aparece en gris.

### Drivers

- Las opciones con borde **violeta** necesitan un driver. Si te falta, la app no te deja marcarla: te avisa cuál falta y te lleva a **Herramientas > Buscar drivers**. Un perfil que necesita drivers que te faltan no se aplica hasta que los instales.
- **Buscar drivers** revisa tu PC y te muestra qué conviene bajar (placa de video, chipset, lo que falta de tu placa madre, el programa de tu mouse, teclado o auriculares y si la BIOS está vieja). **No instala nada**: solo te abre la página oficial de lo que falta.

### Antes de usarlo

- **Las opciones con ⚠ (borde amarillo) pueden dar problemas en algunas PCs.** Si pasás el mouse por encima, te dice por qué.
- **Xbox, Game Pass y Minecraft:** lo que toca Xbox o la Game Bar avisa en su tarjeta, no lo marca "Marcar solo seguras" y, antes de aplicarlo, la app te pregunta (con **Sin Xbox** se aplica todo lo demás sin eso). Gaming Services solo lo borra **Quitar Xbox completo**, que no está en ningún perfil. Los perfiles Seguro, Optimizado y RAM no tocan Xbox; los Competitivo solo borran la Game Bar (preguntando antes).
- Casi todo se puede deshacer: marcalo y tocá **Restablecer seleccionadas**. Si una opción no se puede deshacer, te lo avisa.
- Los perfiles **Full Optimizado** apagan el antivirus: la app te lo avisa antes de aplicarlos.

### Más cosas

- **Actualizaciones:** al abrirse, la app revisa si hay una versión nueva en GitHub y te avisa con un cartel azul.
- **Idioma:** español o inglés, con el botón de abajo a la izquierda.
- **Logs:** con "Abrir carpeta de logs" ves todo lo que se cambió.
- **Zoom:** Ctrl + rueda del mouse (o Ctrl + / Ctrl -) agranda o achica la app. Ctrl + 0 la vuelve al tamaño normal.
- La optimización para gaming (`scripts/Gaming.ps1`), el debloat (`scripts/Debloat.ps1`) y la limpieza (`scripts/Limpieza.ps1`) corren dentro de la app, sin abrir ventanas de consola. Solo borrar una cuenta y entrar sin contraseña abren una ventana de PowerShell para pedirte datos.

### Colaborar

Mirá [CONTRIBUTING.md](CONTRIBUTING.md). Se aceptan issues y pull requests, en español o en inglés. [Licencia MIT](LICENSE).

### Créditos

Hecho por **011Xuca**. Redes: https://011xuca.github.io/links/
Si te sirvió, podés apoyarme en Ko-fi: https://ko-fi.com/011xuca
