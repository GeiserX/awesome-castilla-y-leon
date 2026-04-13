# AGENTS.md — awesome-castilla-y-leon

## Propósito

Selección de software open source que da **soporte específico a Castilla y León** — su gobierno autonómico (JCyL), diputaciones provinciales, ayuntamientos, universidades, empresas, infraestructuras y patrimonio. Todo el contenido en español. El foco es Castilla y León: el software debe dirigirse específicamente a esta comunidad autónoma o a sus provincias y municipios.

## Ámbito

- **9 provincias** de Castilla y León están dentro del ámbito: Ávila, Burgos, León, Palencia, Salamanca, Segovia, Soria, Valladolid, Zamora.
- Principales ciudades: Valladolid (capital), Burgos, Salamanca, León, Segovia, Ávila, Zamora, Palencia, Soria, Ponferrada, Aranda de Duero, Miranda de Ebro, Medina del Campo, Béjar, Ciudad Rodrigo, Astorga.
- **Universidades**: UVa (Universidad de Valladolid), USAL (Universidad de Salamanca), ULE (Universidad de León), UBU (Universidad de Burgos), UEMC (Universidad Europea Miguel de Cervantes), IE University (Segovia), UCAV (Universidad Católica de Ávila), UNED centros asociados.
- **Instituciones**: JCyL (Junta de Castilla y León), AUVASA (Autobuses Urbanos de Valladolid), Diputaciones Provinciales, SACYL (Sanidad de Castilla y León), ITACyL (Instituto Tecnológico Agrario), ADE (Agencia de Innovación y Desarrollo Económico), EREN (Ente Regional de la Energía), Fundación Patrimonio Natural.
- **Datos abiertos**: datosabiertos.jcyl.es (portal oficial de la Junta).

## Criterios de inclusión

### Incluir

- Software que interactúa con la **JCyL** o sus organismos (Sede Electrónica, Portal de Transparencia, datos abiertos).
- Herramientas para **ayuntamientos o diputaciones** de Castilla y León.
- Software de **universidades castellanoleonesas** (UVa, USAL, ULE, UBU) cuando sea específico de la región o la universidad.
- Herramientas de **datos abiertos** de Castilla y León (datosabiertos.jcyl.es).
- Software de **transporte** de Castilla y León (AUVASA, autobuses urbanos, RENFE cercanías CyL).
- Herramientas de **agricultura e ITACyL** (Instituto Tecnológico Agrario de Castilla y León).
- Software relacionado con el **Camino de Santiago** (tramos por Castilla y León: Burgos, León, Palencia).
- Herramientas de **cartografía y SIG** específicas de Castilla y León (IDECyL).
- Software sobre **patrimonio y cultura** de la región (Catedrales, Camino de la Lengua, Las Médulas, Atapuerca).
- Herramientas de **turismo** regional.
- Software de **energía y agua** regional (EREN, Confederación Hidrográfica del Duero).
- Proyectos de **smart cities** para ciudades de Castilla y León.
- Software sobre **deportes** de Castilla y León (Real Valladolid, CB Valladolid, Burgos CF).
- Proyectos del **sistema sanitario** (SACYL).
- Software **educativo** específico de la región (Educacyl).
- Herramientas de **meteorología** regional.
- Proyectos de **industria y empresa** (ADE, FEDER CyL).
- Software sobre **medio ambiente** (Fundación Patrimonio Natural, Red Natura 2000 en CyL).
- Herramientas del **Boletín Oficial** (BOCyL, BOPs provinciales).

### No incluir

- Software **genérico** que funciona en toda España sin funcionalidad específica de Castilla y León — eso pertenece a awesome-spain.
- Software de **ámbito europeo** — eso pertenece a awesome-europe.
- Software de **otras comunidades autónomas** españolas.
- Software creado por castellanoleoneses que **no tiene funcionalidad específica** de la región.
- Repositorios **archivados o de solo lectura** — van a `DELETED.md`.
- Repos donde el autor indica que el proyecto está **roto, sin mantenimiento o deprecado**.
- Repos **sin README significativo** o que son claramente repos de test/experimento.
- Ejercicios de clase o trabajos académicos sin utilidad real.

### Zona gris — usar criterio

- Proyectos de universidades castellanoleonesas que podrían ser genéricos — incluir si tienen datos o configuración específica de Castilla y León.
- Software que cubre Castilla y León junto con otras regiones — incluir si Castilla y León es un foco principal.

## Estándares de calidad

**Mismo listón que [awesome-spain](https://github.com/GeiserX/awesome-spain):**

- **No repos archivados**: si se descubre archivado tras la inclusión, mover a `DELETED.md` inmediatamente.
- **No repos extremadamente sin mantenimiento**: al menos un commit en los últimos 3 años, salvo que sea un proyecto claramente estable/completo.
- **No repos rotos**: si el README dice «deprecated», «no longer maintained», «use X instead» o similar — no incluir. Mover a `DELETED.md` si ya está listado.
- **Estrellas mínimas**: preferir repos con al menos unas pocas estrellas, pero herramientas nicho excepcionales con 0-1 estrellas pueden incluirse si cubren un hueco importante.
- **Verificar cada repo** antes de añadir: comprobar `archived`, `pushed_at`, `stargazers_count` vía `gh api repos/owner/name`.

## Formato de entrada

```markdown
- [Nombre](https://github.com/owner/repo) [![Stars](...)](stargazers) [![Last Commit](...)](commits) [![Language](...)](repo) [![License](...)](LICENSE) [![Tag](...)](url) - Descripción que empieza en mayúscula y termina con punto.
```

Las insignias se generan automáticamente con `scripts/transform-readme.py`. Para contribuir, basta con añadir la entrada en formato simple:

```markdown
- [Nombre](https://github.com/owner/repo) - Descripción que empieza en mayúscula y termina con punto.
```

- La descripción **no debe empezar con el nombre** del proyecto.
- Máximo una línea por entrada.
- Validar con awesome-lint-extra: `python3 lint.py` o mediante el workflow de CI.
- Entradas en **orden alfabético** dentro de cada categoría.
- Categorías en **orden alfabético** en el índice y en el cuerpo del documento.
- Entradas en `DELETED.md` también en **orden alfabético** dentro de cada sección.

## Verificación antes de añadir

Antes de incluir un repositorio, comprobar:

- **Existe y es público**: el enlace de GitHub funciona y el repo no es privado.
- **No está archivado o de solo lectura**: si archivado, va a `DELETED.md` (sección «Archivados»).
- **No está deprecado**: comprobar si el README dice «deprecated», «unmaintained», «broken», «use X instead».
- **Actividad razonable**: al menos un commit en los últimos 3 años, salvo que sea un proyecto estable/completo.
- **No es un duplicado**: cruzar con `README.md` y `DELETED.md`.
- **Calidad mínima**: tiene documentación (README) y no es un repositorio vacío o de test.

## Pull requests y contribuciones

- Las PRs deben usar la plantilla en `.github/PULL_REQUEST_TEMPLATE.md`.
- **Obligatorio**: incluir en la PR la **URL del servicio, API o institución de Castilla y León** a la que el software da soporte.
- Plantillas de issues disponibles para sugerir proyectos (`anadir-proyecto.md`) y solicitar retirada (`retirar-proyecto.md`).

## Estructura

- Secciones con `##`, subsecciones con `###`.
- Índice de contenido al principio entre comentarios `<!--lint disable/enable awesome-list-item-->`.
- Al final: sección Contribuir, Nota y Descargo de responsabilidad (como párrafos en negrita, no encabezados ##).

## Temas prohibidos

No se aceptan proyectos relacionados con: pornografía, contenido NSFW, loterías o apuestas, religión, política partidista.

## Difusión

- Notificar a los propietarios de repos abriendo un issue titulado «Listado en awesome-castilla-y-leon» con un breve mensaje en español (tuteo) ofreciendo retirar si lo prefieren. Solo 1 issue por organización/usuario — no spamear repos del mismo propietario.
- Publicar en comunidades de Castilla y León (Reddit, foros universitarios, Telegram de devs) tras alcanzar masa crítica.
- Enviar PR a [sindresorhus/awesome](https://github.com/sindresorhus/awesome) tras 30 días desde la creación del repo.

## Aprendizajes

- Las búsquedas en GitHub con `"castilla y leon"` dan resultados limitados. Es más efectivo buscar por instituciones concretas (JCyL, UVa, USAL, ULE, UBU, AUVASA) y por ciudades principales (Valladolid, Burgos, Salamanca, León, Segovia).
- Muchos repos de universidades son ejercicios de clase sin utilidad real — filtrar con criterio.
- VallaBus es la organización más activa con repos específicos de Valladolid (vallabus, api-auvasa).
- La JCyL no tiene organización GitHub oficial conocida. Los datos abiertos están en datosabiertos.jcyl.es.
- AUVASA no tiene presencia oficial en GitHub. Los repos son de la comunidad (VallaBus, antares500).
- La USAL no tiene organización GitHub oficial significativa. Los repos son de estudiantes/profesores individuales.
- La UVa tiene presencia mínima: `uva-trasgo` (grupo de investigación en computación paralela) es el más relevante.
- El topic `castilla-y-leon` en GitHub tiene muy pocos repos.
- **León**: cuidado con búsquedas — la mayoría de resultados son de León (México/Nuevo León). Filtrar siempre por España.
- **Burgos**: la UBU no tiene presencia significativa en GitHub.
- **Rate limits**: el API de búsqueda de GitHub (30 req/min) se agota rápidamente. Estrategia efectiva: usar `gh api repos/...` (core API, 5000/h) para verificar repos conocidos.
- Los BOP (Boletines Oficiales Provinciales) de Valladolid tienen proyectos de scraping activos (AxierSangroniz).
- El portal de datos abiertos de la JCyL (datosabiertos.jcyl.es) tiene un bot de Telegram comunitario (ComputingVictor).

*Generated by [LynxPrompt](https://lynxprompt.com) CLI*
