<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="../profile/assets/oyzters-dark.png">
    <img src="../profile/assets/oyzters-light.png" alt="Oyzters" width="380">
  </picture>
</p>

Official GitHub presence for **Oyzters**, an independent team of ITSON students building tools for academic life: a social network for the community and layers that make the institutional portals usable — CIA, iVirtual and the curriculum map.

You'll find two kinds of repositories here:

- **Open source tools**, MIT-licensed. They run in your browser, on top of your own session: no server in between and no access to your credentials.
- **The PotroNET platform**: the app, its API and its admin panel.

*Leer en español: [README.md](../README.md)*

---

## Tools

All MIT, all used daily on ITSON's real portals.

| Repository | What it is |
|---|---|
| [**CIA-Wrap**](https://github.com/oyzters/CIA-Wrap) | Extension that gives the **CIA / PeopleSoft** portal a modern interface: sidebar, cards, light and dark mode, full-width screens and the Student Center as a dashboard. → [cia.potronet.com](https://cia.potronet.com) |
| [**iVirtual-Wrap**](https://github.com/oyzters/iVirtual-Wrap) | A reskin for **iVirtual** (Moodle): redesigned login, top bar, dashboard and courses. As an extension, userscript or bookmarklet. → [ivirtual.potronet.com](https://ivirtual.potronet.com) |
| [**Wayfinder**](https://github.com/oyzters/Wayfinder) | Visual tracker for the **Software Engineering 2023** curriculum map: status per course, progress by credits and by block, and each course's prerequisites. Everything is stored in your browser. → [isw.potronet.com](https://isw.potronet.com) |

Tired of hunting for the portal's long URL? [cia.potronet.com/entrar](https://cia.potronet.com/entrar) and [ivirtual.potronet.com/entrar](https://ivirtual.potronet.com/entrar) take you straight there.

Issues and pull requests are welcome on these three. Read each repository's README first.

## PotroNET

The ITSON community's social network. The three repositories make up a single platform.

| Repository | What it is |
|---|---|
| [**PotroNET**](https://github.com/oyzters/PotroNET) | The app: a social network exclusive to ITSON students — profiles, posts and feed. A PWA, designed for phones first. → [potronet.com](https://potronet.com) |
| [**PotroNET-API**](https://github.com/oyzters/PotroNET-API) | REST API: authentication, profiles, posts and feed. → [api.potronet.com](https://api.potronet.com) |
| [**PotroNET-Admin**](https://github.com/oyzters/PotroNET-Admin) | The platform's admin panel. → [admin.potronet.com](https://admin.potronet.com) |

React 19, TypeScript, Vite, Tailwind and shadcn/ui on the front; Express on Vercel Functions behind it; Supabase (Postgres, Auth and RLS) underneath.

## How we build

The tools live **on the student's side**: they ask nobody for permission, don't go through a server of ours and never handle your password. You install, turn off and remove them like any other extension.

Two rules hold on every project: **the portal is still the portal** — we change how it looks and how you move through it, not the system's logic — and **phone first**: if something can't be read on a 375 px screen, it isn't finished.

## Team

**Manuel Cortez** · **Sebastian Escalante** — ITSON students. Made by students, for students.

## Contact

- Manuel Cortez — [mdjesuscv@gmail.com](mailto:mdjesuscv@gmail.com)
- Sebastian Escalante — [sebastianescram01@gmail.com](mailto:sebastianescram01@gmail.com)

<sub>Oyzters is an independent project with no affiliation with or official endorsement from the Instituto Tecnológico de Sonora (ITSON). "ITSON", "CIA", "iVirtual", PeopleSoft and Moodle belong to their respective owners.</sub>
