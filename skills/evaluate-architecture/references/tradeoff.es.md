<p align="right">Idioma:&emsp;<a href="tradeoff.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Arquitecto de software](../../../README.es.md) / [Evaluar la arquitectura](../SKILL.es.md)

# Opciones y tradeoff

Fuente: ISO/IEC/IEEE 42030:2019. El tipo de archivo es `tradeoff`.

## Qué fija

Las opciones en juego y lo que cuesta cada una. Al menos dos opciones. Un diagrama Mermaid: una caja por opción. Sin flecha de elección salvo que la decisión ya esté nombrada.

## Cómo hacerlo

1. Un párrafo corto por opción, en lenguaje claro: qué cambia y el coste que nombró la persona o una fuente.
2. Menos de dos opciones: escribe el archivo como `proposed` y nombra el hueco.
3. No elijas al ganador aquí. Eso es `/arch-evaluation-adr`.

## Prompt

`/arch-evaluation-tradeoff` Las opciones para #preocupación son #opciones.

## Done

- El archivo usa los campos de la plantilla. Un hueco es una línea, no una suposición.
- Una sección explicada tiene unas frases claras y un diagrama Mermaid. El diagrama no se llama UML.
- El estado es `accepted` solo cuando no queda hueco. Si queda, es `proposed`.
