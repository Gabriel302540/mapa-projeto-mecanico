---
title: Indicação de tolerâncias no desenho
tags: [tolerancias, desenho]
fontes: [ISO 286-1:2010, ISO 14405-1 (especificação dimensional), ISO 129-1, ABNT NBR 6158:1995, Agostinho, Rodrigues e Lirani Tolerâncias, Ajustes, Desvios e Análise de Dimensões]
status: rascunho
---

**Resumo:** uma tolerância pode ser escrita no desenho de várias formas: pela classe ISO (Ø50 H7), pelos desvios (Ø50 +0,025/0), pelos limites (50,025/50,000) ou por ±. Cada forma tem regras de escrita, e o ajuste entre duas peças é indicado no desenho de conjunto com as duas classes (Ø50 H7/k6).

## O que é

### Formas de indicação

| Forma | Exemplo | Quando usar |
|---|---|---|
| **Classe ISO** | Ø50 H7 | Furos e eixos de ajuste; a oficina consulta a tabela ou usa calibrador |
| **Classe com desvios entre parênteses** | Ø50 H7 $\left(^{+0{,}025}_{0}\right)$ | Mais prático para a oficina, que não precisa consultar tabela |
| **Desvios** | $\varnothing 50^{+0{,}025}_{0}$ | Tolerâncias que não seguem uma classe ISO |
| **Simétrica** | 120 ± 0,1 | Posições e comprimentos com variação simétrica |
| **Limites** | $\begin{smallmatrix}50{,}025\\50{,}000\end{smallmatrix}$ | Quando se quer evitar contas na oficina |
| **Limite único** | R5 máx.; 20 mín. | Raios máximos, profundidades mínimas de rosca |
| **Ajuste (conjunto)** | Ø50 H7/k6 | Desenho de conjunto: indica o ajuste entre as duas peças |

### Regras de escrita

1. **Desvio superior em cima, inferior embaixo**, em letra menor que a cota.
2. **Mesmo número de casas decimais** nos dois desvios: $^{+0{,}025}_{+0{,}009}$, e não $^{+0{,}025}_{+0{,}01}$. O desvio zero é escrito só "0", sem sinal.
3. **Mesma unidade da cota** (mm), sem escrever a unidade.
4. **Desvios simétricos:** escreve-se uma vez com "±": 50 ± 0,1.
5. **Ângulos:** $30° \pm 0°30'$ ou $30° \pm 0{,}5°$.
6. **No conjunto**, a classe do furo vem antes da do eixo: "Ø50 H7/k6" ou com as duas classes uma sobre a outra.

### O princípio da independência e a envoltória

Por padrão, pela **ISO 8015**, uma tolerância dimensional controla **só o tamanho local** (as medidas entre dois pontos opostos), e não a forma. Um eixo pode estar dentro de Ø50 g6 em todos os pontos medidos e mesmo assim estar levemente torto. Se a função exige que o eixo **monte** num furo perfeito (o eixo inteiro dentro de um cilindro de diâmetro máximo), aplica-se o **requisito de envoltória**, indicado pelo símbolo Ⓔ após a tolerância: **Ø50 g6 Ⓔ**. Ver [[03-gdt/index|GD&T]].

Alguns desenhos e empresas trabalham com o princípio da envoltória como padrão (antiga norma alemã), o que deve estar declarado no desenho. ⚠️ verificar o padrão da empresa e a nota "ISO 8015" na legenda.

## Por que importa no projeto

- **Clareza para a oficina:** a forma de indicar deve facilitar a fabricação e a inspeção, sem cálculos desnecessários no chão de fábrica.
- **Evitar ambiguidades:** casas decimais diferentes ou sinais faltando geram dúvida sobre o limite real.
- **Ajuste no conjunto e classe no detalhe:** cada desenho de detalhe precisa ser autossuficiente (ver [[Desenho de conjunto e de detalhe]]).

## Como aplicar (passo a passo / regras práticas)

1. **Ajustes ISO:** escreva a classe e, se a oficina preferir, os desvios entre parênteses.
2. **Posições e comprimentos funcionais:** use ±.
3. **Cotas sem função específica:** deixe para a tolerância geral (ver [[Tolerâncias gerais]]).
4. **Conjunto:** indique o ajuste "H7/k6" nos encaixes relevantes.
5. **Envoltória:** se a peça precisa montar com folga mínima garantida, avalie usar Ⓔ.
6. **Em CAD:** use o recurso de tolerância do estilo de cota, e não texto digitado sobre a cota (que deixa de ser associativo).

## Norma relacionada

- **ISO 286-1:2010**: designação de classes de tolerância e ajustes.
- **ISO 129-1**: indicação de dimensões e tolerâncias.
- **ISO 14405-1**: especificação dimensional (tamanho linear) e modificadores, incluindo Ⓔ.
- **ISO 8015**: princípio da independência.

## Exemplo prático

**Situação:** um eixo de Ø45 recebe um rolamento (assento k6) e um retentor (assento h11).

No desenho de detalhe do eixo:
- Assento do rolamento: **Ø45 k6** $\left(^{+0{,}018}_{+0{,}002}\right)$.
- Assento do retentor: **Ø45 h11** $\left(^{0}_{-0{,}160}\right)$.
- Comprimento do assento do rolamento: 25 ± 0,1.
- Demais cotas: tolerância geral ISO 2768-m.

No desenho de conjunto: **Ø45 k6** no eixo e **Ø85 H7** no alojamento do rolamento (os anéis já têm tolerância própria; indica-se a classe da peça que o projetista define).

⚠️ verificar valores na ISO 286-2.

> [!question] Exercício
>
> O que está errado na indicação $\varnothing 30^{+0{,}03}_{-0{,}015}$? Reescreva corretamente.
>
> > [!success]- Resolução
> >
> > Os desvios têm **números de casas decimais diferentes** (2 e 3). O correto é $\varnothing 30^{+0{,}030}_{-0{,}015}$.

## Erros comuns

- **Casas decimais diferentes** entre os desvios.
- **Esquecer o sinal** de um desvio ou escrever "+0" e "−0".
- **Tolerância digitada como texto** no CAD, que não se atualiza se a cota mudar.
- **Indicar ajuste "H7/k6" no desenho de detalhe**, em vez da classe da própria peça.

## Ver também

- [[Posições de tolerância]]
- [[Tolerâncias gerais]]
- [[Cotagem]]
- [[03-gdt/index|GD&T]]
- [[02-tolerancias-ajustes/index|Índice do módulo 02]]
