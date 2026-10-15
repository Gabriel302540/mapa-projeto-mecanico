---
title: Leitura de um desenho com GD&T
tags: [gdt, leitura]
fontes: [ISO 1101:2017, ISO 5459:2011, ISO 8015:2011, Krulikowski Fundamentals of Geometric Dimensioning and Tolerancing, Henzold Geometrical Dimensioning and Tolerancing for Design, Manufacturing and Inspection]
status: rascunho
---

**Resumo:** ler GD&T é traduzir cada quadro numa frase: "este elemento deve estar dentro de tal zona, com tal tamanho, orientada ou posicionada em relação a tais referências". Esta nota propõe um roteiro de leitura e aplica-o a um exemplo completo de eixo.

## O que é

### Roteiro de leitura

1. **Legenda:** qual norma vale (ISO 8015 ou ASME Y14.5)? Há tolerâncias gerais geométricas? Ver [[Independência e envoltória]].
2. **Referências:** localize os triângulos A, B, C. São superfícies ou eixos? Entenda como a peça se apoia na montagem.
3. **Forma das referências:** há planeza, cilindricidade? Elas definem a qualidade de todas as outras medições.
4. **Para cada quadro**, leia em voz alta:
   - **o quê:** o símbolo (posição, batimento...);
   - **qual elemento:** superfície (seta na face) ou eixo/plano médio (seta alinhada à cota);
   - **zona:** com Ø (cilíndrica) ou sem (planos paralelos), largura t;
   - **modificadores:** Ⓜ, Ⓛ, Ⓟ, CZ;
   - **em relação a quê:** referências na ordem.
5. **Cotas em caixa:** a posição teórica do elemento.
6. **Pergunte a função:** por que o projetista controlou isso? Ajuda a entender e a detectar erros.

### Frases-modelo

| Quadro | Leitura |
|---|---|
| ⏥ 0,02 | "A face deve estar entre dois planos paralelos afastados de 0,02 mm." |
| ⊥ Ø0,03 A | "O eixo do furo deve estar dentro de um cilindro de Ø0,03 mm perpendicular a A." |
| ⌖ Ø0,2 Ⓜ A B | "O eixo de cada furo deve estar num cilindro de Ø0,2 mm (mais o bônus) centrado na posição teórica, medida a partir de A e B." |
| ↗ 0,02 A–B | "Ao girar a peça em torno do eixo comum A–B, cada seção da superfície deve dar no máximo 0,02 mm no relógio." |

## Por que importa no projeto

- **Fabricar:** o torneiro ou fresador precisa saber de onde partir e o que priorizar.
- **Inspecionar:** o inspetor monta a peça no dispositivo conforme as referências.
- **Revisar desenhos de terceiros:** catálogos e desenhos de fornecedores, principalmente estrangeiros, usam GD&T intensamente.

## Como aplicar (passo a passo / regras práticas)

Aplique o roteiro a cada desenho novo. Na dúvida sobre um quadro, desenhe a zona de tolerância num croqui: dois planos, um cilindro, uma faixa. Isso quase sempre esclarece.

## Norma relacionada

- **ISO 1101:2017**, **ISO 5459:2011**, **ISO 8015:2011** e **ISO 2692:2021** (conjunto de regras para ler o desenho ISO).

## Exemplo prático

**Situação:** desenho de um **eixo de saída de redutor**, com as seguintes indicações:

1. Assentos dos rolamentos: **Ø70 k6 Ⓔ**, com triângulos de referência **A** (lado esquerdo) e **B** (lado direito), e **cilindricidade 0,005** em cada um.
2. Assento da engrenagem: **Ø80 m6**, com **batimento circular 0,015 A–B**.
3. Face de encosto da engrenagem: **batimento circular axial 0,01 A–B**.
4. Rasgo de chaveta 22 N9: **simetria 0,03** em relação ao plano médio do assento Ø80.
5. Ponta de acionamento Ø60 k6: **batimento circular 0,02 A–B**.

**Leitura:**

1. Os assentos dos rolamentos devem caber num cilindro perfeito de Ø70,021 (envoltória no máximo material) e cada um deve ter forma cilíndrica dentro de 5 µm. Juntos, definem o **eixo de rotação A–B**.
2. Girando o eixo apoiado em A e B, o assento da engrenagem não pode "bater" mais que 15 µm em nenhuma seção.
3. A face de encosto não pode oscilar mais que 10 µm no relógio axial: a engrenagem encosta sem inclinar.
4. O rasgo deve estar centrado: seu plano médio entre dois planos afastados de 0,03 mm, simétricos ao plano que contém o eixo do assento.
5. A ponta de acionamento não pode bater mais que 20 µm em relação ao eixo de rotação: o acoplamento trabalha alinhado.

⚠️ verificar os valores com o catálogo de rolamentos e a norma de qualidade das engrenagens.

> [!question] Exercício
>
> Leia o quadro abaixo, aplicado (com a seta alinhada à cota) a um padrão de "6× Ø11 +0,2/0":
>
> <span class="fcf"><span>⌖</span><span>Ø0,3 Ⓜ</span><span>A</span><span>B</span><span>C</span></span>
>
> > [!success]- Resolução
> >
> > "O **eixo** de cada um dos 6 furos deve estar dentro de um **cilindro de Ø0,3 mm**, centrado na **posição teórica** (dada por cotas em caixa), com a peça apoiada primeiro em **A**, depois em **B** e por último em **C**. Como há **Ⓜ**, a tolerância aumenta com o tamanho do furo: um furo com Ø11,2 tem Ø0,3 + 0,2 = Ø0,5 de tolerância de posição."

## Erros comuns

- **Ler a seta na superfície como se fosse no eixo**, e vice-versa.
- **Ignorar a ordem das referências.**
- **Esquecer o bônus** de Ⓜ.
- **Ler um desenho ASME com regras ISO.**

## Ver também

- [[Quadro de tolerância]]
- [[Referências geométricas]]
- [[Batimento]]
- [[Requisito de máximo material]]
- [[03-gdt/index|Índice do módulo 03]]
