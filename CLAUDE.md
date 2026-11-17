# CLAUDE.md — awesome-castilla-y-leon

## Project Overview

Curated list of awesome resources about Castilla y León, Spain.

- **Repo:** [GeiserX/awesome-castilla-y-leon](https://github.com/GeiserX/awesome-castilla-y-leon)
- **License:** CC0-1.0

## Mínimo para entrar: rechazo directo

La lista recoge software con recorrido. Una PR que propone un repositorio sin estrellas ni historia se cierra sin más revisión. Se rechaza si, el día que se abre la PR, el repositorio cumple **cualquiera** de estas condiciones:

- Tiene **menos de 5 estrellas**.
- Tiene **menos de 3 meses**. Cuenta la fecha del primer commit; si el autor lo movió desde otro repositorio, cuenta la del original.
- Es **un volcado**: uno o dos commits del mismo día, o una copia de los datos de otra web sin el código que los genera.

La única excepción es el software publicado por un organismo oficial (un ministerio, una comunidad autónoma, un ayuntamiento, `ctt-gob-es`): entra aunque sea nuevo.

```bash
gh api repos/<owner>/<repo> --jq '{estrellas: .stargazers_count, creado: .created_at}'
```

Respuesta al cerrar, en pocas líneas y sin pedir estrella:

> Gracias por la propuesta. La cierro porque el repositorio todavía no llega al mínimo de la lista: 5 estrellas y 3 meses de historia. Cuando los tenga, vuelve a mandarlo y lo miro.

## Verificación antes de añadir

Si pasa el mínimo, comprobar:

- **Existe y es público**: el enlace de GitHub funciona y el repo no es privado.
- **No está archivado ni en solo lectura**: si está archivado, va a `DELETED.md` (sección «Archivados»).
- **Funciona hoy**: si **consume un servicio** (una API, una sede electrónica, una web que raspa), sigue haciéndolo. Si **no consume ninguno** (un validador, un formato, un dataset), su lógica o sus datos siguen siendo correctos. Antes de fusionar, se ejecuta o se coteja con la fuente oficial.
- **No es un duplicado**: cruzar con `README.md` y `DELETED.md`. Si ya hay una entrada mantenida que hace lo mismo, la nueva tiene que aportar algo más.
- **Calidad mínima**: tiene documentación (README) y no es un repositorio vacío o de pruebas.
- **La descripción es fiel**: el lenguaje, el alcance y las etiquetas de servicio coinciden con lo que hace el repositorio.

## Permanencia: qué se queda y qué se retira

Se queda lo que funciona y no tiene un sustituto mantenido en la lista. La reputación decide quién tiene que demostrar qué. Nada se retira sin que Sergio lo apruebe.

- **Archivado**: se retira siempre.
- **Roto**: se retira, tenga la edad que tenga. Hay que enseñar el fallo: ejecutar el proyecto, o comprobar que el servicio que consume ya no responde como espera.
- **Sustituido**: si otra entrada mantenida de la lista hace lo mismo, la vieja se retira aunque tenga reputación. Va a `DELETED.md` con el enlace a la que la sustituye.
- **Sirve a un sistema retirado**: se retira aunque sea oficial.
- **Viejo**: más de 3 años sin commits en la rama por defecto (no `pushed_at`, que las ramas de bots rejuvenecen). Si no es ninguno de los casos anteriores:
  - **con reputación**, se queda mientras no se demuestre que está roto;
  - **sin reputación**, se queda solo si se comprueba que funciona hoy, ejecutándolo o cotejándolo con el servicio que consume. Si no se puede comprobar, se retira.

Reputación es una de estas tres cosas:

- lo publica un organismo oficial;
- lo publica una organización conocida (rOpenSpain, Civio, Datadista, BSC/AINA…);
- tiene uso real visible: estrellas, forks, o descargas o dependientes en su registro (PyPI, npm, Packagist, RubyGems, CRAN, NuGet, crates.io). No hay un número fijo: se juzga caso a caso.

La revisión es trimestral. Lista las entradas con más de 3 años sin commits y revisa cada una con estos criterios; la tabla con la propuesta se le enseña a Sergio antes de mover nada a `DELETED.md`.

## Respuesta a quien abre una PR

Quien añade su proyecto a la lista quiere que se vea. Cuantas más estrellas tiene awesome-castilla-y-leon, más arriba sale en GitHub y más gente llega a cada entrada, así que darle una estrella también beneficia a quien contribuye. Toda respuesta a una PR de otra persona lo aprovecha:

- **Antes de responder, comprueba si ya le ha dado una estrella:**
  ```bash
  gh api --paginate repos/GeiserX/awesome-castilla-y-leon/stargazers --jq '.[].login' | grep -qix '<login>' && echo "ya tiene estrella"
  ```
  Si no sale nada (o `gh` falla), usa la frase condicional «si no le has dado ya una estrella».
- **PR fusionada:** da las gracias e invita a dar la estrella explicando qué gana con ello. Si ya la tiene, agradécela en vez de pedirla.
  > ¡Gracias, ya está en la lista! Si no le has dado ya una estrella ⭐ a awesome-castilla-y-leon, te animo a hacerlo: cuantas más estrellas tiene la lista, más arriba sale en GitHub y más gente descubre tu proyecto.
- **PR cerrada por no llegar al mínimo:** usa la respuesta de «Mínimo para entrar». No hace falta revisar el código ni los datos.
- **PR cerrada sin fusionar:** no se pide estrella por defecto, porque es pedir algo a cambio de un no. Solo se pide cuando le beneficia de verdad: la entrada pasa a otra de nuestras listas, o le invitas a volver cuando el proyecto cumpla los criterios.
- Responde en el idioma en que escribió el autor (castellano por defecto), tuteando y en pocas líneas.

---

*Generated by [LynxPrompt](https://lynxprompt.com) CLI*

<!-- BEGIN BEADS INTEGRATION v:1 profile:minimal hash:6cd5cc61 -->
## Beads Issue Tracker

This project uses **bd (beads)** for issue tracking. Run `bd prime` to see full workflow context and commands.

### Quick Reference

```bash
bd ready              # Find available work
bd show <id>          # View issue details
bd update <id> --claim  # Claim work
bd close <id>         # Complete work
```

### Rules

- Use `bd` for ALL task tracking — do NOT use TodoWrite, TaskCreate, or markdown TODO lists
- Run `bd prime` for detailed command reference and session close protocol
- Use `bd remember` for persistent knowledge — do NOT use MEMORY.md files

**Architecture in one line:** issues live in a local Dolt DB; sync uses `refs/dolt/data` on your git remote; `.beads/issues.jsonl` is a passive export. See https://github.com/gastownhall/beads/blob/main/docs/SYNC_CONCEPTS.md for details and anti-patterns.

## Agent Context Profiles

The managed Beads block is task-tracking guidance, not permission to override repository, user, or orchestrator instructions.

- **Conservative (default)**: Use `bd` for task tracking. Do not run git commits, git pushes, or Dolt remote sync unless explicitly asked. At handoff, report changed files, validation, and suggested next commands.
- **Minimal**: Keep tool instruction files as pointers to `bd prime`; use the same conservative git policy unless active instructions say otherwise.
- **Team-maintainer**: Only when the repository explicitly opts in, agents may close beads, run quality gates, commit, and push as part of session close. A current "do not commit" or "do not push" instruction still wins.

## Session Completion

This protocol applies when ending a Beads implementation workflow. It is subordinate to explicit user, repository, and orchestrator instructions.

1. **File issues for remaining work** - Create beads for anything that needs follow-up
2. **Run quality gates** (if code changed) - Tests, linters, builds
3. **Update issue status** - Close finished work, update in-progress items
4. **Handle git/sync by active profile**:
   ```bash
   # Conservative/minimal/default: report status and proposed commands; wait for approval.
   git status

   # Team-maintainer opt-in only, unless current instructions forbid it:
   git pull --rebase
   git push
   git status
   ```
5. **Hand off** - Summarize changes, validation, issue status, and any blocked sync/commit/push step

**Critical rules:**
- Explicit user or orchestrator instructions override this Beads block.
- Do not commit or push without clear authority from the active profile or the current user request.
- If a required sync or push is blocked, stop and report the exact command and error.
<!-- END BEADS INTEGRATION -->

## Where the tracker syncs

This repo is public, so its tracker syncs only to the private remote named by `sync.remote` in `.beads/config.yaml`. The block above says sync uses "your git remote". Here that never means this GitHub repo. Don't add it as a Dolt remote and don't push `refs/dolt/*` to it.
