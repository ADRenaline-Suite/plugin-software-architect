---
name: describe-architecture
description: Writes the 4+1 document and the arc42 manual so a reader can follow them. Each section is a few plain sentences and one diagram. Use it when someone asks what the system is, how the code is organized, how the parts call each other, where they run, or for the architecture manual.
---

<p align="right">Idioma:&emsp;<a href="SKILL.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Arquitecto de software](../../README.es.md)

# Describir la arquitectura

Escribe un documento que se pueda seguir sin conocer el método. El 4+1 es un archivo con cinco secciones. El manual arc42 es otro archivo. Cita el 4+1. No lo copia.

Fuente: ISO/IEC/IEEE 42010:2022 (entidad de interés, interesados, preocupaciones, puntos de vista, vistas). Plantilla arc42 9.1, inglés, octubre de 2026. Philippe Kruchten, «Architectural Blueprints — The 4+1 View Model of Software Architecture», IEEE Software, 1995. C4, Simon Brown (https://c4model.com/), solo para la sección de contexto.

## Antes de escribir

1. Lee solo la referencia de esta situación: [4plus1](references/4plus1.es.md), [logical](references/logical.es.md), [development](references/development.es.md), [process](references/process.es.md), [physical](references/physical.es.md), [scenarios](references/scenarios.es.md), [arc42](references/arc42.es.md), [context](references/context.es.md), [strategy](references/strategy.es.md), [concepts](references/concepts.es.md), [risks](references/risks.es.md) o [glossary](references/glossary.es.md).
2. Un command nombra una referencia. Escribe solo esa situación.
3. Un pedido de 4+1 que no nombra command hace lo mismo que `/arch-4plus1`. Un pedido del manual arc42 que no nombra command hace lo mismo que `/arch-arc42`.
4. Lee la carpeta o los archivos que la persona nombró. Usa los nombres que estén ahí. Una parte, una llamada, un puerto o un nodo que ninguna fuente nombró no se escribe. El hueco es una línea en esa sección.
5. No escribas el caso de uso, el contrato OpenAPI, el modelo de amenazas, el modelo de datos ni el modelo de dominio. Pide ese plugin. Cita lo que ya escribió.
6. No dibujes un diagrama UML en este archivo. Pide a `plugin-uml-diagrams` cuando la referencia lo diga, y enlaza el archivo que escriba.

## Diagramas

Cada sección que la referencia marca como explicada lleva un diagrama en el mismo archivo.

1. Primero dos o tres frases cortas. Dicen qué está mirando quien lee.
2. Después un diagrama Mermaid. Las cajas son partes que una fuente nombró. Las flechas son relaciones que una fuente nombró. Las etiquetas van en el idioma del artefacto.
3. Debajo del diagrama, una frase dice qué muestra la figura.
4. El diagrama es una explicación. No lo llames UML, C4 ni un archivo PlantUML.
5. Cuando la referencia pida un dibujo UML, pídelo a `plugin-uml-diagrams` con ese tipo y esa versión, y enlaza el `.svg` que guardó. El Mermaid se queda en este documento para que se pueda leer solo.

## Idioma

Las instrucciones siguen en inglés. El artefacto va en el idioma del pedido. Si el pedido nombra un idioma, se usa ese. Si no, se usa el idioma en el que está escrito el pedido. Se conservan los nombres que la persona ya usó. Los encabezados de la plantilla se traducen y los campos se mantienen. El tipo en el nombre del archivo sigue siendo el id en inglés. Las columnas de `STATUS.md` siguen `N`, `archivo`, `estado`, `sustituye`, `notas`. La respuesta usa ese mismo idioma. Los prompts de la referencia están en inglés: se muestran en el idioma del pedido y los nombres de command no se traducen.

## Si falta un prerrequisito

`/arch-4plus1` igual escribe el archivo. Una sección sin hechos lista el hueco y el archivo se queda `proposed`. La sección de escenarios se queda en hueco hasta que se cite un caso de uso. Las otras secciones se escriben.

`/arch-arc42` igual escribe el archivo. Una sección que solo puede citar una pieza que falta lista esa pieza y el command que la escribe. El archivo se queda `proposed` hasta que la entidad de interés, los interesados, las preocupaciones y la sección de contexto tengan hechos. No los inventa.

Un command de una sola sección sin hechos no escribe archivo.

Cuando el hueco pide a la persona un hecho, escribe las mismas cuatro partes en esa sección del reporte y en el chat. Usa el idioma del pedido. Conserva los nombres de los commands.

1. Qué falta. Dos o tres frases. Nombra el hecho que falta, dice qué hace esta sección con él y qué no redacta. Dice que el archivo se queda `proposed` hasta que ese hecho se cite.
2. Cómo llenarlo. Los pasos, en orden. Dice de dónde sale el hecho: texto que la persona pega, o un archivo accepted del plugin que lo posee. Si ya existe un archivo de este tema, lo nombra y dice que se enmiende.
3. Plantilla. El prompt de la referencia, relleno con lo que la persona ya dijo. Donde aún falte un valor, deja el hueco (`#…`).
4. Ejemplo. Un mensaje ya relleno, después de la plantilla. Conserva los nombres que la persona ya usó y rellena solo los huecos con valores de muestra. Su primera línea dice que es una muestra para reemplazar, que no es una cita y que esos valores de muestra no son hechos del documento.

Un hueco que no pide escribir nada se queda en una línea.

## Entrega

La carpeta es `adrenaline/software-architect/` en la raíz del proyecto. Si `.cursor/adrenaline.json` tiene `outputDirs["plugin-software-architect"]` con una ruta relativa, sin `..` y no absoluta, se usa esa. Si falta el archivo, la clave o una ruta válida, se usa `adrenaline/software-architect/` y, en el último caso, se dice. Si `adrenaline/software-architect/` aún no existe y `software-architect/` en la raíz ya tiene el `ORIGIN.json` o el `STATUS.md` de este plugin, se sigue escribiendo ahí y se dice. Crea la carpeta si no existe. No escribas fuera de ella. Si la persona nombra un proyecto, una app, un servicio o un dominio, el archivo de ese asunto va en `<asunto>/`. Un archivo de todo el producto se queda en la raíz de la salida. `<NNN>` es el siguiente libre de toda la carpeta. La celda `archivo` es `<asunto>/<archivo>` cuando hay asunto (`adrenaline/software-architect/008-adr-asunto-subcarpeta.md`).

El archivo es `<NNN>-<tipo>-<tema>.md`. `<NNN>` es el siguiente entero libre, de tres dígitos, y no se reutiliza. `<tipo>` es el id en inglés de la referencia.

Mantén `<carpeta>/STATUS.md` con las columnas `N`, `archivo`, `estado`, `sustituye` y `notas`.

Mantén `<carpeta>/ORIGIN.json` junto a `STATUS.md`. No es un archivo `<NNN>` y no tiene fila en `STATUS.md`. Se escribe al crear la carpeta. En una entrega posterior, se vuelve a escribir solo si falta o si un campo difiere. Los campos son `suite` `ADRenaline-Suite`, `plugin` `plugin-software-architect`, `repository` `https://github.com/ADRenaline-Suite/plugin-software-architect` y `convention` `adr-001`. El marcador nombra la carpeta. No dice que cada archivo de dentro esté intacto.

`notas` lista `sources: <ruta relativa>; read: <marca UTC>` con `yyyy-MM-ddTHH:mm:ssZ`. No pongas `|` dentro de `notas`. Las rutas son relativas a la raíz del proyecto, sin `..`.

Si el tema ya tiene un archivo:

- Quien pide enmendar ese mismo archivo: se edita, se conserva el `<NNN>` y se conserva `accepted` si ya lo estaba.
- Un reemplazo o una decisión nueva sobre el mismo tema: el siguiente `<NNN>`, y la fila anterior pasa a `superseded` (`sustituye` apunta al `N` nuevo).
- Tema nuevo: el siguiente `<NNN>`.

`accepted` cuando cada sección que la referencia exige tiene hechos y un diagrama, y no queda hueco. `proposed` cuando una sección lista un hueco. Al cerrar, di la carpeta, el archivo, el `N` y el estado.

## Hecho

Antes de cerrar, evalúa esta lista y la lista `## Done` de la referencia de esta situación. Un command fija la situación: usa la referencia que ese command nombra. Cada ítem es cierto, o corriges la entrega en este turno. No dejes un archivo que falle un ítem. No lo marques `accepted` mientras un ítem falle. Una plantilla que la referencia nombra se aplica y se anota en Assumed; la entrega usa el estado que esa referencia nombra. Un prerrequisito que aún detiene la entrega no es una lista fallida: sigue «Si falta un prerrequisito» y no escribas archivos de esa pieza.

- La situación de este turno es la única que se escribe, salvo que el pedido pida dos. Cada entrega tiene su `<NNN>`.
- Los archivos están solo en la carpeta de salida, con el nombre que dice Entrega. `<NNN>` no se reutiliza. `STATUS.md` coincide con los archivos y con el estado que esta situación permite. `ORIGIN.json` está en esa carpeta, sus cuatro campos coinciden con este plugin y no tiene fila en `STATUS.md`. Un hueco que la referencia deja en `proposed` se queda `proposed`.
- El idioma del artefacto coincide con el pedido. Las columnas de `STATUS.md` siguen `N`, `archivo`, `estado`, `sustituye`, `notas`.
- Cada sección que la referencia exige está presente. Cada sección explicada tiene unas frases claras y un diagrama Mermaid. El diagrama no se llama UML. Un archivo UML que esta referencia pide está enlazado, o la sección dice que se pidió a `plugin-uml-diagrams` y aún no volvió.
- No se inventó ninguna parte. Un hueco que pide a la persona un hecho es el hueco de cuatro partes en el reporte y en la respuesta: qué falta, cómo llenarlo, la plantilla y un ejemplo. El ejemplo está marcado como muestra y no es un hecho. Un hueco que no pide escribir nada se queda en una línea.
- La respuesta nombra la carpeta, los archivos, el `N` y el estado. Cuando un prerrequisito detiene la pieza, la respuesta es ese mismo hueco de cuatro partes y no nombra un archivo nuevo.

## Ejemplo

Entrada: una carpeta `apps/` cuyo `README.md` nombra tres aplicaciones, `counter`, `cart` y `orders`, y dice que el carrito publica un evento que orders lee. El pedido es «escribe el 4+1 de apps, en español», y no nombra command.

Salida: `001-4plus1-counter-cart-orders.md`, estado `proposed`. Las secciones Lógica, Desarrollo, Proceso y Física tienen un texto corto y un diagrama Mermaid que usa solo esos tres nombres y el evento que el README dijo. La sección Escenarios y la respuesta usan las mismas cuatro partes: qué falta (casos de uso para citar, no para redactar), cómo llenarlo, la plantilla con `#casos-de-uso` y un mensaje de muestra. La muestra no es un caso de uso citado. La respuesta nombra `adrenaline/software-architect/`, el archivo, `001` y `proposed`.
