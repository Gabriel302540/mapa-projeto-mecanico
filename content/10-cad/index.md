---
title: 10 · CAD
tags: [indice, cad]
---

**Resumo:** AutoCAD e boas práticas de detalhamento: layers, blocos, cotas, layouts e plotagem.

## Por que este módulo importa
Um padrão de CAD bem definido faz todos os desenhos da equipe saírem iguais, facilita revisões e evita erros de escala na plotagem.

## Tópicos
Ordem sugerida de estudo: de cima para baixo.

- [x] [[Organização de layers]]
- [x] [[Blocos e atributos]]
- [x] [[Estilos de cota e texto|Estilos de cota e de texto]]
- [x] [[Model e layout|Model e layout (paper space)]]
- [x] [[Plotagem e escalas]]
- [x] [[Padrão de detalhamento]]
- [x] [[Nomenclatura de arquivos|Nomenclatura e organização de arquivos]]

## Normas principais
Lista de partida, para conferir no documento original. Nenhum trecho de norma é reproduzido aqui.

- ISO 13567 (série) — organização de layers em CAD ⚠️ verificar aplicação em mecânica

## Módulos relacionados
- [[01-desenho-tecnico/index|01 · Desenho técnico]]
- [[09-metodologia-de-projeto/index|09 · Metodologia de projeto]]

## Revisão rápida

Tente responder antes de abrir a resposta.

> [!question] 1. Por que as propriedades dos objetos devem ser 'ByLayer'?
>
> > [!success]- Resposta
> >
> > Para que **cor, tipo e espessura de linha venham do layer**, garantindo o padrão da norma e permitindo alterar todo o desenho mudando só o layer. Ver [[Organização de layers]].

> [!question] 2. Em que layer devem ser desenhados os objetos de um bloco e por quê?
>
> > [!success]- Resposta
> >
> > No **layer 0**, porque assim eles **herdam o layer** em que o bloco é inserido. Ver [[Blocos e atributos]].

> [!question] 3. Como gerar automaticamente a lista de desenhos de um projeto a partir das legendas?
>
> > [!success]- Resposta
> >
> > Com a **extração de dados** dos **atributos** do bloco de legenda (número, título, revisão) de todos os arquivos. Ver [[Blocos e atributos]].

> [!question] 4. Sem anotatividade, que altura de texto usar no modelo para 3,5 mm no papel numa vista 1:20?
>
> > [!success]- Resposta
> >
> > $3{,}5 \times 20 = 70$ mm no modelo. Ver [[Estilos de cota e texto]].

> [!question] 5. Por que nunca se deve digitar o valor de uma cota por cima do valor medido?
>
> > [!success]- Resposta
> >
> > Porque a cota perde a **associatividade**: se a geometria mudar, o valor não acompanha, e o desenho fica com cota errada sem ninguém perceber. Ver [[Estilos de cota e texto]].

> [!question] 6. Qual a regra de ouro do espaço do modelo e onde se aplica a escala das vistas?
>
> > [!success]- Resposta
> >
> > **Desenhar sempre em 1:1** no modelo. A escala das vistas é aplicada nas **viewports** do layout. Ver [[Model e layout]].

> [!question] 7. Em que escala se plota um layout? Por quê?
>
> > [!success]- Resposta
> >
> > Em **1:1**, porque o layout já está em tamanho de papel e as escalas das vistas estão nas viewports. Ver [[Plotagem e escalas]].

> [!question] 8. Linhas de centro saem contínuas numa viewport em 1:10 e corretas em outra em 2:1. Qual a causa provável?
>
> > [!success]- Resposta
> >
> > **PSLTSCALE desligado**: os padrões de tipo de linha não são escalados por viewport. Ligar (PSLTSCALE = 1) e regenerar. Ver [[Plotagem e escalas]].

> [!question] 9. Cite quatro itens de uma lista de verificação antes de liberar um desenho.
>
> > [!success]- Resposta
> >
> > Legenda completa; vistas suficientes; cotas completas sem duplicidade; tolerâncias e ajustes nas cotas funcionais e tolerância geral declarada; rugosidades; soldas; notas gerais; revisão atualizada; coerência com o conjunto. Ver [[Padrão de detalhamento]].

> [!question] 10. Por que usar caminhos relativos em referências externas (xrefs)?
>
> > [!success]- Resposta
> >
> > Para que as referências **não quebrem** quando a pasta do projeto for copiada ou movida para outro computador ou servidor. Ver [[Nomenclatura de arquivos]].

