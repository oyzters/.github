<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="profile/assets/oyzters-dark.png">
    <img src="profile/assets/oyzters-light.png" alt="Oyzters" width="380">
  </picture>
</p>

Presencia oficial en GitHub de **Oyzters**, un equipo independiente de estudiantes del ITSON que construye herramientas para la vida académica: una red social para la comunidad y capas que vuelven usables los portales institucionales — CIA, iVirtual y el mapa curricular.

Aquí encontrarás dos tipos de repositorios:

- **Herramientas open source**, con licencia MIT. Corren en tu navegador, sobre tu propia sesión: sin servidor intermedio y sin tocar tus credenciales.
- **La plataforma PotroNET**: la app, su API y su panel de administración.

*Read in English: [README.en.md](docs/README.en.md)*

---

## Herramientas

Todas son MIT y se usan a diario en los portales reales del ITSON.

| Repositorio | Qué es |
|---|---|
| [**CIA-Wrap**](https://github.com/oyzters/CIA-Wrap) | Extensión que le pone una interfaz moderna al portal **CIA / PeopleSoft**: sidebar, tarjetas, modo claro y oscuro, pantallas a todo lo ancho y el Centro de Alumnado como dashboard. → [cia.potronet.com](https://cia.potronet.com) |
| [**iVirtual-Wrap**](https://github.com/oyzters/iVirtual-Wrap) | Reskin del **iVirtual** (Moodle): login, barra superior, tablero y cursos rediseñados. Como extensión, userscript o bookmarklet. → [ivirtual.potronet.com](https://ivirtual.potronet.com) |
| [**Wayfinder**](https://github.com/oyzters/Wayfinder) | Seguimiento visual del mapa curricular de **Ingeniero en Software 2023**: estado por materia, progreso por créditos y por bloque, y la seriación de cada materia. Todo se guarda en tu navegador. → [isw.potronet.com](https://isw.potronet.com) |

¿Cansado de buscar el link largo del portal? [cia.potronet.com/entrar](https://cia.potronet.com/entrar) e [ivirtual.potronet.com/entrar](https://ivirtual.potronet.com/entrar) te llevan directo.

Issues y pull requests son bienvenidos en estos tres. Lee primero el README de cada repositorio.

## PotroNET

La red social de la comunidad ITSON. Los tres repositorios forman una sola plataforma.

| Repositorio | Qué es |
|---|---|
| [**PotroNET**](https://github.com/oyzters/PotroNET) | La app: red social exclusiva para estudiantes del ITSON — perfiles, publicaciones y feed. PWA, pensada primero para el celular. → [potronet.com](https://potronet.com) |
| [**PotroNET-API**](https://github.com/oyzters/PotroNET-API) | API REST: autenticación, perfiles, publicaciones y feed. → [api.potronet.com](https://api.potronet.com) |
| [**PotroNET-Admin**](https://github.com/oyzters/PotroNET-Admin) | Panel de administración de la plataforma. → [admin.potronet.com](https://admin.potronet.com) |

React 19, TypeScript, Vite, Tailwind y shadcn/ui en el frente; Express sobre Vercel Functions detrás; Supabase (Postgres, Auth y RLS) como base.

## Cómo construimos

Las herramientas viven **del lado del estudiante**: no piden permisos a nadie, no pasan por un servidor nuestro y nunca manejan tu contraseña. Se instalan, se apagan y se quitan como cualquier extensión.

Dos reglas que se mantienen en cada proyecto: **el portal sigue siendo el portal** — cambiamos cómo se ve y cómo se navega, no la lógica del sistema — y **el celular primero**: si algo no se lee en una pantalla de 375 px, no está terminado.

## Equipo

**Manuel Cortez** · **Sebastian Escalante** — estudiantes del ITSON. Un proyecto hecho por estudiantes, para estudiantes.

## Contacto

- Manuel Cortez — [mdjesuscv@gmail.com](mailto:mdjesuscv@gmail.com)
- Sebastian Escalante — [sebastianescram01@gmail.com](mailto:sebastianescram01@gmail.com)

<sub>Oyzters es un proyecto independiente, sin afiliación ni respaldo oficial del Instituto Tecnológico de Sonora (ITSON). "ITSON", "CIA", "iVirtual", PeopleSoft y Moodle pertenecen a sus respectivos titulares.</sub>

<sub>Este repositorio es la configuración de la organización. Cómo se publica y cómo se regenera el lockup: [docs/MANTENIMIENTO.md](docs/MANTENIMIENTO.md).</sub>
