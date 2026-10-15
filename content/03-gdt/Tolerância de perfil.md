---
title: Tolerância de perfil
tags: [gdt, perfil]
fontes: [ISO 1101:2017, ISO 1660:2017 (perfis), ASME Y14.5-2018, Krulikowski Fundamentals of Geometric Dimensioning and Tolerancing (cap. de perfil)]
status: rascunho
---

**Resumo:** a tolerância de perfil controla formas que não são retas, planas ou circulares: curvas, contornos e superfícies livres. Define uma faixa de largura constante em torno do perfil ideal (dado por cotas teoricamente exatas). Sem referência, controla só a forma; com referências, controla também orientação e posição. É a tolerância mais versátil do GD&T.

## O que é

| Símbolo | Característica | Zona |
|---|---|---|
| ⌒ | **Perfil de linha** | Em cada seção, entre duas linhas envolvendo círculos de diâmetro t centrados no perfil ideal |
| ⌓ | **Perfil de superfície** | Entre duas superfícies envolvendo esferas de diâmetro t centradas na superfície ideal |

Na prática: a zona é uma "faixa" de largura total $t$, distribuída **igualmente** dos dois lados do perfil ideal (±t/2), salvo indicação de faixa deslocada (modificador UZ na ISO, *unequally disposed*).

### Três usos, dependendo das referências

| Indicação | O que controla |
|---|---|
| Sem referência | Só a **forma** do perfil (ele pode estar em qualquer posição e inclinação) |
| Com referência de orientação | **Forma + orientação** |
| Com referências completas (A, B, C) | **Forma + orientação + posição** |

### O perfil ideal

O perfil teórico é definido por **cotas teoricamente exatas** (em caixa): raios, ângulos, coordenadas ou o próprio modelo 3D (em desenhos baseados em modelo).

## Por que importa no projeto

- **Peças cortadas a laser, plasma ou oxicorte:** o contorno inteiro de uma chapa recortada pode ser controlado com **um único** perfil de superfície, em vez de dezenas de cotas com ±.
- **Cames, perfis de dentes, gabaritos e matrizes de dobra.**
- **Peças fundidas e forjadas:** perfil com referências em alvos controla a peça bruta para garantir sobremetal de usinagem.
- **Substitui concentricidade e simetria** em normas modernas (ASME 2018).

## Como aplicar (passo a passo / regras práticas)

1. **Defina o perfil ideal** com cotas em caixa ou pelo modelo CAD.
2. **Indique a extensão** do perfil controlado: "todo o contorno" (símbolo de círculo na junção da linha de chamada, *all around*), ou "entre X e Y".
3. **Escolha as referências** conforme o que se quer controlar (só forma, ou forma + posição).
4. **Valor:** a largura total da faixa; ±t/2 de cada lado.
5. **Para peças cortadas termicamente**, consulte a capacidade do processo (laser: décimos de milímetro; plasma: algumas vezes mais; oxicorte: ainda mais). ⚠️ verificar com o fornecedor.

## Norma relacionada

- **ISO 1101:2017**: perfis de linha e de superfície.
- **ISO 1660:2017**: cotagem e tolerâncias de perfis.
- **ASME Y14.5-2018**: perfil com uso ampliado.

## Exemplo prático

**Situação:** uma **chapa de desgaste** de 12,5 mm, cortada a plasma, tem contorno curvo para encaixar numa estrutura, com quatro furos para parafusos de fixação.

- Contorno definido por cotas em caixa (raios e posições de tangência).
- **Perfil de superfície** em todo o contorno, em relação à face A (apoio) e aos furos B:

<span class="fcf"><span>⌓</span><span>1</span><span>A</span><span>B</span></span>

- Significa que todo o contorno real deve ficar dentro de uma faixa de ±0,5 mm em torno do contorno ideal, posicionado em relação à face e aos furos.
- **Furos:** posição Ø0,5 Ⓜ em relação a A, com cotas em caixa.

Com isso, a oficina recebe um critério único e claro para aceitar a chapa, e o contorno encaixa na estrutura.

> [!question] Exercício
>
> Um perfil de superfície de 0,4 mm é aplicado a uma face curva com referências A, B e C. Um ponto da superfície real está 0,25 mm "para fora" do perfil ideal. Está aprovado?
>
> > [!success]- Resolução
> >
> > A zona de 0,4 mm é distribuída igualmente: **±0,2 mm** em torno do perfil ideal. Um ponto a 0,25 mm para fora está **fora da zona** → **reprovado**.

## Erros comuns

- **Perfil sem cotas teoricamente exatas** para definir o perfil ideal.
- **Esquecer que o valor é a largura total** (±t/2, e não ±t).
- **Não indicar a extensão** do perfil (até onde vale).
- **Aplicar perfil com referência quando só a forma importa**, encarecendo a fabricação.

## Ver também

- [[Tolerâncias de localização]]
- [[Quadro de tolerância]]
- [[07-processos-fabricacao/index|Processos de fabricação]]
- [[03-gdt/index|Índice do módulo 03]]
