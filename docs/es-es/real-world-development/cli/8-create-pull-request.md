---
title: "Lección 8: Crea y fusiona la solicitud de incorporación de cambios"
description: "Revisa la funcionalidad de filtrado, las instrucciones, la aptitud, el perfil de QA y las pruebas; después crea una solicitud de incorporación de cambios y usa Agent Merge."
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

La implementación del filtrado, las actualizaciones de instrucciones, la aptitud, el perfil de control de calidad (QA) y las pruebas están guardadas en una misma rama. Ahora revisarás todo junto y abrirás una solicitud de incorporación de cambios. Fusionaste tú mismo la solicitud de incorporación de cambios (PR) de la valoración con estrellas; esta vez permitirás que **Agent Merge** gestione el proceso.

> [!NOTE]
> Normalmente separaríamos la funcionalidad, las instrucciones, la aptitud y el agente de QA en varias PR. Para agilizar el taller, has mantenido todo el flujo de filtrado y calidad en una conversación y una rama, y lo incluirás en una sola PR.

En esta lección, harás lo siguiente:

- aprenderás qué es Agent Merge y cómo automatiza el ciclo de vida de una PR.
- inspeccionarás todos los cambios de la funcionalidad y las pruebas de verificación.
- crearás la PR del filtrado.
- habilitarás Agent Merge solo después de revisar los cambios y confirmar que la PR se ha fusionado.

## Escenario

Durante el flujo de trabajo de filtrado, has usado Copilot para planificar, implementar y verificar una funcionalidad. Tailspin Toys ahora quiere automatizar el trabajo restante de la PR sin quitar al desarrollador el control de autorización de la fusión.

## Presentación de Agent Merge

**Agent Merge** automatiza el trabajo restante necesario para integrar una solicitud de incorporación de cambios. Al habilitarlo, Copilot resuelve los bloqueos de la PR —corrige comprobaciones de integración continua (CI) fallidas, responde a comentarios de revisión y vuelve a aplicar la base cuando hace falta— y, después, habilita la fusión automática de GitHub si el repositorio lo permite.

Hasta ahora has seleccionado tú **Merge pull request**. Agent Merge puede encargarse de esa responsabilidad. Revisa el trabajo y confirma que está listo antes de habilitar Agent Merge.

## Usa Agent Merge para gestionar la PR

Con todo el código creado, vamos a revisarlo, crear la PR y permitir que Agent Merge gestione el resto.

1. Vuelve a tu Codespace.
2. Abre el cuadro de agentes con `/agent`.
3. Selecciona **Default** en la lista y pulsa <kbd>Enter</kbd>.
4. Crea una PR con el comando `/pr create`.
5. Activa Agent Merge con `/pr agentmerge`.
6. Copilot supervisará el proceso de integración continua de la PR. Cuando todo se supere, la fusionará.
7. Confirma que aparece un mensaje de Copilot similar a «PR #14 was squash-merged successfully».

> [!IMPORTANT]
> Agent Merge no omite las aprobaciones obligatorias, la protección de ramas, las colas de fusión, la configuración del repositorio ni los permisos que falten. Si se bloquea, lee el motivo y, cuando el repositorio lo permita, realiza manualmente la fusión revisada.

## Resumen y siguientes pasos

Has automatizado varias partes del proceso de desarrollo: generar código, probarlo y validarlo, y ahora gestionar la solicitud de incorporación de cambios. En concreto:

- aprendiste qué es Agent Merge y cómo automatiza el ciclo de vida de la PR.
- inspeccionaste todos los cambios de la funcionalidad y las pruebas de verificación.
- creaste la PR del filtrado.
- habilitaste Agent Merge solo después de revisar los cambios y confirmaste que la PR se fusionó.

A continuación, [explorarás otros comandos de barra útiles de Copilot CLI][next-lesson] para administrar el contexto y los modelos, compartir sesiones y delegar trabajo en la nube de forma opcional.

## Recursos

- [Administrar solicitudes de incorporación de cambios con Copilot CLI][manage-prs]
- [Referencia de comandos de Copilot CLI][cli-reference]

[previous-lesson]: ../7-qa-agent/
[next-lesson]: ../9-cli-power-tools/
[manage-prs]: https://docs.github.com/copilot/how-tos/copilot-cli/use-copilot-cli/manage-pull-requests
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
