---
title: Cadeia de tolerâncias (empilhamento)
tags: [tolerancias, analise-dimensional]
fontes: [Agostinho, Rodrigues e Lirani Tolerâncias, Ajustes, Desvios e Análise de Dimensões (cap. de cadeias de cotas), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. de tolerâncias — análise estatística), Fischer Mechanical Tolerance Stackup and Analysis]
status: rascunho
---

**Resumo:** quando várias peças se encostam numa montagem, as variações de cada uma se somam e determinam uma folga ou interferência final. A análise de cadeia (empilhamento) calcula essa variação, pelo pior caso (soma direta) ou por método estatístico (raiz da soma dos quadrados), e mostra onde apertar ou aliviar tolerâncias.

## O que é

Uma **cadeia de cotas** é uma sequência fechada de dimensões que, somadas com sinal, resultam numa **cota resultante** (normalmente uma folga). Exemplo: a folga axial de um eixo dentro de uma carcaça depende do comprimento interno da carcaça e das larguras de todas as peças montadas no eixo.

### Montando a cadeia

1. Identifique a **cota resultante** (a folga que interessa).
2. Percorra o "laço" de peças de um lado ao outro da folga, como num circuito.
3. Cada cota que **aumenta** a folga quando cresce é **positiva**; cada uma que **diminui** a folga é **negativa**.

$$
F = \sum_{\text{positivas}} C_i - \sum_{\text{negativas}} C_j
$$

### Método do pior caso (aritmético)

As tolerâncias simplesmente se somam:

$$
T_F = \sum_{i=1}^{n} T_i
$$

Garante 100 % das montagens dentro do limite, mas tende a exigir tolerâncias apertadas e caras quando há muitas peças.

### Método estatístico (RSS — raiz da soma dos quadrados)

Se as cotas variam de forma independente e aproximadamente normal, com processos centrados, a variação resultante é:

$$
T_F = \sqrt{\sum_{i=1}^{n} T_i^2}
$$

Isso é **menor** que a soma direta, porque é improvável que todas as peças estejam no extremo ao mesmo tempo. A premissa é forte: processos estáveis e centrados. Em produção de poucas peças (comum em manutenção e equipamentos especiais), o pior caso costuma ser mais seguro.

## Por que importa no projeto

- **Folgas axiais de rolamentos:** um rolamento livre precisa de espaço para a dilatação térmica do eixo; um conjunto de rolamentos cônicos precisa de uma folga ou pré-carga bem definida.
- **Montagens que "não fecham":** peças individualmente aprovadas que, juntas, não montam. Quase sempre o problema é uma cadeia não analisada.
- **Onde investir precisão:** a análise mostra qual peça contribui mais para a variação. Apertar a tolerância da peça certa é mais barato que apertar todas.
- **Alternativas de projeto:** calços e arruelas de ajuste (*shims*), anéis elásticos com espessuras selecionáveis e porcas de ajuste eliminam a necessidade de tolerâncias apertadas.

## Como aplicar (passo a passo / regras práticas)

1. **Desenhe o laço** em um croqui, com setas para cada cota e o sinal.
2. **Converta todas as cotas para nominal médio ± tolerância simétrica** (uma cota $30^{0}_{-0{,}12}$ vira $29{,}94 \pm 0{,}06$).
3. **Calcule a folga nominal (média)** pela soma com sinais.
4. **Calcule a variação** pelo pior caso e, se fizer sentido, pelo RSS.
5. **Compare com o requisito.** Se não atender, aperte a tolerância da maior contribuição, mude a referência de cotagem (para encurtar a cadeia) ou introduza um elemento de ajuste.
6. **Encurte a cadeia:** quanto menos peças no laço, menor a variação. Cotar a dimensão funcional diretamente (ver [[Cotagem]]) é a forma mais simples de fazer isso.

## Norma relacionada

Não há uma norma ISO específica para o método; ele é tratado na literatura técnica. A base de tolerâncias usada nas cotas é a **ISO 286** e a **ISO 2768**.

## Exemplo prático

**Situação:** um eixo com **dois rolamentos e um espaçador** entre eles é montado numa carcaça entre dois encostos. Deve sobrar uma folga axial entre 1,0 e 2,0 mm para a dilatação térmica do eixo.

| Cota | Valor | Convertida (média ± T/2) | Sinal |
|---|---|---|---|
| Distância entre encostos da carcaça | 200 ± 0,10 | 200,00 ± 0,10 | + |
| Largura do rolamento 1 | $30^{0}_{-0{,}12}$ | 29,94 ± 0,06 | − |
| Espaçador | 138,5 ± 0,05 | 138,50 ± 0,05 | − |
| Largura do rolamento 2 | $30^{0}_{-0{,}12}$ | 29,94 ± 0,06 | − |

⚠️ verificar a tolerância de largura dos rolamentos no catálogo.

**Folga média:** $200{,}00 - 29{,}94 - 138{,}50 - 29{,}94 = 1{,}62$ mm.

**Pior caso:** $T/2 = 0{,}10 + 0{,}06 + 0{,}05 + 0{,}06 = 0{,}27$ mm → folga de **1,35 a 1,89 mm**. ✔ Atende ao requisito.

**RSS:** $T/2 = \sqrt{0{,}10^2 + 0{,}06^2 + 0{,}05^2 + 0{,}06^2} = \sqrt{0{,}0197} \approx 0{,}14$ mm → 1,48 a 1,76 mm.

**Leitura:** a carcaça é a maior contribuição (0,10 de 0,27). Se o requisito fosse mais apertado, a primeira providência seria melhorar a tolerância entre os encostos da carcaça, ou usar um calço de ajuste na tampa.

> [!question] Exercício
>
> Numa cadeia de 5 peças, cada uma com ±0,1 mm, qual a variação da cota resultante pelo pior caso e pelo RSS? Quanto se "ganha" com o método estatístico?
>
> > [!success]- Resolução
> >
> > - **Pior caso:** $5 \times 0{,}1 = \pm 0{,}5$ mm.
> > - **RSS:** $\sqrt{5 \times 0{,}1^2} = 0{,}1\sqrt{5} \approx \pm 0{,}22$ mm.
> >
> > O RSS dá uma variação cerca de 2,2 vezes menor ($\sqrt{5}$). A vantagem cresce com o número de peças, mas só vale se os processos forem estáveis, centrados e independentes.

## Erros comuns

- **Errar o sinal** de uma cota no laço.
- **Usar o RSS em peças únicas** ou em processos não centrados.
- **Esquecer peças "finas"** no laço (juntas, arruelas, anéis elásticos), que também têm tolerância.
- **Não considerar a dilatação térmica** em operação, que muda as folgas.

## Ver também

- [[Cotagem]]
- [[Tipos de ajuste]]
- [[Conceitos de tolerância]]
- [[02-tolerancias-ajustes/index|Índice do módulo 02]]
