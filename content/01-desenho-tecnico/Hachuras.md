---
title: Hachuras
tags: [desenho-tecnico, cortes]
fontes: [ABNT NBR 12298:1995, ISO 128-50, French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de vistas em corte)]
status: rascunho
---

**Resumo:** hachuras são linhas finas paralelas, normalmente a 45°, que preenchem as superfícies tocadas por um plano de corte. Elas dizem "aqui tem material cortado" e, em conjuntos, ajudam a distinguir uma peça da outra.

## O que é

Em um [[Cortes e seções|corte ou seção]], a área onde o plano imaginário "toca" o material é preenchida com **hachura**: linhas paralelas, **contínuas estreitas**, inclinadas de preferência a **45°** em relação ao contorno principal ou ao eixo da peça.

### Regras principais

1. **Mesma peça, mesma hachura:** em todos os cortes e seções de uma peça, a hachura tem a mesma direção e o mesmo espaçamento.
2. **Peças vizinhas, hachuras diferentes:** em desenhos de conjunto, peças adjacentes recebem hachuras em **direções opostas** ou com **espaçamentos diferentes**.
3. **Espaçamento proporcional à área:** áreas pequenas, hachura mais fechada; áreas grandes, mais aberta. Nunca tão fechada que pareça uma mancha.
4. **Áreas muito grandes:** pode-se hachurar só uma faixa ao longo do contorno.
5. **Seções muito finas** (chapas, juntas, perfis de parede fina) podem ser **preenchidas em preto**. Se houver várias lado a lado, deixa-se um pequeno espaço branco entre elas.
6. **A hachura é interrompida** para dar lugar a cotas e textos dentro da área hachurada.
7. **Ângulo alternativo:** quando o contorno ou o eixo da peça já está a 45°, usa-se outro ângulo (30° ou 60°), para a hachura não ficar paralela ao contorno.
8. **Peças compostas** (soldadas, rebitadas, coladas) desenhadas como uma peça só podem ter as partes distinguidas por direções de hachura diferentes.

### Hachura e material

A hachura **geral** serve para qualquer material, e **o material é informado na legenda**. Existem padrões específicos para alguns materiais (por exemplo, para não metálicos, madeira, concreto), mas em desenho mecânico eles são pouco usados. ⚠️ verificar na NBR 12298 se há padrões obrigatórios por material.

## Por que importa no projeto

- **Sem hachura, o corte não é lido como corte:** quem lê não distingue cheio de vazio.
- **Em conjuntos**, é a hachura que mostra onde termina o alojamento e começa o rolamento, ou onde termina a tampa e começa a junta.
- **Peças soldadas:** direções diferentes deixam claro de quantas chapas a peça é feita.

## Como aplicar (passo a passo / regras práticas)

1. Defina a direção principal (45°) e o espaçamento (em CAD, um padrão do tipo ANSI31/ISO com escala ajustada à folha).
2. Hachure **todas** as áreas cortadas da mesma peça com o mesmo padrão.
3. Em conjuntos, alterne a direção (45° / 135°) entre peças vizinhas; quando faltarem direções, varie o espaçamento.
4. Não hachure eixos, parafusos, nervuras e outros elementos nos cortes longitudinais. Ver [[Cortes e seções]].
5. Preencha em preto juntas, chapas finas e retentores pequenos, se a escala não permitir hachurar.
6. Abra um "vazio" na hachura sob cada cota ou texto.

## Norma relacionada

- **ABNT NBR 12298:1995**, *Representação de área de corte por meio de hachuras em desenho técnico*. Define hachura a 45° em linha estreita e as regras de peças adjacentes. ⚠️ verificar se continua vigente.
- **ISO 128-50**: representação de áreas em cortes e seções. ⚠️ verificar a parte vigente da ISO 128.

## Exemplo prático

**Situação:** corte longitudinal de um **acoplamento de engrenagens** (dois cubos dentados, uma luva bipartida aparafusada e uma vedação entre cubo e luva), montado em dois eixos.

| Peça | Hachura |
|---|---|
| Eixos | Sem hachura (corte longitudinal) |
| Cubo esquerdo | 45° |
| Luva esquerda | 135° |
| Cubo direito | 45°, espaçamento maior (para diferenciar do cubo esquerdo) |
| Luva direita | 135°, espaçamento maior |
| Vedações (o-rings) | Preenchidas em preto (seção pequena) |
| Parafusos da luva | Sem hachura |

## Erros comuns

- **Hachura com linha larga.**
- **Duas peças vizinhas com a mesma hachura**, parecendo uma peça só.
- **Mesma peça com hachuras diferentes** em cortes diferentes.
- **Hachura paralela a um contorno a 45°**, que se confunde com a aresta.
- **Hachura passando por cima das cotas.**

## Ver também

- [[Cortes e seções]]
- [[Tipos de linha]]
- [[Desenho de conjunto e de detalhe]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
