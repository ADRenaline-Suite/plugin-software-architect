<p align="right">Idioma:&emsp;<a href="adr.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Arquitecto de software](../../../README.es.md) / [Evaluar la arquitectura](../SKILL.es.md)

# Decisión de arquitectura

Fuente: Michael Nygard, estado, contexto, decisión y consecuencias. El tipo de archivo es `adr`.

## Qué fija

Una decisión ya tomada. No reabre el escenario.

## Cómo hacerlo

1. El estado es `accepted` cuando el texto de la decisión es el que dijo la persona. `proposed` cuando la decisión sigue siendo candidata.
2. El contexto cita el escenario de calidad y el tradeoff cuando esos archivos existen. No los copia.
3. Las consecuencias dicen qué se vuelve más fácil y qué más difícil, solo a partir de lo que se dijo o se leyó.
4. Sin caso de uso, sin modelo de amenazas, sin código.

## Plantilla

```markdown
# <NNN> — <título>

- Estado: proposed | accepted

## Contexto

## Decisión

## Consecuencias
```

## Prompt

`/arch-evaluation-adr` La decisión para #preocupación es #decisión.

## Done

- El archivo usa los campos de la plantilla. Un hueco es una línea, no una suposición.
- Una sección explicada tiene unas frases claras y un diagrama Mermaid. El diagrama no se llama UML.
- El estado es `accepted` solo cuando no queda hueco. Si queda, es `proposed`.
