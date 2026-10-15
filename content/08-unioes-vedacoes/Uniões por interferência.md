---
title: Uniões por interferência
tags: [unioes, eixo-cubo]
fontes: [DIN 7190-1 (uniões por interferência — cálculo) ⚠️ verificar, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 3 — cilindros de parede grossa; cap. 7 — ajustes de interferência), Norton Projeto de Máquinas (cap. de eixos), Niemann Elementos de Máquinas (cap. de uniões eixo-cubo)]
status: rascunho
---

**Resumo:** numa união por interferência, o eixo é maior que o furo do cubo; depois de montados, a pressão de contato entre eles transmite torque e força axial por atrito, sem chaveta. A pressão é calculada pelas equações de Lamé para cilindros de parede grossa, a partir da interferência e da geometria. Verifica-se que a interferência mínima transmite a carga e que a máxima não sobrecarrega o cubo.

## O que é

### Pressão de contato (Lamé)

Para eixo maciço e cubo do **mesmo material** (módulo $E$), diâmetro de contato $d$, diâmetro externo do cubo $d_o$ e interferência **diametral** $\delta$:

$$
p = \frac{E\,\delta}{2\,d}\left(\frac{d_o^2 - d^2}{d_o^2}\right)
$$

Para materiais diferentes ou eixo vazado, usa-se a forma geral:

$$
p = \frac{\delta}{d\left[\dfrac{1}{E_o}\left(\dfrac{d_o^2 + d^2}{d_o^2 - d^2} + \nu_o\right) + \dfrac{1}{E_i}\left(\dfrac{d^2 + d_i^2}{d^2 - d_i^2} - \nu_i\right)\right]}
$$

### Capacidade de transmissão

$$
T = \frac{\pi\,\mu\,p\,d^2\,L}{2} \qquad\qquad F_{\text{axial}} = \pi\,\mu\,p\,d\,L
$$

com $L$ o comprimento de contato e $\mu$ o coeficiente de atrito (≈ 0,1–0,15 em montagem por prensa com lubrificação; ≈ 0,15–0,2 ou mais em montagem térmica a seco). ⚠️ verificar na DIN 7190 ou referência adotada.

### Tensão no cubo

A tensão tangencial (de tração) no furo do cubo é a maior:

$$
\sigma_t = p\,\frac{d_o^2 + d^2}{d_o^2 - d^2}
$$

Ela deve ficar abaixo do escoamento do cubo (com margem), e é crítica em **cubos de ferro fundido** (frágil).

### Efeito da rugosidade

Na montagem, os picos da rugosidade são amassados, e a interferência efetiva fica menor que a medida. Desconta-se uma parcela proporcional à rugosidade (ver [[Rugosidade pela função]]).

### Montagem

Prensagem (força axial ≈ $F_{\text{axial}}$ calculado com o atrito de montagem), aquecimento do cubo ou resfriamento do eixo (nitrogênio líquido). Ver [[Tipos de ajuste]] para a temperatura de montagem. Em uniões grandes, a **injeção de óleo** sob pressão permite montar e desmontar.

## Por que importa no projeto

- **Transmite torques altos** em pouco espaço, sem enfraquecer o eixo com rasgo de chaveta.
- **Não afrouxa** com vibração.
- **Coroas, cubos de acoplamentos pesados, buchas permanentes, rodas** são montados assim.
- **Desvantagens:** desmontagem difícil, concentração de tensão na borda do cubo (fadiga por *fretting* no eixo), sensibilidade às tolerâncias.

## Como aplicar (passo a passo / regras práticas)

1. Escolha um ajuste (H7/s6, H7/u6...) e calcule $\delta_{\min}$ e $\delta_{\max}$ (ver [[Tipos de ajuste]]).
2. Desconte o efeito da rugosidade.
3. Calcule $p_{\min}$ e verifique se $T$ e $F_{\text{axial}}$ atendem, com segurança.
4. Calcule $p_{\max}$ e verifique $\sigma_t$ no cubo (e a pressão no eixo).
5. Calcule a força de prensagem ou a temperatura de montagem.
6. Arredonde a borda do cubo ou aumente o diâmetro do eixo na região do cubo para reduzir a concentração de tensão.

## Norma relacionada

- **DIN 7190-1**: cálculo de uniões por interferência (método alemão completo). ⚠️ verificar.
- **ISO 286**: ajustes. Ver [[Ajustes recomendados]].

## Exemplo prático

**Situação:** cubo de aço montado a quente num eixo de **Ø80** com ajuste **H7/s6** (interferência de 29 a 78 µm; ver [[Tipos de ajuste]]). Cubo com $d_o$ = 160 mm, $L$ = 80 mm, $E$ = 207 GPa, $\mu$ = 0,15. (Sem descontar a rugosidade, para simplificar.)

| | $\delta$ = 0,029 mm (mínima) | $\delta$ = 0,078 mm (máxima) |
|---|---|---|
| $p = \dfrac{207\,000\,\delta}{160} \times 0{,}75$ | ≈ 28 MPa | ≈ 76 MPa |
| $T = \dfrac{\pi \times 0{,}15 \times p \times 80^2 \times 80}{2}$ | ≈ **3,4 kN·m** | ≈ 9,1 kN·m |
| $\sigma_t = p \times \dfrac{160^2 + 80^2}{160^2 - 80^2}$ | ≈ 47 MPa | ≈ **126 MPa** |

- **Torque garantido** (interferência mínima): ≈ 3,4 kN·m. Para um torque de serviço de 2 kN·m, o coeficiente de segurança contra deslizamento é ≈ 1,7.
- **Tensão máxima no cubo**: ≈ 126 MPa, confortável para um cubo de aço; num cubo de ferro fundido cinzento, seria preocupante.

> [!question] Exercício
>
> No exemplo, o que acontece com o torque transmissível se o comprimento do cubo dobrar? E se o diâmetro externo do cubo aumentar muito (cubo "infinito")?
>
> > [!success]- Resolução
> >
> > - **L × 2:** o torque **dobra** ($T \propto L$).
> > - **$d_o \to \infty$:** o fator $(d_o^2 - d^2)/d_o^2$ tende a 1 (era 0,75), então a pressão aumenta cerca de 33 %, e o torque também. Ou seja, aumentar muito o cubo tem retorno limitado; comprimento e interferência têm mais efeito.

## Erros comuns

- **Calcular com a interferência máxima** (o torque garantido vem da mínima).
- **Esquecer a rugosidade**, superestimando a pressão.
- **Interferência alta em cubo de ferro fundido.**
- **Borda do cubo em canto vivo** sobre o eixo (fadiga por fretting).

## Ver também

- [[Tipos de ajuste]]
- [[Chavetas]]
- [[Acoplamentos]]
- [[08-unioes-vedacoes/index|Índice do módulo 08]]
