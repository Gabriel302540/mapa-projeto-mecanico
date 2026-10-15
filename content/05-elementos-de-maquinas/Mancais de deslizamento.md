---
title: Mancais de deslizamento (buchas)
tags: [elementos, mancais]
fontes: [ISO 4378 (terminologia de mancais de deslizamento), ISO 7902 (mancais hidrodinâmicos — cálculo) ⚠️ verificar, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 12 — lubrificação e mancais de deslizamento), Niemann Elementos de Máquinas (cap. de mancais de deslizamento), catálogos técnicos de buchas de bronze e autolubrificantes]
status: rascunho
---

**Resumo:** num mancal de deslizamento, o eixo (munhão) gira dentro de uma bucha, separado dela por um filme de lubrificante — ou em contato parcial, quando o filme não se forma completamente. São robustos, suportam choques, cargas muito altas e rotações baixas, e ocupam pouco espaço radial. O dimensionamento básico verifica a pressão média p, a velocidade v e o produto pv.

## O que é

### Regimes de lubrificação

| Regime | Situação | Exemplo |
|---|---|---|
| **Limite** | Superfícies em contato, separadas só por camadas finas de lubrificante e aditivos | Rotação muito baixa, partidas, buchas engraxadas de articulações |
| **Misto** | Parte da carga no filme, parte nos picos de rugosidade | Mancais pesados de baixa rotação |
| **Hidrodinâmico** | Filme completo gerado pela própria rotação (efeito de cunha) | Turbinas, motores, compressores, redutores grandes |
| **Hidrostático** | Filme completo gerado por bomba externa | Máquinas muito pesadas e lentas, mancais de precisão |

### Grandezas básicas

Para um mancal de diâmetro $d$, comprimento $L$, carga radial $F$ e rotação $n$:

$$
p = \frac{F}{d\,L} \qquad\qquad v = \frac{\pi\,d\,n}{60\,000}\ [\text{m/s}] \qquad\qquad pv
$$

- **p** limita o esmagamento e a extrusão do material da bucha.
- **v** limita o aquecimento e o desgaste.
- **pv** é proporcional à potência dissipada por atrito por unidade de área: limita a temperatura.

Cada material de bucha tem limites de $p$, $v$ e $pv$ (do fabricante). Ordens de grandeza para **bronze lubrificado com graxa** em regime limite/misto: $p$ até cerca de 10 a 15 MPa em rotações baixas e $pv$ de 1 a 3 MPa·m/s. Buchas autolubrificantes (bronze sinterizado, polímeros, bronze com grafite) têm limites próprios. ⚠️ verificar no catálogo do material.

### Geometria e folga

- **Relação L/d:** normalmente entre 0,5 e 1,5. Buchas longas sofrem mais com desalinhamento (contato nas bordas).
- **Folga diametral:** ordem de 0,1 % a 0,2 % do diâmetro em mancais hidrodinâmicos (ajustes como H7/e7, H8/f7); maiores em mancais pesados e quentes. ⚠️ verificar.
- **Canais de lubrificação:** levam o lubrificante para a **zona descarregada** (nunca no meio da zona de carga, onde interrompem o filme).

### Mancal hidrodinâmico (noção)

O comportamento é governado pelo **número de Sommerfeld**:

$$
S = \left(\frac{r}{c}\right)^2 \frac{\mu\,N}{P}
$$

com $r$ o raio, $c$ a folga radial, $\mu$ a viscosidade, $N$ a rotação (rps) e $P$ a pressão média. Gráficos (Raimondi e Boyd) dão, a partir de $S$, a espessura mínima do filme, o atrito e a temperatura. A espessura mínima precisa ser várias vezes maior que a soma das rugosidades do munhão e da bucha.

## Por que importa no projeto

- **Equipamentos pesados e lentos**, sujeitos a choques e contaminação, frequentemente usam mancais de deslizamento de bronze, refrigerados a água, com grandes diâmetros.
- **Articulações, pinos e alavancas** usam buchas engraxadas ou autolubrificantes.
- **Custo e espaço:** uma bucha é muito mais compacta e barata que um rolamento equivalente em cargas altas e rotações baixas.
- **Desvantagens:** atrito de partida maior, dependência total da lubrificação, desgaste gradual (folga aumenta com o tempo).

## Como aplicar (passo a passo / regras práticas)

1. **Calcule p, v e pv** com a carga máxima de operação.
2. **Escolha o material** cujos limites atendam com margem (bronze, metal patente/babbitt, autolubrificante, polímero).
3. **Defina L/d** e a folga (ajuste ISO).
4. **Projete a lubrificação:** graxeira, canais na zona descarregada, ou sistema de óleo.
5. **Especifique o acabamento** do munhão (Ra 0,2–0,8) e a dureza maior que a da bucha. Ver [[Rugosidade pela função]].
6. **Fixe a bucha** no alojamento com interferência (H7/p6 ou s6) ou com pino anti-giro.
7. **Considere a refrigeração** se pv e a carga forem altos.

## Norma relacionada

- **ISO 4378**: terminologia de mancais de deslizamento.
- **ISO 7902**: cálculo de mancais radiais hidrodinâmicos. ⚠️ verificar.
- **ISO 4379 / DIN 1850**: dimensões de buchas de ligas de cobre. ⚠️ verificar.

## Exemplo prático

**Situação:** bucha de bronze engraxada para o eixo de uma roda motriz de transportador lento: **F = 40 kN**, **d = 100 mm**, **L = 100 mm**, **n = 60 rpm**.

- $p = \dfrac{40\,000}{100 \times 100} = 4{,}0$ MPa
- $v = \dfrac{\pi \times 100 \times 60}{60\,000} \approx 0{,}31$ m/s
- $pv \approx 4{,}0 \times 0{,}31 = 1{,}26$ MPa·m/s

Valores compatíveis com bronze engraxado, com margem razoável (confirmar no catálogo do material). Munhão retificado Ra 0,4, endurecido; ajuste H8/e8 na bucha; bucha fixada no alojamento com H7/s6; graxeira com canal levando a graxa para a parte superior (zona descarregada, já que a carga é para baixo).

> [!question] Exercício
>
> Na mesma bucha, a rotação passa para 300 rpm e a carga cai para 25 kN. O pv aumenta ou diminui?
>
> > [!success]- Resolução
> >
> > - $p = 25\,000/10\,000 = 2{,}5$ MPa
> > - $v = \pi \times 100 \times 300/60\,000 \approx 1{,}57$ m/s
> > - $pv \approx 3{,}9$ MPa·m/s
> >
> > O **pv triplica**, mesmo com carga menor. Provavelmente fica acima do limite do bronze engraxado, e seria preciso lubrificação a óleo, outro material ou um rolamento.

## Erros comuns

- **Canal de lubrificação na zona de carga.**
- **Munhão mais mole que a bucha.**
- **Bucha longa com eixo flexível**, gerando contato nas bordas.
- **Folga pequena demais** em mancais que aquecem.
- **Calcular só p** e esquecer pv.

## Ver também

- [[Seleção de rolamentos]]
- [[Ajustes recomendados]]
- [[Rugosidade pela função]]
- [[06-materiais/index|Materiais]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
