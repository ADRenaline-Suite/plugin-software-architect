<p align="right">Idioma:&emsp;<a href="evaluation.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Arquitecto de software](../../../README.es.md) / [Evaluar la arquitectura](../SKILL.es.md)

# Evaluación

Fuente: ISO/IEC/IEEE 42030:2019. El tipo de archivo es `evaluation`.

## Qué fija

Los tres pasos en un archivo: el escenario de seis partes, las opciones y el tradeoff con su diagrama, y un enlace al ADR cuando se eligió una decisión. Si en este turno se eligió, escribe también el ADR como su propio `<NNN>-adr-<tema>.md`.

## Cómo hacerlo

1. Escribe la sección del escenario y la del tradeoff. El diagrama sigue al skill.
2. Si no hay opción elegida, la sección de decisión es el hueco `Aún no hay decisión. Se registra con /arch-evaluation-adr.` y el archivo se queda `proposed`.
3. Si hay opción elegida, escribe también el archivo ADR y enlázalo. No pegues aquí el cuerpo del ADR.

## Prompt

`/arch-evaluation` La preocupación es #preocupación. Las opciones son #opciones.

## Done

- El archivo usa los campos de la plantilla. Un hueco es una línea, no una suposición.
- Una sección explicada tiene unas frases claras y un diagrama Mermaid. El diagrama no se llama UML.
- El estado es `accepted` solo cuando no queda hueco. Si queda, es `proposed`.
