# Mapa de Projeto Mecânico — instruções do projeto

Site pessoal de estudos de projeto mecânico do Gabriel (Eng. Mecânica UTFPR, estagiário na Raízen: projeto de equipamentos de moenda, padronização de componentes, layout). Publicado com Quartz v4 no GitHub Pages: https://gabriel302540.github.io/mapa-projeto-mecanico. As notas ficam em `content/`, que também é o vault do Obsidian.

O Gabriel é iniciante em Git e Node: explique em português simples o que foi feito e os comandos usados.

## Profundidade do conteúdo (pedido explícito do Gabriel)

Ao escrever notas:
- Pesquise o máximo de referências possível (livros-texto, normas, catálogos de fabricantes, materiais técnicos confiáveis) antes de escrever, e cite todas.
- Explique cada ideia de forma clara e completa, sem pular etapas de raciocínio. Prefira explicar demais a de menos.
- Inclua exemplos práticos numéricos e situações reais da indústria (moenda, caldeiraria, transmissão de potência) sempre que fizer sentido.

## Regras de conteúdo

- NÃO copie trechos de livros nem de normas ABNT/ISO. Escreva com palavras próprias e cite a fonte (livro + capítulo, ou número da norma).
- Português do Brasil, linguagem técnica mas direta.
- Fórmulas em LaTeX, unidades no SI.
- Marque com "⚠️ verificar" qualquer valor ou requisito de norma que deva ser conferido no documento original.
- Links entre notas com [[wikilinks]] (resolução "shortest", igual ao Obsidian).

## Modelo de nota

Use `content/templates/modelo-nota.md`. Frontmatter: `title`, `tags: [modulo, subtema]`, `fontes: [...]`, `status: rascunho | revisado`. Seções: Resumo, O que é, Por que importa no projeto, Como aplicar, Norma relacionada, Exemplo prático, Erros comuns, Ver também.

## Estrutura

- `content/index.md`: página inicial com o mapa dos módulos.
- `content/NN-modulo/index.md`: índice do módulo, com checklist de tópicos. Ao criar uma nota, troque `- [ ] Tópico` por `- [x] [[Nome da nota]]`.
- `content/99-referencias/`: bibliografia, lista de normas e glossário. Atualize-os ao citar novas fontes ou termos.
- `content/templates/` e `content/private/` não são publicados.
- Imagens em `content/anexos/`.

## Comandos de trabalho

- "nova nota: <tema>": cria a nota no modelo, liga às notas relacionadas e atualiza o índice do módulo.
- "capítulo: <anotações>": transforma as anotações em notas.
- "revisar módulo <nº>": procura links quebrados, notas sem fonte e lacunas.
- "publicar": commit com mensagem descritiva em português + push na `main` (o GitHub Actions publica o site).
- Ao terminar um módulo: preencher a seção "Revisão rápida" do índice com 10 perguntas de autoavaliação.

## Verificação

Rode `npx quartz build` antes de publicar para checar se o site gera sem erros.
