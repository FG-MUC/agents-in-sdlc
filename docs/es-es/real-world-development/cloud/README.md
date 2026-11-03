---
slug: es-es/real-world-development/cloud
title: "Agente en la nube de GitHub Copilot"
authors:
  - geektrainer
lastUpdated: 2026-06-30
---

El [**agente en la nube de GitHub Copilot**](https://docs.github.com/copilot/concepts/agents/cloud-agent/about-cloud-agent) permite que GitHub Copilot trabaje de forma asíncrona en la nube. Asignas trabajo en GitHub y el agente en la nube lo recoge en segundo plano: explora el repositorio, realiza cambios y abre una solicitud de incorporación de cambios mientras tú te ocupas de otras tareas.

En estos ejercicios añadirás instrucciones personalizadas que seguirá el agente en la nube y, después, le asignarás una incidencia de GitHub para que implemente el trabajo. Revisarás y utilizarás agentes personalizados para definir su enfoque, supervisarás y dirigirás las sesiones desde el panel de agentes y terminarás revisando sus solicitudes de incorporación de cambios e iterando sobre los resultados.

## Ejercicios

| Ejercicio | Tema | Descripción |
|----------|-------|-------------|
| [0. Requisitos previos][ex0] | Configuración | Crea tu repositorio y Codespace |
| [1. Instrucciones personalizadas][ex1] | Contexto | Añade instrucciones personalizadas para el agente en la nube |
| [2. Agente en la nube][ex2] | Agente asíncrono | Asigna incidencias al agente en la nube de Copilot |
| [3. Agentes personalizados][ex3] | Agentes especializados | Revisa y utiliza agentes personalizados |
| [4. Administración de agentes][ex4] | Supervisión | Supervisa y dirige las sesiones de los agentes |
| [5. Iteración][ex5] | Revisión | Revisa solicitudes de incorporación de cambios, itera sobre el trabajo de Copilot y elige los siguientes pasos |

## Requisitos previos

Antes de participar en este taller, asegúrate de tener lo siguiente:

- [ ] Una cuenta de GitHub con un plan activo **Copilot Student, Pro, Pro+, Business o Enterprise**
- [ ] El agente en la nube de Copilot habilitado para tu cuenta u organización

> [!TIP]
> ¿No tienes un plan de pago? Los estudiantes cuya condición se haya verificado pueden obtener GitHub Copilot gratis mediante [GitHub Education][callout-student-plan-education]. El plan **Copilot Student** incluye el agente, el protocolo de contexto del modelo (MCP), la revisión de código y las funciones de Copilot CLI que se utilizan en este taller, por lo que puedes completar todos los entornos con él.

[callout-student-plan-education]: https://github.com/education/students

> [!NOTE]
> El agente en la nube está disponible en **Copilot Student, Pro, Pro+, Business y Enterprise**; en todos los planes excepto Copilot Free. En Copilot Business o Enterprise, un administrador debe habilitarlo para la organización.

> [!NOTE]
> Este entorno no incluye MCP. Para explorar el uso de servidores MCP con Copilot, consulta el [entorno de CLI][cli] o el [entorno de VS Code][vscode].

## Empieza

**[Empieza con el ejercicio 0: Requisitos previos →][ex0]**

[ex0]: 0-prerequisites/
[ex1]: 1-custom-instructions/
[ex2]: 2-cloud-agent/
[ex3]: 3-custom-agents/
[ex4]: 4-managing-agents/
[ex5]: 5-iterating/
[cli]: ../cli/
[vscode]: ../vscode/
