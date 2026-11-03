---
title: "Lição 10: Retrospectiva e próximos passos"
description: "Recapitule o fluxo do Copilot CLI, os dois pull requests, as personalizações reutilizáveis e outros recursos."
authors:
  - geektrainer
lastUpdated: 2026-09-29
---

Você usou o GitHub Copilot CLI em um fluxo contínuo de trabalho na Tailspin Toys. Você:

- preparou um Codespace, instalou o Copilot CLI, explorou o projeto e encontrou a issue de filtros já criada.
- adicionou avaliações com estrelas, revisou o resultado no navegador encaminhado e mesclou manualmente seu primeiro pull request (PR).
- começou pela issue de filtros, definiu a abordagem no modo Plan, implementou no modo Autopilot e revisou no modo Interactive.
- orientou o agente com instruções personalizadas, personalizou a skill `quality-checks` existente e usou-a para executar testes unitários, lint e verificações de tipos.
- adicionou o servidor Playwright do Model Context Protocol (MCP) e usou-o para explorar os filtros em um navegador real.
- criou e selecionou um agente personalizado de garantia de qualidade (QA) para avaliar requisitos, cobertura, resultados da skill e evidências do navegador.
- revisou toda a alteração dos filtros e autorizou o Agent Merge para o PR.
- explorou comandos de barra para contexto, modelos, compartilhamento e delegação opcional para a nuvem.

## O que você entregou

O workshop inclui dois marcos de PR, cada um em sua própria branch criada a partir da `main` atualizada:

1. **Avaliações com estrelas:** exiba o `starRating` existente e um estado explícito para itens sem avaliação nos cards.
2. **Fluxo de filtros e qualidade:** implemente os filtros, atualize as instruções e aplique-as ao recurso, personalize o relatório da skill `quality-checks`, crie um perfil de QA e inclua os testes relacionados.

Desde o planejamento dos filtros até a abertura do PR, você usou a mesma conversa e branch. Reunimos esse trabalho em um único PR para agilizar o workshop.

## Diferentes tipos de verificação

Você verificou o código de várias formas: com testes automatizados, examinando o site no navegador e usando o Copilot para explorar a interface pelo MCP. A skill `quality-checks` executou testes unitários, lint e verificações de tipos e apresentou os resultados no novo formato. Antes do PR, o QA reuniu esses resultados com a revisão dos requisitos e da cobertura de testes.

Os testes adicionados devem preencher lacunas reais; uma execução de QA que não precisa de novos testes também pode estar correta. Revise o código e as evidências antes de autorizar o merge e atualize as evidências afetadas depois das alterações.

## Práticas recomendadas

O contexto e as ferramentas fornecidos orientam o trabalho do Copilot. Neste workshop, você atualizou instruções, personalizou uma skill, criou um perfil de QA e configurou um servidor MCP. Reutilize essas personalizações entre conversas e ajuste-as conforme as necessidades da equipe. Instruções definem padrões, skills descrevem tarefas repetíveis, agentes personalizados definem funções especializadas e servidores MCP conectam ferramentas externas. Revise as alterações e os resultados das ferramentas, não apenas o resumo do agente.

Escolha o **modo e o modelo** de acordo com a tarefa. Use **Plan** para definir uma abordagem antes de implementar, **Interactive** para acompanhar alterações focadas e **Autopilot** para tarefas bem delimitadas. Escolha um modelo mais rápido para edições rotineiras e outro mais capaz para trabalhos complexos.

O contexto importa tanto quanto a infraestrutura. Descrever com clareza *o que* você quer criar, *por que* e *como* influencia significativamente o resultado.

## Mais recursos para explorar

Você concluiu o fluxo principal. Outras funcionalidades do CLI que vale a pena conhecer:

- `/review` para pedir ao agente de revisão de código que analise as alterações.
- `/rubber-duck` para explicar um problema e obter outra perspectiva.
- `/fleet` para coordenar subtarefas independentes em paralelo.
- `/worktree` para isolar uma tarefa.
- `/delegate` para enviar uma tarefa ao agente de nuvem do Copilot.

## Próximos passos

A melhor forma de melhorar com qualquer ferramenta é continuar usando-a. Use-a em código de produção, projetos pessoais ou naquele pequeno aplicativo que você pensa em criar há anos. Compartilhe o que aprendeu com sua equipe e aprenda com as experiências dos colegas. E, como sempre, explore a documentação.

Se quiser ampliar a Tailspin Toys pelo terminal, continue com a série opcional [Foundry Backer Concierge][foundry]. Para comparar outros ambientes, explore o [workshop do VS Code][vscode], o [workshop do aplicativo GitHub Copilot][app] ou o [workshop do agente de nuvem do Copilot][cloud].

## Recursos

- [Sobre o GitHub Copilot CLI][about-cli]
- [Referência de comandos do Copilot CLI][cli-reference]
- [Personalizar o Copilot CLI][customize-cli]
- [Gerenciar pull requests com o Copilot CLI][manage-prs]

[previous-lesson]: ../9-cli-power-tools/
[foundry]: ../8-foundry-agent/
[vscode]: ../../vscode/
[app]: ../../app/
[cloud]: ../../cloud/
[about-cli]: https://docs.github.com/copilot/concepts/agents/about-copilot-cli
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
[customize-cli]: https://docs.github.com/copilot/how-tos/copilot-cli/customize-copilot
[manage-prs]: https://docs.github.com/copilot/how-tos/copilot-cli/use-copilot-cli/manage-pull-requests
