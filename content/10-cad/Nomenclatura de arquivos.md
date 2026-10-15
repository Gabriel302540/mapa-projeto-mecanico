---
title: Nomenclatura e organização de arquivos
tags: [cad, documentacao]
fontes: [ISO 11442 (gestão de documentos técnicos) ⚠️ verificar, ISO 7200 (identificação de documentos), Autodesk AutoCAD — documentação oficial (referências externas e caminhos relativos), boas práticas de gestão de dados de produto (PDM)]
status: rascunho
---

**Resumo:** com centenas de desenhos, a forma de nomear e organizar arquivos decide se alguém encontra a versão certa em segundos ou trabalha com um arquivo errado. Um padrão de nome baseado no número do desenho, pastas por situação (em elaboração, liberado, obsoleto) e cuidados com referências externas evitam a maioria dos problemas.

## O que é

### Padrão de nome

Um formato comum é o **número do desenho** (único, igual ao da legenda) seguido da **revisão** nos arquivos emitidos:

```
DES-0123_C.pdf          (emitido, revisão C)
DES-0123.dwg            (arquivo de trabalho)
```

Recomendações:
- **Sem espaços, acentos ou caracteres especiais** (evita problemas em servidores, e-mail e sistemas).
- **Número igual ao da legenda.**
- **Títulos descritivos** ficam na legenda e no sistema, não necessariamente no nome do arquivo.
- **Datas**, se usadas, no formato AAAA-MM-DD (ordenam corretamente).

### Estrutura de pastas

```
PROJETO_XYZ/
├── 01_EM_ELABORACAO/
├── 02_LIBERADO/
│   ├── DWG/
│   └── PDF/
├── 03_OBSOLETO/
├── 04_MEMORIAIS/
├── 05_CATALOGOS_REFERENCIAS/
└── 06_AS_BUILT/
```

O arquivo só passa para **LIBERADO** depois de aprovado (ver [[Controle de desenhos]]). Revisões antigas vão para **OBSOLETO**, não são apagadas.

### Referências externas (xrefs)

Desenhos que usam outros como referência (arranjo geral com xref dos equipamentos) devem usar **caminhos relativos**, para não "quebrar" ao copiar a pasta do projeto. Ao enviar arquivos a terceiros, use o empacotamento (ETRANSMIT) com todas as referências e fontes.

### Sistemas PDM/GED

Em equipes maiores, sistemas de gestão de dados de produto (PDM) ou de documentos (GED) controlam versões, estados de aprovação e acesso, substituindo as pastas manuais. O princípio é o mesmo: **uma fonte única da verdade**.

## Por que importa no projeto

- **Achar o desenho certo rapidamente**, inclusive anos depois, na manutenção.
- **Evitar trabalhar sobre versões erradas.**
- **Enviar pacotes completos** a fornecedores (sem referências faltando).

## Como aplicar (passo a passo / regras práticas)

1. **Defina e documente** o padrão de nome e de pastas.
2. **Nome do arquivo = número do desenho.**
3. **Separe por situação** (elaboração, liberado, obsoleto).
4. **Use caminhos relativos** em xrefs e imagens.
5. **Faça cópia de segurança** automática e versionada da pasta de projetos.
6. **Arquive PDFs** dos documentos liberados (de preferência PDF/A).

## Norma relacionada

- **ISO 7200**: identificação de documentos (número e revisão).
- **ISO 11442**: gestão de documentação técnica. ⚠️ verificar.

## Exemplo prático

**Situação:** a pasta de um projeto antigo tem arquivos como "eixo novo final.dwg", "eixo novo final 2.dwg" e "eixo REVISADO ok.dwg". Ninguém sabe qual foi fabricado.

**Reorganização:**
1. Comparar os arquivos com os PDFs enviados à fabricação (e com a peça instalada, se necessário).
2. Atribuir número de desenho e revisão conforme o padrão: DES-0457 rev. A, B, C.
3. Mover a versão fabricada para LIBERADO (e AS_BUILT, se for o caso) e as demais para OBSOLETO.
4. Registrar no quadro de revisões o que mudou entre elas.

> [!question] Exercício
>
> Por que nomes de arquivo como "eixo final.dwg" são um problema, mesmo numa equipe pequena?
>
> > [!success]- Resolução
> >
> > Porque **"final" não diz qual versão** é válida, e logo surgem "final 2", "final revisado"... O nome não corresponde ao número da legenda, impossibilitando a busca; não indica a revisão; e outra pessoa não consegue saber, sem abrir e comparar os arquivos, qual foi fabricado. Com número único e revisão, a identificação é imediata.

## Erros comuns

- **Nomes descritivos e ambíguos** ("final", "novo", "ok").
- **Apagar revisões antigas** em vez de arquivá-las.
- **Caminhos absolutos** em referências externas.
- **Enviar DWG sem as referências** e fontes.

## Ver também

- [[Controle de desenhos]]
- [[Padrão de detalhamento]]
- [[Plotagem e escalas]]
- [[10-cad/index|Índice do módulo 10]]
