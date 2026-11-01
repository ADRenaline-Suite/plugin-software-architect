<p align="right">Idioma:&emsp;<a href="logical.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Arquitecto de software](../../../README.es.md) / [Describir la arquitectura](../SKILL.es.md)

# Vista lógica

Fuente: Philippe Kruchten, IEEE Software, 1995. El tipo de archivo es `logical`. Es una sección del 4+1. El documento entero es `/arch-4plus1`.

## Qué fija

La responsabilidad de cada parte. Las cajas son las partes. Las flechas son solo las responsabilidades que una fuente dijo.

## Cómo hacerlo

1. Lee la carpeta que la persona nombró.
2. Escribe unas frases claras y después un diagrama Mermaid, como dice el skill.
3. No añadas las otras cuatro vistas en este archivo.

## Prompt

`/arch-4plus1-logical` Lee la carpeta #carpeta. Escribe esta vista de #sistema en #idioma.

## Done

- El archivo usa los campos de la plantilla. Un hueco es una línea, no una suposición.
- Una sección explicada tiene unas frases claras y un diagrama Mermaid. El diagrama no se llama UML.
- El estado es `accepted` solo cuando no queda hueco. Si queda, es `proposed`.
