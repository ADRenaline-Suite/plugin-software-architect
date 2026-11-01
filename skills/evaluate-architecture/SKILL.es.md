---
name: evaluate-architecture
description: Evaluates one architecture concern. It writes the quality scenario, the options and the tradeoff, and the decision record, with a diagram of the choice. Use it when someone asks which option to pick, or to record a decision already taken.
---

<p align="right">Idioma:&emsp;<a href="SKILL.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Arquitecto de software](../../README.es.md)

# Evaluar la arquitectura

Una evaluación es una decisión, en tres pasos. El escenario dice la preocupación de forma que se pueda comprobar. El tradeoff compara las opciones. El ADR registra la opción elegida. Un paso sin el anterior se queda `proposed` y nombra el command que llena el hueco.

Fuente: ISO/IEC/IEEE 42030:2019. ISO/IEC 25010:2023, los nueve nombres de calidad de producto. Escenario de atributo de calidad como lo usan ATAM (SEI) y el Quality Attribute Workshop: origen del estímulo, estímulo, entorno, artefacto, respuesta y medida. ADR, Michael Nygard: estado, contexto, decisión y consecuencias.

## Antes de escribir

1. Lee solo la referencia de esta situación: [quality-scenario](references/quality-scenario.es.md), [tradeoff](references/tradeoff.es.md), [adr](references/adr.es.md) o [evaluation](references/evaluation.es.md).
2. Un command nombra una referencia. Escribe solo esa situación.
3. Un pedido de evaluar una arquitectura que no nombra command hace lo mismo que `/arch-evaluation`.
4. Nombra la característica de calidad con un nombre vigente de ISO/IEC 25010:2023: idoneidad funcional, eficiencia de desempeño, compatibilidad, capacidad de interacción, fiabilidad, seguridad, mantenibilidad, flexibilidad o safety. No uses usabilidad ni portabilidad.
5. Una evaluación sin al menos dos opciones no está completa. Se queda `proposed`.
6. No dibujes un diagrama UML aquí. Si hace falta una vista para juzgar las opciones, pídela a `plugin-uml-diagrams` y enlázala. No escribas el caso de uso, el escenario de prueba ni el modelo de amenazas.

## Diagramas

El tradeoff y la evaluación completa incluyen un diagrama Mermaid. Las cajas son las opciones que una fuente nombró. Una flecha marca la opción elegida, y solo cuando ya hay decisión. Debajo de la figura, una frase dice qué muestra. El diagrama es una explicación. No lo llames UML.

## Idioma

Las instrucciones siguen en inglés. El artefacto va en el idioma del pedido. Si el pedido nombra un idioma, se usa ese. Si no, se usa el idioma en el que está escrito el pedido. Se conservan los nombres que la persona ya usó. Los encabezados de la plantilla se traducen y los campos se mantienen. El tipo en el nombre del archivo sigue siendo el id en inglés. Las columnas de `STATUS.md` siguen `N`, `archivo`, `estado`, `sustituye`, `notas`. La respuesta usa ese mismo idioma.

## Si falta un prerrequisito

Un command de un solo paso sin preocupación, o un ADR sin decisión, no escribe archivo.

Cuando el hueco pide a la persona un hecho, escribe las mismas cuatro partes en esa sección del reporte y en el chat. Usa el idioma del pedido. Conserva los nombres de los commands.

1. Qué falta. Dos o tres frases. Nombra el hecho que falta, dice qué hace esta sección con él y qué no redacta. Dice que el archivo se queda `proposed` hasta que ese hecho se cite.
2. Cómo llenarlo. Los pasos, en orden. Dice de dónde sale el hecho: texto que la persona pega, o un archivo accepted del plugin que lo posee. Si ya existe un archivo de este tema, lo nombra y dice que se enmiende.
3. Plantilla. El prompt de la referencia, relleno con lo que la persona ya dijo. Donde aún falte un valor, deja el hueco (`#…`).
4. Ejemplo. Un mensaje ya relleno, después de la plantilla. Conserva los nombres que la persona ya usó y rellena solo los huecos con valores de muestra. Su primera línea dice que es una muestra para reemplazar, que no es una cita y que esos valores de muestra no son hechos del documento.

Un hueco que no pide escribir nada se queda en una línea.

`/arch-evaluation` igual escribe el archivo de evaluación. Un paso que falta es ese hueco de cuatro partes y el archivo se queda `proposed`. La respuesta repite esas cuatro partes.

## Entrega

La carpeta es `adrenaline/software-architect/` en la raíz del proyecto. Si `.cursor/adrenaline.json` tiene `outputDirs["plugin-software-architect"]` con una ruta relativa, sin `..` y no absoluta, se usa esa. Si falta el archivo, la clave o una ruta válida, se usa `adrenaline/software-architect/` y, en el último caso, se dice. Si `adrenaline/software-architect/` aún no existe y `software-architect/` en la raíz ya tiene el `ORIGIN.json` o el `STATUS.md` de este plugin, se sigue escribiendo ahí y se dice. Crea la carpeta si no existe. No escribas fuera de ella.

El archivo es `<NNN>-<tipo>-<tema>.md`. `<NNN>` es el siguiente entero libre, de tres dígitos, y no se reutiliza. `<tipo>` es el id en inglés de la referencia.

Mantén `<carpeta>/STATUS.md` con las columnas `N`, `archivo`, `estado`, `sustituye` y `notas`.

Mantén `<carpeta>/ORIGIN.json` junto a `STATUS.md`. No es un archivo `<NNN>` y no tiene fila en `STATUS.md`. Se escribe al crear la carpeta. En una entrega posterior, se vuelve a escribir solo si falta o si un campo difiere. Los campos son `suite` `ADRenaline-Suite`, `plugin` `plugin-software-architect`, `repository` `https://github.com/ADRenaline-Suite/plugin-software-architect` y `convention` `adr-001`.

`notas` lista `sources: <ruta relativa>; read: <marca UTC>` con `yyyy-MM-ddTHH:mm:ssZ`. No pongas `|` dentro de `notas`.

Si el tema ya tiene un archivo:

- Quien pide enmendar ese mismo archivo: se edita, se conserva el `<NNN>` y se conserva `accepted` si ya lo estaba.
- Un reemplazo: el siguiente `<NNN>`, y la fila anterior pasa a `superseded`.
- Tema nuevo: el siguiente `<NNN>`.

`accepted` cuando los campos que la referencia exige están llenos y el tradeoff nombra al menos dos opciones. `proposed` cuando queda un hueco. Un ADR accepted es lo que cita `/arch-arc42`. Al cerrar, di la carpeta, el archivo, el `N` y el estado.

## Hecho

Antes de cerrar, evalúa esta lista y la lista `## Done` de la referencia de esta situación. Un command fija la situación: usa la referencia que ese command nombra. Cada ítem es cierto, o corriges la entrega en este turno. No dejes un archivo que falle un ítem. No lo marques `accepted` mientras un ítem falle. Una plantilla que la referencia nombra se aplica y se anota en Assumed; la entrega usa el estado que esa referencia nombra. Un prerrequisito que aún detiene la entrega no es una lista fallida: sigue «Si falta un prerrequisito» y no escribas archivos de esa pieza.

- La situación de este turno es la única que se escribe, salvo que el pedido pida dos. Cada entrega tiene su `<NNN>`.
- Los archivos están solo en la carpeta de salida, con el nombre que dice Entrega. `<NNN>` no se reutiliza. `STATUS.md` coincide con los archivos y con el estado que esta situación permite. `ORIGIN.json` está en esa carpeta, sus cuatro campos coinciden con este plugin y no tiene fila en `STATUS.md`. Un hueco que la referencia deja en `proposed` se queda `proposed`.
- El idioma del artefacto coincide con el pedido. Las columnas de `STATUS.md` siguen `N`, `archivo`, `estado`, `sustituye`, `notas`.
- El nombre de calidad es uno de los nueve de ISO/IEC 25010:2023. El escenario tiene seis partes. El tradeoff nombra al menos dos opciones, o el archivo se queda `proposed`.
- El diagrama, cuando esta situación lo lleva, muestra solo opciones que fueron nombradas. No se llama UML.
- No se inventó ninguna parte. Un hueco que pide a la persona un hecho es el hueco de cuatro partes en el reporte y en la respuesta: qué falta, cómo llenarlo, la plantilla y un ejemplo. El ejemplo está marcado como muestra y no es un hecho. Un hueco que no pide escribir nada se queda en una línea.
- La respuesta nombra la carpeta, los archivos, el `N` y el estado. Cuando un prerrequisito detiene la pieza, la respuesta es ese mismo hueco de cuatro partes y no nombra un archivo nuevo.

## Ejemplo

Entrada: «el catálogo debe responder 2.000 lecturas por segundo en pico, por debajo de 200 ms, sin perder pedidos. Opciones: una réplica de lectura o una caché.» El pedido está en español y no nombra command.

Salida: `001-evaluation-lecturas-del-catalogo.md`, estado `proposed`, porque aún no se elige una opción. El escenario tiene seis partes. El Mermaid muestra las dos opciones y ninguna flecha de elección. La respuesta nombra `adrenaline/software-architect/`, el archivo, `001` y `proposed`, y dice que `/arch-evaluation-adr` registra la elección.
