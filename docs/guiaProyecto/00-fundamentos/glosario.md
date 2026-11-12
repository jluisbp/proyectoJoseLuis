# Glosario común del alumnado

## Cómo usar este glosario

- Busca el término en el índice; cada entrada tiene un enlace fijo que puedes usar desde tus propios documentos.
- Cada entrada dice qué es, a veces un ejemplo inventado y **dónde lo verás** en el curso.
- Si falta un término o algo no se entiende, anótalo como bloqueo en tu `docs/registro-tutoria.md`.

## Índice

**Git y GitHub:** [Clonar](#clonar) · [Commit](#commit) · [Conflicto](#conflicto) · [Conventional Commits y «ámbito»](#conventional-commits-y-ámbito) · [Correo `noreply`](#correo-noreply) · [Fast-forward](#fast-forward) · [`force push`](#force-push) · [Fork](#fork) · [`.gitignore`](#gitignore) · [Hash de commit](#hash-de-commit) · [Issue](#issue) · [Kebab-case](#kebab-case) · [`main`](#main) · [Merge commit («Create a merge commit»)](#merge-commit-create-a-merge-commit) · [Pull](#pull) · [Pull Request (PR)](#pull-request-pr) · [Push](#push) · [Rama](#rama) · [Rebase](#rebase) · [Repositorio (repo)](#repositorio-repo) · [Squash («Squash and merge»)](#squash-squash-and-merge) · [Tag (de Git) frente a label (de GitHub)](#tag-de-git-frente-a-label-de-github) · [Upstream](#upstream)

**Curso:** [Briefing](#briefing) · [Declaración de uso de IA](#declaración-de-uso-de-ia) · [Defensa oral](#defensa-oral) · [Definición de hecho](#definición-de-hecho) · [Fase](#fase) · [Historia de usuario](#historia-de-usuario) · [Hito (H1, H2, H3)](#hito-h1-h2-h3) · [Plantilla del proyecto](#plantilla-del-proyecto) · [RA, CE y cómo leer «RA1 / 1f»](#ra-ce-y-cómo-leer-ra1--1f) · [Registro de tutoría](#registro-de-tutoría) · [Repo de práctica frente a repo del proyecto](#repo-de-práctica-frente-a-repo-del-proyecto) · [Tablero Kanban](#tablero-kanban) · [Tutor](#tutor) · [Vía A y vía B](#vía-a-y-vía-b)

**Documentar y requisitos:** [Dado / Cuando / Entonces](#dado--cuando--entonces) · [Fuente primaria / secundaria / oficial](#fuente-primaria--secundaria--oficial) · [Markdown](#markdown) · [Mermaid](#mermaid) · [README](#readme) · [RF / RNF / REST](#rf--rnf--rest) · [Ruta relativa](#ruta-relativa) · [SOTA](#sota) · [Trazabilidad](#trazabilidad) · [`verificado` / `declarado` / `no leído`](#verificado--declarado--no-leído)

**Datos y seguridad:** [AEPD](#aepd) · [API](#api) · [Biblioteca y framework](#biblioteca-y-framework) · [Dato personal](#dato-personal) · [`.env`](#env) · [`.env.example`](#envexample) · [Hash y «sal»](#hash-y-sal) · [LOPDGDD](#lopdgdd) · [OWASP](#owasp) · [RGPD](#rgpd) · [Secret scanning](#secret-scanning) · [Token de acceso / clave de API](#token-de-acceso--clave-de-api)

**IA:** [Agente](#agente) · [Alucinación](#alucinación) · [IA, machine learning y LLM](#ia-machine-learning-y-llm) · [OpenCode (V1 frente a V2)](#opencode-v1-frente-a-v2) · [Parámetros (de un modelo)](#parámetros-de-un-modelo) · [Permiso (`allow` / `ask` / `deny`)](#permiso-allow--ask--deny) · [Plan B sin IA](#plan-b-sin-ia) · [Prompt](#prompt) · [Skill](#skill) · [Token (de un modelo de IA)](#token-de-un-modelo-de-ia) · [Ventana de contexto](#ventana-de-contexto)

**Otros:** [C4](#c4) · [Lighthouse](#lighthouse) · [Terminal (según el sistema operativo)](#terminal-según-el-sistema-operativo)

## Git y GitHub

**Git** es el programa que guarda la historia de tu trabajo. **GitHub** es la web donde la publicas y la revisas.

### Clonar

Copiar un repositorio de GitHub a tu ordenador, con toda su historia.

*Ejemplo:* `git clone https://github.com/ana-ejemplo/proyecto-demo.git`

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

### Commit

Una «foto» de tus cambios guardada en la historia, con un mensaje que explica qué cambiaste.

*Ejemplo:* `docs: añade descripción al README`

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

### Conflicto

Dos cambios tocan la misma línea y Git no sabe cuál conservar. Lo decides tú, abriendo el fichero y borrando las marcas `<<<<<<<`, `=======` y `>>>>>>>`.

**Dónde lo verás:** [cap. 01](01-git-y-github.md) (errores frecuentes).

### Conventional Commits y «ámbito»

Formato de mensaje de commit: `tipo(ámbito opcional): descripción`. El tipo dice qué haces (`feat`, `fix`, `docs`, `chore`, `test`, `refactor`). El **ámbito** es una palabra entre paréntesis que indica la parte afectada. En el curso, las correcciones que pide el tutor llevan el ámbito `tutor`.

*Ejemplo:* `fix(tutor): valida el formulario vacío`

**Dónde lo verás:** [cap. 01](01-git-y-github.md); [metodologia.md](../../metodologia.md) §4.

### Correo `noreply`

Dirección que GitHub te da para firmar commits sin enseñar tu correo personal. Formato: `ID+USUARIO@users.noreply.github.com`.

*Ejemplo:* `123456+ana-ejemplo@users.noreply.github.com`

**Dónde lo verás:** [cap. 01](01-git-y-github.md) (paso 0b) y [cap. 04](04-claves-y-datos-personales.md).

### Fast-forward

Merge sin commit extra: Git solo adelanta el puntero de tu rama porque no hay nada que unir. Si cada lado tiene commits propios, Git rechaza el `push` con el mensaje `non-fast-forward`.

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

### `force push`

Subir tus commits imponiéndolos y pisando la historia que hay en GitHub (`git push --force`). **Está prohibido en el proyecto**: el seguimiento semanal se hace sobre tu historial y tiene que contar cómo has avanzado. Si Git rechaza un `push`, no lo fuerces: haz `pull`, resuelve y vuelve a subir, o pregunta.

**Dónde lo verás:** [cap. 01](01-git-y-github.md), [cap. 04](04-claves-y-datos-personales.md) y [metodologia.md](../../metodologia.md) §4.

### Fork

Copia de un repositorio ajeno en tu cuenta de GitHub, para proponer cambios. **En el curso no se usa**: partes de una plantilla.

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

### Hash de commit

Identificador único de un commit: 40 caracteres completo; con `git log -1 --format=%h` sale el **corto**, de 7. No lo confundas con el [hash y «sal»](#hash-y-sal) de las contraseñas.

*Ejemplo:* `ada5718`

**Dónde lo verás:** [entrega de hito](../entrega-de-hito.md).

### `.gitignore`

Fichero que lista lo que Git debe ignorar y no subir (claves, dependencias, ficheros temporales).

*Ejemplo:* Una línea `.env` hace que Git no suba tu fichero `.env`.

**Dónde lo verás:** [cap. 01](01-git-y-github.md) y [cap. 04](04-claves-y-datos-personales.md); ya viene en [`plantilla-proyecto/`](../../../plantilla-proyecto/).

### Issue

Ficha de GitHub para una tarea, un error o una corrección. En el curso cada tarea es un Issue con su definición de hecho.

*Ejemplo:* Issue #12 «Validar el formulario»

**Dónde lo verás:** [cap. 01](01-git-y-github.md) y [metodologia.md](../../metodologia.md) §4.1.

### Kebab-case

Escribir en minúsculas y unir las palabras con guiones, sin tildes ni espacios.

*Ejemplo:* `plan-de-riesgos`

**Dónde lo verás:** [cap. 01](01-git-y-github.md) (nombres de rama) y [cap. 09](09-opencode-skills-agentes.md) (carpetas de skills).

### `main`

La rama principal del repositorio. En el curso contiene solo la versión entregable: nunca trabajas directamente en ella.

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

### Merge commit («Create a merge commit»)

Forma de integrar un PR que une la rama con un commit de unión y **conserva tus commits tal cual**. Es la opción que usamos al pulsar Merge.

**Dónde lo verás:** [cap. 01](01-git-y-github.md) y [metodologia.md](../../metodologia.md) §4.

### Pull

Traer las novedades de GitHub a tu rama (`git fetch` y luego integrarlas). Es el camino inverso de `push`.

*Ejemplo:* `git pull`

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

### Pull Request (PR)

Petición de integrar tu rama en `main`. Se revisa en GitHub antes (vía A) o después (vía B) de integrar.

*Ejemplo:* PR #3 «docs: añade README»

**Dónde lo verás:** [cap. 01](01-git-y-github.md); [metodologia.md](../../metodologia.md) §4.

### Push

Subir tus commits a GitHub.

*Ejemplo:* `git push`

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

### Rama

Línea de trabajo independiente. Una rama, un cambio. Nombre `<tipo>/<kebab-case>`.

*Ejemplo:* `docs/plan-de-riesgos`, `feat/login`

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

### Rebase

Reescribir y recolocar commits. Existe, pero **aquí no se usa**, porque reescribe la historia.

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

### Repositorio (repo)

Carpeta de proyecto con todos sus ficheros y toda su historia de cambios. Hay uno local (en tu ordenador) y uno remoto (en GitHub).

*Ejemplo:* `proyecto-demo`

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

### Squash («Squash and merge»)

Forma de integrar un PR aplastando todos sus commits en uno. **No se usa**: perderías el detalle de tu historia.

**Dónde lo verás:** [cap. 01](01-git-y-github.md) y [metodologia.md](../../metodologia.md) §4.

### Tag (de Git) frente a label (de GitHub)

Las dos se traducen como «etiqueta», pero son cosas distintas. Un **tag** es un nombre fijo para un commit concreto: en cada hito se crea uno en `main` (`h1`, `h2`, `h3`). Una **label** es una pegatina de color que se pone a un Issue o PR para clasificarlo.

*Ejemplo:* Tag `h1` en `main` frente a label `necesita-tutor` en un PR

**Dónde lo verás:** [cap. 01](01-git-y-github.md) y [metodologia.md](../../metodologia.md) §4.

### Upstream

Rama remota con la que está enlazada tu rama local. Lo verás en mensajes que empiezan por `hint:`.

*Ejemplo:* `origin/docs/anade-readme`

**Dónde lo verás:** [cap. 01](01-git-y-github.md).

## Curso

### Briefing

La clase semanal de 1 hora (jueves): qué llevamos al día, bloqueos y siguiente paso. El trabajo se hace en casa durante la semana.

**Dónde lo verás:** [metodologia.md](../../metodologia.md) §5 y [contacto-y-ayuda.md](../contacto-y-ayuda.md).

### Declaración de uso de IA

Fichero `docs/declaracion-uso-ia.md` de tu repo donde anotas para qué has usado IA y qué has aceptado o cambiado. Usar IA está permitido; no declararla, no.

**Dónde lo verás:** [declaracion-uso-ia.md](../../../plantilla-proyecto/docs/declaracion-uso-ia.md); [cap. 10](10-ia-agentica-en-el-proyecto.md).

### Defensa oral

Presentación final en la que explicas y defiendes tu proyecto. Ahí se comprueba que lo has hecho y lo entiendes. El profesor te comunicará el formato y la duración.

**Dónde lo verás:** [metodologia.md](../../metodologia.md) §7 y [fases-del-proyecto.md](../../fases-del-proyecto.md).

### Definición de hecho

Lista de condiciones que dicen cuándo una tarea está terminada. Se escribe en cada Issue, antes de empezar.

*Ejemplo:* «Hecho cuando: el formulario rechaza correos vacíos y hay una prueba que lo demuestra.»

**Dónde lo verás:** [metodologia.md](../../metodologia.md) §4.1 y [cap. 06](06-requisitos-verificables.md).

### Fase

Cada parte ordenada del proyecto: análisis, diseño, planificación, implementación, pruebas, despliegue y mantenimiento. Las fases del curso son una adaptación didáctica del ciclo de vida del software.

**Dónde lo verás:** [fases-del-proyecto.md](../../fases-del-proyecto.md); [cap. 05](05-etapas-de-desarrollo.md).

### Historia de usuario

Forma corta de describir una necesidad desde quien usará el producto: qué quiere y para qué. Convención del curso: forma parte de los elementos de Scrum adaptados a un proyecto individual.

*Ejemplo:* «Como socia quiero cancelar una reserva para liberar la pista.»

**Dónde lo verás:** [metodologia.md](../../metodologia.md) §1; [cap. 05](05-etapas-de-desarrollo.md).

### Hito (H1, H2, H3)

Fecha de entrega fija. **H1: 26-nov. H2: 21-ene. H3: 7-may.** Fechas **provisionales** hasta que se apruebe el calendario del centro. En cada hito se crea un tag en `main`.

**Dónde lo verás:** [fases-del-proyecto.md](../../fases-del-proyecto.md); [cap. 05](05-etapas-de-desarrollo.md).

### Plantilla del proyecto

Repositorio modelo del que creas el tuyo (*Use this template*). Trae la carpeta `docs/` con los entregables, `.gitignore` y la configuración de GitHub.

**Dónde lo verás:** [`plantilla-proyecto/`](../../../plantilla-proyecto/).

### RA, CE y cómo leer «RA1 / 1f»

**RA** = Resultado de Aprendizaje (lo que debes ser capaz de hacer). **CE** = Criterio de Evaluación (cada punto concreto con el que se comprueba un RA, con letra: a, b, c…). «**RA1 / 1f**» = criterio **f** del RA1. El RA1 corresponde a la fase de análisis; el 1f trata de determinar las características del proyecto, que es donde entran los requisitos verificables. Texto oficial completo: no se copia aquí.

*Ejemplo:* RA2 = diseño, RA3 = planificación, RA4 = pruebas y seguimiento (correspondencia didáctica de la metodología).

**Dónde lo verás:** [metodologia.md](../../metodologia.md) §3; [cap. 06](06-requisitos-verificables.md).

### Registro de tutoría

Fichero `docs/registro-tutoria.md` de tu repo de proyecto donde anotas horas, bloqueos y qué te costó cada semana. Sirve para ayudarte, no para penalizarte.

**Dónde lo verás:** [registro-tutoria.md](../../../plantilla-proyecto/docs/registro-tutoria.md).

### Repo de práctica frente a repo del proyecto

El **repo de práctica** es uno de usar y tirar donde aprendes Git sin riesgo (no lleva registro de tutoría ni declaración de IA). El **repo del proyecto** es el tuyo de verdad, creado desde la plantilla, donde se evalúa tu trabajo.

**Dónde lo verás:** [cap. 01](01-git-y-github.md) (tarea).

### Tablero Kanban

Tablero con columnas que muestra el estado de cada tarea. En GitHub se hace con *Projects*.

*Ejemplo:* Backlog → Por hacer → En curso → En revisión → Hecho

**Dónde lo verás:** [metodologia.md](../../metodologia.md) §4.1; [cap. 05](05-etapas-de-desarrollo.md).

### Tutor

Convención del curso: el profesor del módulo. Es quien revisa tus PR y a quien escribes por correo (ver contacto y ayuda).

**Dónde lo verás:** [contacto-y-ayuda.md](../contacto-y-ayuda.md); [metodologia.md](../../metodologia.md).

### Vía A y vía B

Dos formas de revisión. **Vía A**: el tutor revisa **antes** de integrar (etiqueta `necesita-tutor`); no pulses Merge hasta su visto bueno. **Vía B**: revisa **después**, en la revisión semanal. Tu primer PR y los PR de los 7 días previos a un hito van por la vía A.

**Dónde lo verás:** [metodologia.md](../../metodologia.md) §4.2 bis; [cap. 01](01-git-y-github.md).

## Documentar y requisitos

### Dado / Cuando / Entonces

Plantilla para escribir un criterio de aceptación: **Dado** una situación inicial, **Cuando** pasa algo, **Entonces** debe ocurrir esto.

*Ejemplo:* Dado que la pista 3 está reservada, cuando otro socio intenta reservarla, entonces ve el aviso «pista ocupada».

**Dónde lo verás:** [cap. 06](06-requisitos-verificables.md).

### Fuente primaria / secundaria / oficial

**Primaria**: origen directo del dato (el texto de una ley, la documentación de una herramienta). **Secundaria**: alguien cuenta lo que dice la primaria (un blog, un resumen). **Oficial**: publicada por el propio organismo o proyecto. Prefiere siempre primaria y oficial.

**Dónde lo verás:** [cap. 08](08-sota-y-fuentes.md).

### Markdown

Lenguaje para dar formato a texto plano con símbolos sencillos. Los ficheros acaban en `.md`.

*Ejemplo:* `# Título` crea un título.

**Dónde lo verás:** [cap. 02](02-documentar-markdown-mermaid.md).

### Mermaid

Lenguaje de texto para dibujar diagramas dentro de un fichero Markdown. GitHub los dibuja solo. En el curso no se usan capturas de diagramas.

*Ejemplo:* `flowchart LR` empieza un diagrama de flujo.

**Dónde lo verás:** [cap. 02](02-documentar-markdown-mermaid.md).

### README

Fichero `README.md` que se muestra al abrir un repositorio: qué es el proyecto y cómo empezar.

**Dónde lo verás:** [cap. 01](01-git-y-github.md) y [cap. 02](02-documentar-markdown-mermaid.md).

### RF / RNF / REST

Tres tipos de requisito. **RF** (funcional): qué hace el sistema. **RNF** (no funcional): cómo lo hace (rendimiento, seguridad, accesibilidad…). **REST** (restricción): límite impuesto (plazo, presupuesto, tecnología). Aquí `REST` es una restricción; **no** tiene que ver con las API REST.

*Ejemplo:* RF-02 Crear una reserva · RNF-01 Carga en menos de 2 s · REST-01 Entrega antes del 7-may

**Dónde lo verás:** [cap. 06](06-requisitos-verificables.md).

### Ruta relativa

Dirección de un fichero contada desde el fichero donde estás, sin dirección web completa. `../` sube una carpeta.

*Ejemplo:* Desde este glosario, `../../metodologia.md` apunta a `docs/metodologia.md`.

**Dónde lo verás:** [cap. 02](02-documentar-markdown-mermaid.md).

### SOTA

Estado del arte: lo que ya existe hoy para resolver el problema de tu proyecto. Se documenta en `01b-sota.md`.

**Dónde lo verás:** [cap. 08](08-sota-y-fuentes.md).

### Trazabilidad

Poder seguir el hilo desde un objetivo hasta el requisito que lo cubre y la prueba que lo comprueba.

*Ejemplo:* OBJ-01 → RF-02 → P-07

**Dónde lo verás:** [cap. 06](06-requisitos-verificables.md).

### `verificado` / `declarado` / `no leído`

Estado de cada fuente. **verificado**: la has abierto y leído tú. **declarado**: alguien lo afirma (otra persona, una web o una IA) y tú no lo has comprobado. **no leído**: tienes la referencia pero no la has abierto. Diferencia: en «declarado» hay una afirmación sin comprobar; en «no leído» ni siquiera has mirado la fuente.

*Ejemplo:* Dato dicho por una IA → `declarado`. Enlace guardado para luego → `no leído`.

**Dónde lo verás:** [cap. 08](08-sota-y-fuentes.md); [README del 00](README.md).

## Datos y seguridad

### AEPD

Agencia Española de Protección de Datos: la autoridad que supervisa el cumplimiento del RGPD y la LOPDGDD en España.

**Dónde lo verás:** [cap. 04](04-claves-y-datos-personales.md).

### API

Conjunto de funciones que un programa o servicio ofrece para que otros programas lo usen. No confundir con la clave de API.

*Ejemplo:* Una API del tiempo devuelve la previsión de una ciudad.

**Dónde lo verás:** [cap. 04](04-claves-y-datos-personales.md), [cap. 07](07-ia-y-llm.md).

### Biblioteca y framework

**Biblioteca**: código ya hecho que llamas desde tu programa cuando lo necesitas. **Framework**: estructura que define cómo organizas tu programa y que te llama a ti.

**Dónde lo verás:** [cap. 07](07-ia-y-llm.md); [cap. 08](08-sota-y-fuentes.md).

### Dato personal

Información sobre una persona identificada o identificable (nombre, correo, teléfono, DNI…). En el proyecto: datos de prueba ficticios.

**Dónde lo verás:** [cap. 04](04-claves-y-datos-personales.md).

### `.env`

Fichero local donde guardas claves y ajustes como variables. **Nunca se sube**: va en `.gitignore`.

*Ejemplo:* `API_KEY=clave-demo-0000`

**Dónde lo verás:** [cap. 04](04-claves-y-datos-personales.md).

### `.env.example`

Copia de `.env` **sin valores reales** que sí se sube, para que se sepa qué variables hacen falta.

*Ejemplo:* `API_KEY=`

**Dónde lo verás:** [cap. 04](04-claves-y-datos-personales.md).

### Hash y «sal»

Un **hash** convierte un texto en una cadena fija que no se puede deshacer. Las contraseñas se guardan como hash, no tal cual. La **sal** es un dato aleatorio que se añade antes de calcularlo para que dos contraseñas iguales no den el mismo hash. En Git también verás «hash» como identificador de un commit; es otro uso de la palabra.

**Dónde lo verás:** [cap. 07](07-ia-y-llm.md) (ejemplo de IA con errores); [cap. 04](04-claves-y-datos-personales.md).

### LOPDGDD

Ley Orgánica 3/2018 de Protección de Datos Personales y garantía de los derechos digitales. Concreta el RGPD en España.

**Dónde lo verás:** [cap. 04](04-claves-y-datos-personales.md).

### OWASP

Organización que publica guías de seguridad para aplicaciones web. Se cita en el cap. 07 como ejemplo de dónde contrastar.

**Dónde lo verás:** [cap. 07](07-ia-y-llm.md).

### RGPD

Reglamento (UE) 2016/679, la norma europea de protección de datos personales.

**Dónde lo verás:** [cap. 04](04-claves-y-datos-personales.md).

### Secret scanning

Servicio de GitHub que busca claves y credenciales subidas por error en un repositorio, incluido su historial. Que exista no te exime: si subes una clave, anúlala.

**Dónde lo verás:** [cap. 04](04-claves-y-datos-personales.md).

### Token de acceso / clave de API

Texto largo que da acceso a un servicio con ciertos permisos, como una llave. Se trata como una contraseña: no va al repo ni a un chat de IA. **No es lo mismo que el token de un modelo de IA** (ver más abajo).

*Ejemplo:* `ghp_...` (ejemplo de forma; nunca pegues uno real)

**Dónde lo verás:** [cap. 01](01-git-y-github.md) y [cap. 04](04-claves-y-datos-personales.md).

## IA

### Agente

IA con instrucciones, herramientas y permisos propios. En OpenCode hay agentes principales (conversan contigo) y subagentes (ayudantes para una subtarea).

**Dónde lo verás:** [cap. 09](09-opencode-skills-agentes.md); [cap. 10](10-ia-agentica-en-el-proyecto.md).

### Alucinación

Respuesta que suena bien pero es falsa o inventada. Por eso se contrasta con fuentes.

*Ejemplo:* Una función que no existe en la biblioteca.

**Dónde lo verás:** [cap. 07](07-ia-y-llm.md); [cap. 08](08-sota-y-fuentes.md).

### IA, machine learning y LLM

**IA**: sistemas que hacen tareas que parecen inteligentes. **Machine learning** (aprendizaje automático): el sistema ajusta su fórmula interna a partir de muchos ejemplos en vez de seguir reglas escritas. **LLM** (*large language model*): modelo entrenado con mucho texto que genera texto prediciendo la siguiente pieza.

**Dónde lo verás:** [cap. 07](07-ia-y-llm.md).

### OpenCode (V1 frente a V2)

Programa de terminal con un agente de IA que puede leer y editar tu proyecto si se lo permites. Tiene dos versiones: en el curso usamos la **V2** (paquete `@opencode/cli`; `opencode --version` debe empezar por `v2.`). La V1 (paquete `opencode-ai`) no sirve para nuestra configuración (conclusión del proyecto) y la mayoría de tutoriales de internet son de la V1.

**Dónde lo verás:** [cap. 09](09-opencode-skills-agentes.md).

### Parámetros (de un modelo)

Los números internos que el modelo ajustó al entrenarse; un modelo grande tiene miles de millones. No son los parámetros de una función de programación.

*Ejemplo:* GPT-3: 175.000 millones de parámetros.

**Dónde lo verás:** [cap. 07](07-ia-y-llm.md).

### Permiso (`allow` / `ask` / `deny`)

Regla que dice si un agente puede usar una herramienta: `allow` sin preguntar, `ask` preguntándote, `deny` nunca. Si ninguna regla encaja, pregunta.

*Ejemplo:* Editar ficheros: `ask`

**Dónde lo verás:** [cap. 09](09-opencode-skills-agentes.md).

### Plan B sin IA

Saber cómo harías la tarea sin IA, por si se acaba la cuota o falla el servicio. El hito no se mueve.

**Dónde lo verás:** [cap. 09](09-opencode-skills-agentes.md); [cap. 10](10-ia-agentica-en-el-proyecto.md).

### Prompt

El texto que le envías al modelo: instrucciones, contexto y petición.

*Ejemplo:* «Explícame qué hace este método Java en 5 líneas.»

**Dónde lo verás:** [cap. 07](07-ia-y-llm.md).

### Skill

Carpeta con un `SKILL.md` de instrucciones que el agente carga cuando la tarea lo pide.

*Ejemplo:* `.opencode/skills/revisar-requisito/SKILL.md`

**Dónde lo verás:** [cap. 09](09-opencode-skills-agentes.md).

### Token (de un modelo de IA)

Trozo de texto que el modelo procesa (palabra, parte de palabra o signo). La cuota se mide en tokens. **No es el token de acceso** de GitHub.

*Ejemplo:* «programación» puede partirse en 2-3 tokens.

**Dónde lo verás:** [cap. 07](07-ia-y-llm.md).

### Ventana de contexto

Todo lo que el modelo puede «tener delante» a la vez: tu conversación, los ficheros que le das y su respuesta. Si se llena, lo antiguo puede perderse.

**Dónde lo verás:** [cap. 07](07-ia-y-llm.md).

## Otros

### C4

Modelo para dibujar la arquitectura de un sistema en niveles (contexto, contenedores, componentes, código). **No hace falta para el hito H1**; se pide en el diseño (H2).

**Dónde lo verás:** [metodologia.md](../../metodologia.md) §2; [`02-diseno.md`](../../../plantilla-proyecto/docs/02-diseno.md).

### Lighthouse

Herramienta de Google (integrada en el navegador Chrome) que mide calidad de una página: rendimiento, accesibilidad, buenas prácticas.

*Ejemplo:* «Accesibilidad ≥ 90 en Lighthouse» como requisito.

**Dónde lo verás:** [cap. 06](06-requisitos-verificables.md).

### Terminal (según el sistema operativo)

Ventana donde escribes comandos. En **Windows**, el instalador de Git incluye *Git Bash* (o PowerShell si ya la manejas). En **macOS**, la aplicación *Terminal*. En **Linux**, la terminal de tu distribución. Los detalles de cada sistema: ver el cap. 01.

*Ejemplo:* `git --version`

**Dónde lo verás:** [cap. 01](01-git-y-github.md) (paso 0a).

---

Volver al [índice de fundamentos](README.md).
