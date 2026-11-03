---
title: "Lição 8: Crie e mescle o PR do recurso"
description: "Revise os filtros, as instruções, a atualização da skill, o perfil de QA e os testes; depois crie um PR e use o Agent Merge."
authors:
  - geektrainer
lastUpdated: 2026-09-18
---

A implementação dos filtros, as atualizações das instruções, a atualização da skill, o perfil de garantia de qualidade (QA) e os testes estão salvos em uma única branch. Agora você vai revisar tudo em conjunto e abrir um pull request. Você mesmo mesclou o pull request (PR) da avaliação com estrelas; desta vez, permitirá que o **Agent Merge** gerencie o processo.

> [!NOTE]
> Normalmente, dividiríamos o recurso, as atualizações das instruções, a skill e o agente de QA em vários PRs. Para agilizar o workshop, você manteve todo o fluxo de filtros e qualidade em uma conversa e uma branch, reunindo o trabalho em um único PR.

Nesta lição, você vai:

- aprender o que é o Agent Merge e como ele automatiza o ciclo de vida do merge.
- inspecionar todas as alterações do recurso e as evidências de verificação.
- criar o PR dos filtros.
- habilitar o Agent Merge somente depois da revisão e confirmar que o PR foi mesclado.

## Cenário

Durante o fluxo de implementação dos filtros, você usou o Copilot para planejar, implementar e verificar um recurso. Agora a Tailspin Toys quer automatizar o trabalho restante do PR, mantendo o desenvolvedor responsável por autorizar o merge.

## Conheça o Agent Merge

O **Agent Merge** automatiza o trabalho restante necessário para integrar um pull request. Quando você o habilita, o Copilot resolve o que está bloqueando o PR: corrige verificações de integração contínua (CI) com falha, responde aos comentários de revisão e faz rebase quando necessário. Em seguida, habilita o merge automático do GitHub se o repositório permitir.

Até agora, você selecionou **Merge pull request** manualmente. O Agent Merge pode assumir essa responsabilidade. Revise o trabalho e confirme que ele está pronto antes de habilitar o Agent Merge.

## Use o Agent Merge para gerenciar o PR

Com todo o código criado, vamos revisar as alterações, criar o PR e deixar o Agent Merge gerenciar o restante do processo.

1. Volte ao Codespace.
2. Abra a caixa do agente digitando `/agent`.
3. Selecione **Default** na lista de opções e pressione <kbd>Enter</kbd>.
4. Crie um novo PR com o comando `/pr create`.
5. Ative o Agent Merge com `/pr agentmerge`.
6. O Copilot monitorará a integração contínua do PR e fará o merge quando tudo passar.
7. Confirme se o Copilot exibe uma mensagem semelhante a “PR #14 was squash-merged successfully.”

> [!IMPORTANT]
> O Agent Merge não ignora aprovações obrigatórias, proteção de branch, filas de merge, configurações do repositório ou permissões ausentes. Se ele for bloqueado, leia o motivo e faça manualmente o merge revisado quando o repositório permitir.

## Resumo e próximos passos

Você automatizou várias partes do processo de desenvolvimento: geração, teste e validação de código e, agora, o processo do pull request. Você:

- aprendeu o que é o Agent Merge e como ele automatiza o ciclo de vida do merge.
- inspecionou todas as alterações do recurso e as evidências de verificação.
- criou o PR dos filtros.
- habilitou o Agent Merge somente depois da revisão e confirmou que o PR foi mesclado.

Em seguida, você vai [explorar outros comandos de barra úteis do Copilot CLI][next-lesson] para contexto, modelos, compartilhamento e delegação opcional para a nuvem.

## Recursos

- [Gerenciar pull requests com o Copilot CLI][manage-prs]
- [Referência de comandos do Copilot CLI][cli-reference]

[previous-lesson]: ../7-qa-agent/
[next-lesson]: ../9-cli-power-tools/
[manage-prs]: https://docs.github.com/copilot/how-tos/copilot-cli/use-copilot-cli/manage-pull-requests
[cli-reference]: https://docs.github.com/copilot/reference/copilot-cli-reference/cli-command-reference
