---
title: Concentradores de tensão
tags: [elementos, eixos, fadiga]
fontes: [Pilkey e Pilkey Peterson's Stress Concentration Factors, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 3, 6 e 7), Norton Projeto de Máquinas (cap. de concentração de tensões), DIN 743-2]
status: rascunho
---

**Resumo:** qualquer mudança brusca de geometria — ressalto, furo, rasgo, canal, rosca — faz a tensão local subir acima da tensão nominal. O fator teórico Kt mede esse aumento; o fator de fadiga Kf, que é um pouco menor, considera a sensibilidade do material ao entalhe. Projetar bem os concentradores é a forma mais barata de aumentar a vida de um eixo.

## O que é

### Fator teórico $K_t$

$$
\sigma_{\max} = K_t\,\sigma_{\text{nominal}} \qquad \tau_{\max} = K_{ts}\,\tau_{\text{nominal}}
$$

$K_t$ depende **só da geometria** (relação entre raio do entalhe e diâmetro, relação entre diâmetros) e do tipo de carga. É obtido de gráficos (Peterson) ou por elementos finitos.

### Fator de fadiga $K_f$ e sensibilidade ao entalhe

Na fadiga, o efeito real é um pouco menor que $K_t$, porque o material "redistribui" a tensão em volumes muito pequenos:

$$
K_f = 1 + q\,(K_t - 1)
$$

onde $q$ (de 0 a 1) é a **sensibilidade ao entalhe**. Aços de alta resistência e raios maiores têm $q$ próximo de 1. Uma forma usada é a equação de Neuber:

$$
q = \frac{1}{1 + \sqrt{a}/\sqrt{r}}
$$

com $\sqrt{a}$ dependendo do material (diminui com a resistência) e $r$ o raio do entalhe. Na dúvida, usar $K_f = K_t$ é conservador.

### Valores típicos para primeira estimativa (eixos)

| Detalhe | $K_t$ (flexão) | $K_{ts}$ (torção) |
|---|---|---|
| Ressalto com canto vivo ($r/d$ ≈ 0,02) | 2,7 | 2,2 |
| Ressalto bem arredondado ($r/d$ ≈ 0,1) | 1,7 | 1,5 |
| Rasgo de chaveta feito com fresa de topo ($r/d$ ≈ 0,02) | 2,14 | 3,0 |
| Rasgo de chaveta "em trenó" (fresa de disco) | 1,7 | — |
| Canal de anel elástico | 5,0 | 3,0 |

Fonte: tabela de estimativas iniciais de Shigley. ⚠️ verificar e refinar com os gráficos de Peterson para a geometria real.

## Por que importa no projeto

- **As trincas de fadiga nascem nos concentradores**, quase sempre na superfície.
- **O canal de anel elástico é um dos piores detalhes** possíveis numa região de alto momento: Kt ≈ 5.
- **Dois concentradores juntos** (rasgo de chaveta terminando exatamente no raio do ressalto) multiplicam os efeitos.
- **Soluções de projeto** costumam ser baratas: aumentar o raio, afastar o rasgo do ressalto, usar canais de alívio, mudar a posição de um anel elástico para uma região de momento baixo.

## Como aplicar (passo a passo / regras práticas)

1. **Use o maior raio de concordância possível** nos ressaltos. Se o rolamento tem raio de canto pequeno, use:
   - **canal de alívio** (*undercut*) com raio maior, rebaixado no ressalto;
   - **anel espaçador** com chanfro, permitindo raio maior no eixo.
2. **Termine rasgos de chaveta antes do ressalto**, a uma distância de pelo menos alguns milímetros do início do raio.
3. **Prefira rasgo em trenó** (fresa de disco) quando possível, que tem saída gradual.
4. **Coloque anéis elásticos e furos transversais em regiões de momento baixo** (pontas do eixo, perto dos mancais externos).
5. **Especifique o raio e o acabamento** do raio no desenho: "R5 mín., Ra 1,6".
6. **Considere processos de reforço da superfície:** roletamento dos raios, jateamento com granalha (*shot peening*), têmpera superficial. Eles criam tensões residuais de compressão que dificultam o início da trinca.

## Norma relacionada

- **DIN 743-2**: fatores de forma e de entalhe para eixos (tabelas e fórmulas).
- **Peterson's Stress Concentration Factors**: referência clássica, não normativa, com gráficos para centenas de geometrias.

## Exemplo prático

**Situação:** o eixo de um acionamento de transportador quebrou junto ao assento do rolamento. A fratura começou no canto do ressalto, que tinha raio de 1 mm num eixo de Ø100 → Ø120.

- $r/d = 1/100 = 0{,}01$ e $D/d = 1{,}2$ → $K_t \approx 2{,}8$ ou mais (gráfico de Peterson ⚠️).
- O rolamento tinha raio de canto de 2,1 mm, por isso o projetista usou raio pequeno no eixo.

**Solução de reprojeto:**

- Canal de alívio com **raio de 6 mm** no eixo, rebaixado no ressalto (o rolamento continua encostando na face).
- $r/d = 0{,}06$ → $K_t \approx 1{,}6$ ⚠️.
- Redução de cerca de 40 % na tensão máxima local, sem mudar diâmetros nem rolamento.

> [!question] Exercício
>
> Um ressalto tem $K_t$ = 2,2 e o material tem sensibilidade ao entalhe $q$ = 0,85. Qual é $K_f$? Se a tensão nominal de flexão alternada é 80 MPa, qual a tensão efetiva para a fadiga?
>
> > [!success]- Resolução
> >
> > $K_f = 1 + 0{,}85 \times (2{,}2 - 1) = 1 + 1{,}02 = 2{,}02$.
> > Tensão efetiva: $2{,}02 \times 80 \approx 162$ MPa.

## Erros comuns

- **Não especificar o raio** de concordância no desenho.
- **Rasgo de chaveta terminando no raio** do ressalto.
- **Anel elástico na seção de maior momento.**
- **Usar Kt de tração em flexão ou torção** (são diferentes).
- **Ignorar concentradores em reparos** (soldas, furos para graxeira feitos depois).

## Ver também

- [[Fadiga de eixos]]
- [[Chavetas]]
- [[Fixação axial]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
