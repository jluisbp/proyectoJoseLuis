# Cómo hacer obligaciones y ayudas (H1-C)

Para: `01-analisis.md` §5 y §6 · Tiempo orientativo: 240 min

## Qué te piden

- **CE 1g:** decir qué **obligaciones fiscales, laborales y de prevención de riesgos laborales (PRL)** afectan a tu proyecto, cada una **con su norma** y a quién aplica.
- **CE 1h:** encontrar **al menos una ayuda o subvención real** para incorporar tecnología, con quién puede pedirla, qué cubre, el plazo y la fuente.

**Hecho** es: una tabla de obligaciones con su norma abierta y leída, y una ficha de ayuda con su convocatoria localizada.

Tres palabras que usarás:

- **Obligación:** algo que la ley exige hacer a la empresa que usará tu proyecto (o a ti, si lo vendes). No es una opinión.
- **PRL:** prevención de riesgos laborales, las normas para que trabajar no dañe la salud.
- **Convocatoria:** el anuncio oficial de una ayuda, con sus bases y su plazo.

## Dónde buscar

Solo fuentes oficiales. Una gestoría o un blog sirven para entender, pero **cita siempre la norma o la convocatoria original**.

- **BOE** ([boe.es](https://www.boe.es)): busca la ley por su nombre y número. Es el texto de la norma.
- **Agencia Tributaria** ([sede.agenciatributaria.gob.es](https://sede.agenciatributaria.gob.es)): impuestos y facturación.
- **Seguridad Social** ([sede.seg-social.gob.es](https://sede.seg-social.gob.es)): altas de autónomos y trabajadores.
- **INSST** (Instituto Nacional de Seguridad y Salud en el Trabajo, [insst.es](https://www.insst.es)): prevención de riesgos laborales.
- **AEPD** ([aepd.es](https://www.aepd.es)): protección de datos (ya tienes el [capítulo 04](../00-fundamentos/04-claves-y-datos-personales.md); aquí solo la nombras).
- **Ayudas:** la Base de Datos Nacional de Subvenciones (BDNS), [infosubvenciones.es](https://www.infosubvenciones.es/bdnstrans/GE/es/convocatorias), recoge convocatorias de todas las administraciones con su código BDNS. En Asturias, mira también [SEKUENS (IDEPA)](https://www.idepa.es/busca-financiacion), [Asturias Emprende](https://asturiasemprende.es/) y el Boletín Oficial del Principado de Asturias (BOPA).

Reglas de fuentes: cada dato lleva **enlace y fecha de acceso**. Si usas IA, **abre la norma** y comprueba que existe y dice eso; puede inventar artículos, plazos y ayudas. Decláralo en `docs/declaracion-uso-ia.md`.

## Pasos

1. **Describe a quién ayuda tu proyecto:** autónomo, sociedad o asociación; con personal o sin él; su sector y su lugar.
2. **Recorre estas cuatro preguntas** y apunta qué obligación toca a ese cliente:
   - ¿Factura? Entonces hay **IVA**, **impuesto sobre la renta o sociedades** y normas de **facturación**.
   - ¿Tiene personas contratadas? Entonces hay **alta en la Seguridad Social**, **contrato**, **convenio colectivo** (el acuerdo que fija salarios y condiciones de un sector) y **registro de jornada** (anotar cada día la hora de entrada y salida de la plantilla).
   - ¿Su plantilla trabaja con pantallas? Entonces hay **PRL**.
   - ¿Tu app guarda datos de personas? Entonces hay **protección de datos**.
3. **Busca la norma de cada una** en el BOE o en la sede oficial, **ábrela y lee solo el artículo o el apartado que aplica**, no la ley entera. Con **una norma por familia** (fiscal, laboral, prevención) cumples el mínimo. Apunta el nombre, el número y el enlace.
4. **Mira si tu propio software entra en juego.** Si tu app emite facturas, la norma de facturación se aplica también a ti (ver «Ojo con los cambios»).
5. **Busca una ayuda:** en BDNS y en los portales de Asturias, filtra por tu tipo de entidad y por «tecnología» o «digitalización». Localiza la convocatoria y sus bases.
6. **Rellena la ficha de la ayuda** con las cinco cosas: quién puede pedirla, qué gasto cubre (y cuál excluye), cuánto, plazo y cómo se solicita. Anota si está **abierta**, **cerrada** o **no comprobada**.
7. **Escribe lo que no pudiste comprobar.** Es mejor que fingir.

## Ojo con los cambios

Algunas fechas de facturación han cambiado varias veces. No copies una fecha de una web: **mira la nota oficial vigente** y anota cuándo la consultaste.

- **Facturación con software.** La Ley 11/2021 y el reglamento RD 1007/2023 (el sistema se conoce como Veri\*Factu) exigen que los programas de facturación garanticen la integridad y la trazabilidad de las facturas, y alcanzan también a quien los desarrolla o vende. Su calendario se reformó en el RDL 15/2025; consulta la [nota de la AEAT sobre Veri\*Factu](https://sede.agenciatributaria.gob.es/Sede/iva/sistemas-informaticos-facturacion-verifactu/nota-informativa-ampliacion-plazo-adaptacion-facturacion.html). Se habla de un nuevo aplazamiento, pero cuando se redactó esta guía no había norma publicada.
- **Factura electrónica entre empresas.** Se regula en la Ley 18/2022 y el RD 238/2026. Los plazos de aplicación cuentan desde que entre en vigor una orden ministerial: comprueba si ya se ha publicado y qué fecha fija.
- **Kit Digital.** Es la ayuda más conocida, pero sus convocatorias están cerradas: no la uses como tu ayuda.

## Ejemplo resuelto

Proyecto ficticio común: **Taller Rueda Libre**, un taller de reparación de bicicletas con dos mecánicos y una persona en administración, constituido como S. L., en Asturias. Todo es **ficticio**.

| Obligación | Por qué le toca | Norma (con enlace) | Estado |
|---|---|---|---|
| IVA y facturas | Vende reparaciones y piezas | [Ley 37/1992](https://www.boe.es/buscar/act.php?id=BOE-A-1992-28740) | `sin leer` |
| Impuesto sobre Sociedades | Es una S. L. | [Ley 27/2014](https://www.boe.es/buscar/act.php?id=BOE-A-2014-12328) | `sin leer` |
| Facturación con software | La app de citas también emitirá facturas | [Ley 11/2021](https://www.boe.es/buscar/act.php?id=BOE-A-2021-11473) y calendario en la [nota de la AEAT](https://sede.agenciatributaria.gob.es/Sede/iva/sistemas-informaticos-facturacion-verifactu/nota-informativa-ampliacion-plazo-adaptacion-facturacion.html) | `leído` el calendario (12-nov-2026) |
| Alta de trabajadores | Tiene personal | [Ley General de la Seguridad Social](https://www.boe.es/buscar/act.php?id=BOE-A-2015-11724), art. 16 | `leído` |
| Contrato y registro de jornada | Tiene personal | [Estatuto de los Trabajadores](https://www.boe.es/buscar/act.php?id=BOE-A-2015-11430), arts. 8 y 34.9 | `leído` |
| Convenio colectivo | Tiene personal | Se busca por su actividad en la herramienta REGCON (Registro de Convenios Colectivos) del Ministerio de Trabajo | `sin leer`: dilo así |
| PRL | La administración usa pantalla todo el día | [Ley 31/1995](https://www.boe.es/buscar/act.php?id=BOE-A-1995-24292), arts. 14 a 16, y [RD 488/1997](https://www.boe.es/buscar/act.php?id=BOE-A-1997-8671) | `leído` |

Ayuda (el caso es ilustrativo; la búsqueda y la lectura de bases son reales): en BDNS, con el filtro «Asturias» y la palabra «digitalización», se localiza una convocatoria de digitalización del comercio. El extracto del BOPA dice quién puede pedirla, el porcentaje, el plazo y qué gasto excluye. Resultado de la ficha: **cerrada**, con la fecha de cierre y dónde se publicará la siguiente. Una ayuda cerrada con su ficha completa **vale** si dices que está cerrada.

## Hecho cuando

- [ ] Cada obligación de la tabla lleva su norma con **enlace** y fecha de acceso (1g).
- [ ] Hay obligaciones de las tres familias: fiscales, laborales y de prevención (1g).
- [ ] Cada obligación tiene una columna «Estado» con `leído` o `sin leer`; las que no pude leer lo dicen (1g).
- [ ] La ayuda tiene su convocatoria localizada (código BDNS o boletín), con el enlace (1h).
- [ ] La ficha dice quién puede pedirla, qué cubre, el importe, el plazo y si está abierta o cerrada (1h).
- [ ] Hay un apartado de «lo que no pude comprobar».

## 3 errores típicos

1. **Citar una web de gestoría como norma.** Sirve para entender, pero la fuente es la ley o la convocatoria.
2. **Copiar una fecha sin comprobarla.** Las de facturación han cambiado varias veces; anota cuándo la consultaste.
3. **Dar por buena una ayuda de una noticia.** Sube a la convocatoria y sus bases; si no las encuentras, no es una fuente.

¿Atascado más de 10 minutos? Escribe → [cómo pedir ayuda](../contacto-y-ayuda.md)
