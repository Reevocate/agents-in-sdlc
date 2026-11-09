---
title: "Lição 12 - Publique o site com o GitHub Pages"
description: "Use o aplicativo GitHub Copilot para configurar um workflow do Pages, revisar o pull request e verificar o Space Quiz publicado."
authors:
  - jamesmontemagno
lastUpdated: 2026-10-12
---

Publique o Space Quiz no GitHub Pages para disponibilizá-lo ao público. O Copilot pode preparar o workflow e orientar a implantação, mas você continua responsável por revisar as alterações e confirmar que o site está no ar.

Nesta lição, você vai:

- Pedir ao Copilot para configurar uma implantação no GitHub Pages.
- Revisar o workflow e o pull request antes de fazer o merge.
- Acompanhar a implantação e verificar o site publicado.

## Cenário

O Space Quiz já está em um repositório do GitHub, mas ainda falta uma maneira simples de experimentá-lo. Publicar o site de arquivo único com o GitHub Pages o disponibiliza em uma URL pública sem adicionar um servidor ou uma dependência de runtime.

## Peça ao Copilot para publicar o site

Na sessão do aplicativo Copilot para `space-quiz`, envie este prompt:

```plaintext
Habilite o GitHub Pages para este repositório. Crie um workflow do GitHub Actions que compile o site, se necessário, e o publique no GitHub Pages. Se ainda não houver um README, adicione um que descreva o aplicativo e como executá-lo localmente. Crie um pull request com essas alterações e faça o merge depois que as verificações obrigatórias forem aprovadas. Acompanhe a implantação até que ela seja concluída com sucesso e, em seguida, informe a URL final do site publicado. Se você não tiver permissão para habilitar o Pages ou fazer o merge, diga exatamente o que preciso aprovar ou fazer; não informe que a tarefa foi concluída até que o site esteja no ar.
```

![Diagrama de três etapas: um pull request de space-quiz com merge concluído; uma execução bem-sucedida de GitHub Actions Deploy website com as etapas Build website, Upload artifact e Deploy to Pages; e o Space Quiz publicado em yourname.github.io/space-quiz/.](../../../_images/first-steps-app-pages-deploy.svg)

> [!WARNING]
> Este prompt pede ao agente que crie e faça o merge de um pull request e altere as configurações do Pages do repositório. Antes de continuar, revise o diff, as permissões de implantação e qualquer solicitação de aprovação do GitHub.

## Revise o workflow e verifique a implantação

1. Confirme que o README só foi adicionado se o repositório ainda não tinha um.
2. Revise as alterações do pull request, incluindo as etapas de build e implantação do workflow.
3. Faça o merge somente depois que as verificações obrigatórias do pull request forem aprovadas.
4. Acompanhe a execução de implantação do GitHub Actions até que ela seja concluída com sucesso.
5. Abra a URL informada e confirme que o Space Quiz é carregado.

Se o agente não puder habilitar o Pages ou fazer o merge do pull request, siga as instruções específicas fornecidas. Não considere a tarefa concluída até que a implantação seja bem-sucedida e o site esteja no ar.

## Resumo e próximos passos

O Space Quiz agora está disponível em um site publicado, e você verificou a implantação em vez de confiar apenas no relato do agente. Continue para [Lição 13: Revisão e próximos passos][next-lesson].

[next-lesson]: ../13-review/
