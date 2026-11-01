<p align="right">Idioma:&emsp;<a href="arc42.md" style="vertical-align:middle"><img alt="English" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-en-off.svg" align="middle" style="vertical-align:middle"></a> <img alt="Español" src="https://raw.githubusercontent.com/ADRenaline-Suite/.github/main/profile/lang-es-on.svg" align="middle" style="vertical-align:middle"></p>

[🏠 Arquitecto de software](../../../README.es.md) / [Describir la arquitectura](../SKILL.es.md)

# Manual arc42

Fuente: plantilla arc42 9.1, inglés, octubre de 2026. ISO/IEC/IEEE 42010:2022. El tipo de archivo es `arc42`.

## Qué fija

El manual de arquitectura en doce secciones. Quien lee recibe un párrafo corto por sección. Las secciones que son vistas citan el 4+1 y muestran un diagrama explicativo solo cuando esa vista no está ya en un 4+1 accepted. Si está, la sección enlaza ese archivo y no dibuja un segundo diagrama.

## Cómo hacerlo

1. Secciones, en orden: metas, restricciones y estrategia; contexto; bloques; ejecución; despliegue; conceptos; decisiones; calidad; riesgos; glosario. Bloques cita la lógica y el desarrollo de `/arch-4plus1`. Ejecución cita el proceso. Despliegue cita la física.
2. Decisiones lista los ADR accepted de este plugin. Calidad lista los escenarios de calidad accepted. Si falta una cita, esa sección es el hueco de cuatro partes de este skill y nombra el command: `/arch-evaluation-adr` o `/arch-evaluation-scenario`. El ejemplo no es una cita. La respuesta repite esas cuatro partes.
3. Contexto tiene su propio diagrama: el sistema en el centro y alrededor los nombres externos que dio una fuente.
4. El archivo se queda `proposed` mientras falten la entidad, los interesados, las preocupaciones o los hechos del contexto.
5. No copies una sección del 4+1. Enlázala.

## Prompt

`/arch-arc42` Lee la carpeta #carpeta. Escribe el manual arc42 de #sistema en #idioma.

## Done

- El archivo usa los campos de la plantilla. Un hueco que pide a la persona un hecho es el hueco de cuatro partes, con un ejemplo aparte de la plantilla. El ejemplo no es un hecho. Cualquier otro hueco es una línea, no una suposición.
- Una sección explicada tiene unas frases claras y un diagrama Mermaid. El diagrama no se llama UML.
- El estado es `accepted` solo cuando no queda hueco. Si queda, es `proposed`.

- Las doce secciones están. Una cita que la persona debe aportar es el hueco de cuatro partes, no una vista reescrita. El ejemplo no es una cita.
