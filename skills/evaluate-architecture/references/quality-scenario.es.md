<p align="right">Idioma:&emsp;<a href="quality-scenario.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Arquitecto de software](../../../README.es.md) / [Evaluar la arquitectura](../SKILL.es.md)

# Escenario de calidad

Fuente: ATAM y el Quality Attribute Workshop. ISO/IEC 25010:2023. El tipo de archivo es `quality-scenario`. No es `/arch-4plus1-scenarios`.

## Qué fija

Una preocupación escrita para poder comprobarla: origen del estímulo, estímulo, entorno, artefacto, respuesta y medida. El nombre de calidad es uno de los nueve vigentes.

## Cómo hacerlo

1. Llena las seis partes con lo que la persona dijo o con un archivo que se leyó. Una parte que no dio se queda en hueco y el archivo se queda `proposed`.
2. Este archivo no lleva diagrama. El diagrama de opciones es del tradeoff.

## Plantilla

```markdown
# <título>

- Característica: <un nombre de ISO/IEC 25010:2023>
- Origen del estímulo:
- Estímulo:
- Entorno:
- Artefacto:
- Respuesta:
- Medida de la respuesta:
```

## Prompt

`/arch-evaluation-scenario` La preocupación es #preocupación. La característica es #característica.

## Done

- El archivo usa los campos de la plantilla. Un hueco es una línea, no una suposición.
- Una sección explicada tiene unas frases claras y un diagrama Mermaid. El diagrama no se llama UML.
- El estado es `accepted` solo cuando no queda hueco. Si queda, es `proposed`.

- Las seis partes están o quedan marcadas como hueco.
