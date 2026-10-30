# Historial de versiones

[English](CHANGELOG.md) · [简体中文](CHANGELOG.zh-CN.md) · [繁體中文](CHANGELOG.zh-TW.md) · [日本語](CHANGELOG.ja.md) · [한국어](CHANGELOG.ko.md) · **Español** · [Français](CHANGELOG.fr.md)

## Linux 0.1.0 — 2026-10-30

Broomy llega a Linux, como un solo comando para la terminal.
- **Encuentra**: cachés de gestores de paquetes (pip, uv, npm, pnpm, Yarn, Bun, Composer, Go y Cargo), cachés de Gradle y VS Code, carpetas de compilación de proyectos antiguos, miniaturas, cachés de apps, instaladores en Descargas y en el Escritorio, paquetes de apt descargados, versiones antiguas de snap, el diario del sistema y paquetes que nada necesita. La papelera y Docker solo se miden, no se tocan.
- **Muestra antes de limpiar**: `broomy show` lista cada archivo con su ruta; `broomy clean --dry-run` dice qué pasaría.
- **Limpia con cuidado**: tus archivos van a la papelera (el gestor de archivos puede recuperarlos); los elementos del sistema usan apt, snap y journalctl directamente y te piden la contraseña mediante sudo. Las cachés de programas en ejecución, los enlaces, otros discos y todo lo que git rastrea se dejan en paz.
- Un solo archivo para x86_64 y ARM, sin instalar nada más. Siete idiomas. Nada de código de red.

## 1.2 — 2026-10-29

- **Mover**, una página nueva: las apps que casi no usas y los archivos grandes que no abres desde hace un mes pasan a una carpeta «Moved by Broomy» de un disco externo, solo después de que los marques y confirmes. Cada uno se copia y se comprueba con el original antes de que el original vaya a la papelera; una app deja un enlace en su sitio. Si algún paso falla, no se mueve nada. **Devolver** los trae de vuelta del mismo modo.
- Las apps solo van a discos de estado sólido, y cuando un disco no indica si es de estado sólido o un disco duro, eliges tú. Las apps de la App Store o de un instalador, y las que se ejecutan en segundo plano, se quedan donde están, con el motivo a la vista.
- Una app movida a un disco que no está conectado sigue contando como instalada, así que sus datos nunca se ofrecen como restos de una app eliminada.
- **Desinstalar** ordena según los días que has usado cada app en los últimos 90.
- **Anotar qué días abres cada app** (Ajustes, desactivado por defecto): se guarda en este Mac durante un año y puedes borrarlo.

## 1.1 — 2026-10-27

- **Más cosas que limpiar**: previsualizaciones de Xcode; las cachés que las apps hechas con tecnología web (como VS Code, Slack y Discord) guardan en sus propias carpetas, que se omiten mientras la app está abierta; instantáneas del emulador de Android; cachés de herramientas de línea de comandos; carpetas de datos de apps que ya no están instaladas; imágenes de disco (.iso, .img) junto a los instaladores. Las cuatro últimas empiezan sin marcar.
- **Vaciar la papelera** desde Limpieza, el Resumen o la barra de menús. La vacía el Finder, y solo cuando haces clic y confirmas; nada más en Broomy elimina nada para siempre.
- **Páginas más tranquilas**: los botones secundarios son iconos (su nombre aparece al apuntarlos) y la descripción de cada categoría está tras una ⓘ.
- **Desinstalar** puede ordenar las apps según lo poco que las abres.
- **Sincronización de fotos…** en el Resumen explica cómo pausar Fotos en iCloud o desactivarla en este Mac. Broomy solo abre Fotos; nunca cambia el ajuste por sí mismo.
- El botón de encendido del panel de la barra de menús cierra las ventanas de Broomy y lo deja en la barra de menús; para salir, haz clic derecho en su icono.
- El correo escrito desde Acerca de Broomy empieza su asunto con [Broomy].

## 1.0 — 2026-10-21

Primera versión.
- **Una página por función, una al lado de otra**: Resumen, Limpieza, Desinstalar, Sistema, Salud del disco y Dispositivos. Desliza dos dedos, haz clic en la barra de arriba o pulsa ⌘1…⌘6.
- **Limpieza**: restos de herramientas de desarrollo (Xcode, simuladores, Gradle, Homebrew, cachés de pip, npm, pnpm, Yarn, Bun, CocoaPods, Swift Package Manager, Go y Cargo, y carpetas de compilación de proyectos antiguos), cachés y registros de apps, instaladores en Descargas y en el Escritorio, y lo que dejaron apps eliminadas. Todo va a la papelera.
- **Desinstalar** una app junto con su contenedor, cachés, ajustes, estado de ventanas, datos web e ítems de inicio.
- **Sistema y salud del disco**: CPU, memoria, temperaturas y ventiladores; cuánto ha escrito el SSD interno y cuánto se ha desgastado.
- **Dispositivos**: brillo y volumen de tus pantallas, con el motivo y qué probar cuando una no se puede ajustar; salida de sonido, una rueda del ratón más cómoda, discos externos, USB y Thunderbolt.
- En la barra de menús si quieres. Nueve idiomas. Nada de código de red.
