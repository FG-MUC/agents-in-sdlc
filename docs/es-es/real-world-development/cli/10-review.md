---
title: "Lección 10: Resumen y siguientes pasos"
description: "Repasa el flujo de trabajo de Copilot CLI, las dos solicitudes de incorporación de cambios, las personalizaciones reutilizables y otros recursos."
authors:
  - geektrainer
lastUpdated: 2026-09-29
---

Has usado GitHub Copilot CLI en un flujo de trabajo continuo de Tailspin Toys. Has:

- preparado un Codespace, instalado Copilot CLI, explorado el proyecto y encontrado la incidencia de filtrado preparada.
- añadido valoraciones con estrellas, revisado el resultado en un navegador reenviado y fusionado manualmente tu primera solicitud de incorporación de cambios (PR).
- partido de la incidencia de filtrado, definido el enfoque en modo Plan, implementado en modo Autopilot y revisado en modo Interactive.
- guiado al agente con instrucciones personalizadas, adaptado la aptitud `quality-checks` existente y la usado para ejecutar pruebas unitarias, lint y comprobaciones de tipos.
- añadido el servidor Playwright del protocolo de contexto del modelo (MCP) y lo has usado para explorar el filtrado en un navegador real.
- creado y seleccionado un agente personalizado de control de calidad (QA) para evaluar los requisitos, la cobertura, los resultados de la aptitud y las pruebas en el navegador.
- revisado todo el cambio de filtrado y autorizado Agent Merge para la PR correspondiente.
- explorado comandos de barra para el contexto, los modelos, el uso compartido y la delegación opcional en la nube.

## Lo que has publicado

El taller incluye dos hitos de PR, cada uno en su propia rama creada desde `main` actualizada:

1. **Valoraciones con estrellas:** mostrar la valoración existente `starRating` y un estado explícito para los juegos sin valorar en las tarjetas.
2. **Flujo de filtrado y calidad:** implementar el filtrado, actualizar las instrucciones y aplicarlas a la funcionalidad, personalizar el informe de la aptitud `quality-checks`, crear un perfil de QA e incluir las pruebas asociadas.

Desde la planificación del filtrado hasta la creación de su PR, has usado la misma conversación y rama. Agrupamos ese trabajo en una PR para agilizar el taller.

## Distintos tipos de verificación

Has comprobado el código de varias formas: con pruebas automatizadas, examinando el sitio en el navegador y dejando que Copilot lo explorase mediante MCP. La aptitud `quality-checks` ejecutó las pruebas unitarias, lint y las comprobaciones de tipos, y generó un informe con el formato nuevo. Antes de crear la PR, QA reunió esos resultados con la revisión de los requisitos y de la cobertura de pruebas.

Las pruebas nuevas deben cubrir carencias reales; una ejecución de QA que no necesite pruebas nuevas también puede ser correcta. Revisa el código y las pruebas antes de autorizar la fusión y vuelve a recopilar las pruebas afectadas después de hacer cambios.

## Prácticas recomendadas

El contexto y las herramientas que proporcionas influyen en el trabajo de Copilot. En este taller, actualizaste instrucciones, personalizaste una aptitud, creaste un perfil de QA y configuraste un servidor MCP. Reutiliza estas personalizaciones en otras conversaciones y adáptalas a las necesidades del equipo. Las instrucciones establecen estándares, las aptitudes describen tareas repetibles, los agentes personalizados definen funciones especializadas y los servidores MCP conectan herramientas externas. Revisa los cambios y los resultados de las herramientas, no solo el resumen del agente.

Elige el **modo y el modelo** según la tarea. Usa **Plan** para pensar el enfoque antes de implementarlo, **Interactive** para mantener el control en los cambios específicos y **Autopilot** para tareas bien delimitadas. Elige un modelo más rápido para ediciones rutinarias y uno más capaz para tareas complejas.

El contexto importa tanto como la infraestructura. Describir con claridad *qué* quieres crear, *por qué* y *cómo* influye de forma importante en el resultado.

## Más cosas que explorar

Has completado el flujo de trabajo principal. Estas funciones de CLI también pueden resultarte útiles:

- `/review` para pedir al agente de revisión de código que analice los cambios.
- `/rubber-duck` para explicar un problema y obtener otra perspectiva.
- `/fleet` para coordinar subtareas independientes en paralelo.
- `/worktree` para aislar una tarea.
- `/delegate` para enviar una tarea al agente en la nube de Copilot.

## Siguientes pasos

La mejor forma de mejorar con cualquier herramienta es seguir utilizándola. Úsala con código de producción, proyectos personales o esa pequeña aplicación que llevas años pensando en crear. Comparte lo que aprendas con el equipo y aprovecha lo que hayan aprendido los demás. Y, como siempre, consulta la documentación.

Si quieres ampliar Tailspin Toys desde el terminal, continúa con la serie opcional [Foundry Backer Concierge][foundry]. Para comparar otros entornos, explora el [taller de VS Code][vscode], el [taller de la aplicación GitHub Copilot][app] o el [taller del agente en la nube de Copilot][cloud].

## Recursos

- [Acerca de GitHub Copilot CLI][about-cli]
- [Referencia de comandos de Copilot CLI][cli-reference]
- [Personalizar Copilot CLI][customize-cli]
- [Administrar solicitudes de incorporación de cambios con Copilot CLI][manage-prs]

[previous-lesson]: ../9-cli-power-tools/
[foundry]: ../8-foundry-agent/
[vscode]: ../../vscode/
[app]: ../../app/
[cloud]: ../../cloud/
[about-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
[customize-cli]: https://docs.github.com/copilot/how-tos/copilot-cli/customize-copilot
[manage-prs]: https://docs.github.com/copilot/how-tos/copilot-cli/use-copilot-cli/manage-pull-requests
