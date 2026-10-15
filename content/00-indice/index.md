---
title: 00 · Como usar este mapa
tags: [indice]
---

**Resumo:** convenções do site: como as notas são escritas, o que significam as marcações e como o conteúdo cresce.

## Estrutura de uma nota

Toda nota segue o mesmo roteiro: resumo, o que é, por que importa no projeto, como aplicar, norma relacionada, exemplo prático, erros comuns e links para notas vizinhas. O modelo fica em `templates/modelo-nota.md` (usado no Obsidian, não aparece no site).

## Legenda

| Marcação           | Significado                                                                 |
| ------------------ | --------------------------------------------------------------------------- |
| `status: rascunho` | Nota escrita, ainda não revisada contra a fonte                             |
| `status: revisado` | Conferida contra o livro ou a norma                                         |
| ⚠️ verificar       | Valor ou requisito de norma que precisa ser conferido no documento original |
| `- [ ]` / `- [x]`  | Nos índices de módulo: tópico pendente / nota já escrita                    |

## Regras de conteúdo

- Resumos com palavras próprias. Nenhum trecho de livro ou norma é copiado; a fonte é sempre citada (livro e capítulo, ou número da norma).
- Fórmulas em LaTeX, unidades no SI.
- Sempre que possível, um exemplo ligado à indústria: moenda, caldeiraria, transmissão de potência.

## Exercícios e revisões

- **Exercícios resolvidos** aparecem dentro das notas, numa caixa de pergunta. A resolução fica escondida: clique em **Resolução** para abrir.
- Cada índice de módulo termina com uma **revisão rápida** de 10 perguntas, no mesmo formato.

## Rotina de estudo e de atualização

O site cresce a partir do estudo de livros, normas e da prática. A rotina sugerida:

1. **Estudar** um capítulo ou tema (livro, norma, catálogo, aula).
2. **Anotar** os pontos principais, dúvidas e exemplos vistos na prática, no Obsidian ou em papel.
3. **Transformar em notas:** cada conceito vira uma nota no modelo padrão, com resumo, aplicação, norma, exemplo, erros comuns e links. Notas existentes são complementadas em vez de duplicadas.
4. **Ligar:** acrescentar links para notas relacionadas e atualizar o índice do módulo (o tópico vira `- [x]` com link).
5. **Revisar:** conferir os itens marcados com ⚠️ na fonte original e mudar o `status` da nota de `rascunho` para `revisado`.
6. **Publicar:** sincronizar com o GitHub (o site se atualiza sozinho em 1 a 2 minutos).
7. **Autoavaliar:** refazer as revisões rápidas dos módulos periodicamente.

## Situação do conteúdo

Todos os módulos têm uma primeira versão completa (status `rascunho`). As próximas etapas são revisar cada nota contra as fontes, conferir os itens ⚠️ e acrescentar figuras e novos tópicos.

Voltar ao [[index|Início]].
