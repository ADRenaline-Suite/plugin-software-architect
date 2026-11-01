<p align="right">Idioma:&emsp;<a href="4plus1.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Arquitecto de software](../../../README.es.md) / [Describir la arquitectura](../SKILL.es.md)

# Documento 4+1

Fuente: Philippe Kruchten, IEEE Software, 1995. El tipo de archivo es `4plus1`.

## Qué fija

Un documento que se puede seguir, partido en cinco secciones: Lógica, Desarrollo, Proceso, Física, Escenarios. No espera al arc42 ni a la evaluación.

## Cómo hacerlo

1. Lee la carpeta que la persona nombró. Usa los nombres que estén ahí.
2. Escribe las cinco secciones en ese orden. Cada una de las cuatro primeras tiene dos o tres frases y un diagrama Mermaid, como dice el skill.
3. Proceso pide además a `plugin-uml-diagrams` una secuencia UML 2 y enlaza el `.svg`. Física pide un despliegue UML 2 y enlaza el `.svg`.
4. Escenarios cita los casos de uso que la persona pegó o un archivo accepted de `plugin-project-manager`. No redacta el caso de uso. Si no hay ninguno, esa sección es el hueco de cuatro partes de este skill: qué falta, cómo llenarlo, la plantilla y un ejemplo. El ejemplo no es un caso de uso citado. El archivo se queda `proposed`. La respuesta repite esas cuatro partes.
5. Una sección sin hechos conserva el título. Si ese hueco pide a la persona un hecho, usa el hueco de cuatro partes. Si no, una línea de hueco. Las otras se escriben.

## Plantilla

El archivo lleva el título y después cinco encabezados en este orden: Vista lógica, Vista de desarrollo, Vista de proceso, Vista física, Escenarios. Bajo cada una de las cuatro primeras: dos o tres frases, un diagrama Mermaid y una frase que dice qué muestra la figura. Bajo Escenarios: los casos de uso citados, o el hueco de cuatro partes.

## Prompt

`/arch-4plus1` Lee la carpeta #carpeta. Escribe el 4+1 de #sistema en #idioma.

## Done

- El archivo usa los campos de la plantilla. Un hueco que pide a la persona un hecho es el hueco de cuatro partes, con un ejemplo aparte de la plantilla. El ejemplo no es un hecho. Cualquier otro hueco es una línea, no una suposición.
- Una sección explicada tiene unas frases claras y un diagrama Mermaid. El diagrama no se llama UML.
- El estado es `accepted` solo cuando no queda hueco. Si queda, es `proposed`.
