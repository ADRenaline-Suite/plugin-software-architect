<p align="right">Idioma:&emsp;<a href="scenarios.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Arquitecto de software](../../../README.es.md) / [Describir la arquitectura](../SKILL.es.md)

# Escenarios que atan las vistas

Fuente: Philippe Kruchten, IEEE Software, 1995, el «+1». El tipo de archivo es `scenarios`. No es el escenario de calidad. Ese es `/arch-evaluation-scenario`.

## Qué fija

Qué casos de uso recorren las cuatro vistas. Los cita. No los redacta.

## Cómo hacerlo

1. Cita un caso de uso que la persona pegó, o un archivo accepted de `plugin-project-manager`.
2. Por cada caso de uso, una frase dice qué vistas recorre.
3. Un diagrama Mermaid une cada caso de uso con las vistas que toca. Las cajas son los nombres de caso de uso que se citaron.
4. Si no se cita ninguno, no escribas archivo. El chat usa el hueco de cuatro partes de este skill. Si ya existe un 4+1 de este sistema, pon ese mismo hueco en su sección Escenarios y deja ese archivo `proposed`. El prompt está abajo. El ejemplo rellena `#casos-de-uso` con nombres de muestra y dice qué vistas recorre cada uno. Marca el ejemplo como muestra. No guardes esos nombres como casos de uso citados.

## Prompt

`/arch-4plus1-scenarios` Estos casos de uso atan las vistas de #sistema: #casos-de-uso.

## Done

- El archivo usa los campos de la plantilla. Si no se cita ningún caso de uso, no se escribe archivo de escenarios, y la respuesta es el hueco de cuatro partes con un ejemplo aparte de la plantilla. El ejemplo no es un caso de uso citado. Cualquier otro hueco es una línea, no una suposición.
- Una sección explicada tiene unas frases claras y un diagrama Mermaid. El diagrama no se llama UML.
- El estado es `accepted` solo cuando no queda hueco. Si queda, es `proposed`.

- Aquí no se redactó el texto del caso de uso.
