---
title: "Eixos: dimensionamento estático"
tags: [elementos, eixos]
fontes: [Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 5 — falhas por carregamento estático; cap. 7 — eixos), Norton Projeto de Máquinas (cap. de eixos), Niemann Elementos de Máquinas (cap. de eixos), DIN 743-1]
status: rascunho
---

**Resumo:** um eixo de transmissão sofre flexão (das forças de engrenagens, polias e pesos) e torção (do torque transmitido). O dimensionamento estático verifica se o eixo não escoa sob a maior carga, combinando as tensões por um critério de falha (von Mises ou Tresca). Também se verificam deflexões e ângulos, que costumam limitar o eixo antes da resistência. Na maioria dos eixos girantes, porém, quem manda é a fadiga.

## O que é

### Esforços num eixo de transmissão

1. **Torque** $T$, a partir da potência e da rotação:
$$
T = \frac{P}{\omega} = \frac{60\,P}{2\pi n} \qquad\Rightarrow\qquad T\,[\text{N·m}] \approx \frac{9550\,P\,[\text{kW}]}{n\,[\text{rpm}]}
$$
2. **Momento fletor** $M$: das forças nos elementos montados (forças tangenciais e radiais de engrenagens, tração de correias, peso de rotores), calculado com o eixo como viga apoiada nos mancais. Fazem-se os diagramas nos dois planos (vertical e horizontal) e combina-se: $M = \sqrt{M_V^2 + M_H^2}$.
3. **Força axial**: de engrenagens helicoidais e cônicas, normalmente pequena em tensão.

### Tensões numa seção circular maciça

$$
\sigma = \frac{32\,M}{\pi d^3} \qquad\qquad \tau = \frac{16\,T}{\pi d^3}
$$

### Critérios de falha (materiais dúcteis)

**Von Mises (energia de distorção)** — o mais usado:

$$
\sigma' = \sqrt{\sigma^2 + 3\tau^2} = \frac{16}{\pi d^3}\sqrt{4M^2 + 3T^2} \le \frac{S_y}{n}
$$

**Tresca (máxima tensão de cisalhamento)** — mais conservador:

$$
\frac{32}{\pi d^3}\sqrt{M^2 + T^2} \le \frac{S_y}{n}
$$

Isolando o diâmetro (von Mises):

$$
d = \left[\frac{16\,n}{\pi S_y}\sqrt{4M^2 + 3T^2}\right]^{1/3}
$$

### Rigidez: deflexão e ângulo

Um eixo pode resistir e mesmo assim falhar na função por flexionar demais. Limites típicos (ordens de grandeza):

| Grandeza | Limite típico |
|---|---|
| Ângulo no rolamento rígido de esferas | 0,001 a 0,003 rad |
| Ângulo no rolamento de rolos cilíndricos | 0,0005 a 0,001 rad |
| Ângulo no rolamento autocompensador | bem maior; ver catálogo |
| Deflexão na engrenagem cilíndrica | cerca de 0,01 a 0,13 mm, conforme o módulo |
| Ângulo de torção | cerca de 0,25° a 1° por metro, conforme a aplicação |

⚠️ verificar no catálogo do rolamento e na literatura; os valores dependem da aplicação.

**Ângulo de torção:** $\theta = \dfrac{T L}{G J}$, com $J = \pi d^4/32$ e $G \approx 79$ GPa para aço.

### Velocidade crítica

Eixos com massas grandes (rotores, volantes) têm uma rotação em que a vibração entra em ressonância. Recomenda-se operar abaixo de cerca de metade da primeira velocidade crítica, ou bem acima dela com cuidado especial.

## Por que importa no projeto

- **Sobrecargas de partida e de travamento:** num acionamento que trava (embuchamento, entupimento), o torque pode chegar a 2 ou 3 vezes o nominal. A verificação estática deve usar esse pico.
- **Eixos longos e pesados** (rolos, cilindros) costumam ser dimensionados por **rigidez**, não por resistência.
- **Primeira estimativa rápida:** o critério estático dá um diâmetro mínimo de partida para o cálculo à fadiga.

## Como aplicar (passo a passo / regras práticas)

1. **Croqui** do eixo com mancais, elementos montados e forças.
2. **Torque** pela potência e rotação (incluir fator de serviço ou de pico).
3. **Reações nos mancais e diagramas de momento** nos dois planos; momento resultante.
4. **Identifique seções críticas:** onde $M$ é alto e há concentradores (ressaltos, rasgos, canais). Ver [[Concentradores de tensão]].
5. **Diâmetro estático** pelo critério de von Mises com o torque e o momento de pico.
6. **Verifique a fadiga** (normalmente determinante). Ver [[Fadiga de eixos]].
7. **Verifique deflexões e ângulos** nos mancais e engrenagens.
8. **Escolha diâmetros comerciais** e compatíveis com rolamentos (múltiplos de 5 mm acima de 20 mm, em geral).

## Norma relacionada

- **DIN 743** (partes 1 a 4): cálculo da capacidade de carga de eixos e árvores. Muito usada na Europa.
- Os critérios de falha vêm da **mecânica dos materiais**; não há norma ISO única para o dimensionamento de eixos.

## Exemplo prático

**Situação:** eixo de aço SAE 1045 ($S_y \approx 530$ MPa ⚠️ verificar) transmite **75 kW a 300 rpm**. Na seção do ressalto do mancal, o momento fletor é **3000 N·m**. Coeficiente de segurança estático $n = 2$.

1. Torque: $T = 9550 \times 75/300 = 2387{,}5$ N·m.
2. Diâmetro estático (von Mises):
$$
d = \left[\frac{16 \times 2}{\pi \times 530}\sqrt{4(3{,}0\times10^6)^2 + 3(2{,}39\times10^6)^2}\right]^{1/3} \approx 52\ \text{mm}
$$
(momentos em N·mm).

Esse valor é só o mínimo **estático**. O mesmo eixo, verificado à fadiga na nota [[Fadiga de eixos]], precisa de cerca de **88 mm**. A flexão rotativa alterna a tensão a cada volta, e isso é muito mais severo.

> [!question] Exercício
>
> Um eixo maciço de Ø60 transmite 1500 N·m e sofre um momento fletor de 1200 N·m. Calcule a tensão equivalente de von Mises e o coeficiente de segurança estático para $S_y = 400$ MPa.
>
> > [!success]- Resolução
> >
> > - $\sigma = \dfrac{32 \times 1{,}2\times10^6}{\pi \times 60^3} = \dfrac{3{,}84\times10^7}{678\,584} \approx 56{,}6$ MPa
> > - $\tau = \dfrac{16 \times 1{,}5\times10^6}{\pi \times 60^3} \approx 35{,}4$ MPa
> > - $\sigma' = \sqrt{56{,}6^2 + 3 \times 35{,}4^2} = \sqrt{3204 + 3759} \approx 83{,}4$ MPa
> > - $n = 400/83{,}4 \approx 4{,}8$

## Erros comuns

- **Dimensionar só pela torção** e esquecer a flexão.
- **Usar o torque nominal** na verificação estática, ignorando picos de partida e travamento.
- **Parar no cálculo estático** em eixos girantes, sem verificar a fadiga.
- **Ignorar a rigidez** em eixos longos.
- **Esquecer o rasgo de chaveta** e os ressaltos nas seções críticas.

## Ver também

- [[Fadiga de eixos]]
- [[Concentradores de tensão]]
- [[Chavetas]]
- [[Seleção de rolamentos]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
