# Mantenimiento

Este repositorio es la configuración de la organización **oyzters**.

```
README.md                     el perfil — lo que ve quien entra al repo
profile/
  README.md                   el mismo perfil — lo que GitHub renderiza en github.com/oyzters
  assets/
    oyzters-light.png         el lockup en tinta oscura, 1520×420 (@2x), fondo transparente
    oyzters-dark.png          el mismo en blanco, para el tema oscuro de GitHub
    plate.html                su fuente — se rinde a las dos PNG
    iso.png                   el iso, recortado de potronet/oyzters.png
    figtree.woff2             Figtree, la tipografía del lockup
docs/
  README.en.md                el perfil en inglés
  MANTENIMIENTO.md            este archivo
```

**`README.md` y `profile/README.md` son el mismo texto** y se editan juntos. GitHub solo renderiza
`profile/README.md` en la portada de la organización; el de la raíz existe para que el repositorio
no se vea vacío cuando alguien entra directo. Lo único que cambia entre los dos son las rutas: el de
`profile/` usa URLs absolutas (la portada de la organización no resuelve rutas relativas) y el de la
raíz usa relativas, más la nota final que apunta a este archivo.

## Publicar

Para que el perfil aparezca, el repositorio debe llamarse **`.github`**, ser **público** y tener el
archivo en la rama por defecto:

```bash
gh repo create oyzters/.github --public --source . --push
```

## Regenerar el lockup

El iso y el wordmark en Figtree 800 (`-0.028em`), sin recuadro y con fondo transparente. Son dos
PNG porque GitHub cambia de tema: la clara lleva la tinta `#0F1117` y la oscura todo en blanco. El
`<picture>` de los READMEs elige una u otra con `prefers-color-scheme`.

```bash
cd profile/assets
chrome --headless --disable-gpu --allow-file-access-from-files \
       --force-device-scale-factor=2 --default-background-color=00000000 \
       --window-size=760,210 --screenshot=oyzters-light.png "plate.html"
chrome --headless --disable-gpu --allow-file-access-from-files \
       --force-device-scale-factor=2 --default-background-color=00000000 \
       --window-size=760,210 --screenshot=oyzters-dark.png "plate.html?theme=dark"
```

En Windows, `chrome` es `"C:\Program Files\Google\Chrome\Application\chrome.exe"` y la página se
pasa como `file:///C:/ruta/completa/plate.html`.

### Si cambia el logo

`iso.png` no es el logo tal cual: `potronet/oyzters.png` trae un fondo gris con viñeta. El iso se
obtiene quedándose solo con el trazo negro (luminancia ≤ 8, con transición suave hasta 22, que es
donde arranca el gris del fondo), limitado al círculo del logo para dejar fuera las esquinas oscuras
de la viñeta, y pintado en `#0F1117`. La perla blanca queda hueca: toma el color del fondo de la
página en los dos temas. En el tema oscuro, `plate.html` lo lleva a blanco puro con
`brightness(0) invert(1)`.

## Cuando cambien los repos de la org

Las dos tablas del perfil —herramientas y PotroNET— se escriben a mano. Al publicar un repositorio
nuevo, cambiarle el dominio o la licencia, actualiza las tres copias del texto: `README.md`,
`profile/README.md` y `docs/README.en.md`.

Lo que el perfil afirma sale de los propios repos: las descripciones y dominios de GitHub, el
`LICENSE` de cada uno (CIA-Wrap, iVirtual-Wrap y Wayfinder son MIT; los de PotroNET no declaran
licencia, por eso el perfil no les asigna una) y el stack de `potronet/CLAUDE.md`.
