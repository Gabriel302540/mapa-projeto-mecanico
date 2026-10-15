---
title: Correias e correntes
tags: [elementos, transmissao]
fontes: [ISO 4184 (correias em V clássicas e estreitas), ISO 5292 (cálculo de transmissões por correias em V) ⚠️ verificar, ISO 606 (correntes de rolos), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 17 — elementos mecânicos flexíveis), catálogos técnicos de correias e correntes]
status: rascunho
---

**Resumo:** correias e correntes transmitem potência entre eixos afastados. Correias em V são silenciosas, absorvem choques e funcionam por atrito (com algum deslizamento); correntes de rolos são sincronizadas, suportam torques altos em rotações baixas e ambientes quentes, mas precisam de lubrificação e têm variação de velocidade (efeito poligonal).

## O que é

### Correias em V

- **Perfis:** clássicos (Z, A, B, C, D) e estreitos (SPZ, SPA, SPB, SPC; maior capacidade para a mesma largura).
- **Funcionamento:** a cunha da correia no canal da polia multiplica a força normal e, portanto, o atrito.
- **Relação de tensões** (correias planas, equação de Euler; nas em V, o atrito efetivo é maior):

$$
\frac{F_1}{F_2} = e^{\mu\theta}
$$

- **Comprimento da correia** (polias de diâmetros $D$ e $d$, distância entre centros $C$):

$$
L \approx 2C + \frac{\pi(D + d)}{2} + \frac{(D - d)^2}{4C}
$$

- **Ângulo de abraçamento na polia menor:**

$$
\theta = 180° - 2\arcsin\!\left(\frac{D - d}{2C}\right)
$$

**Seleção (roteiro de catálogo):**

1. Potência de projeto $P_d = P \times f_s$ (fator de serviço pelo tipo de máquina e horas).
2. Perfil pelo gráfico potência × rotação da polia menor.
3. Diâmetros das polias (respeitando o diâmetro mínimo do perfil) e relação.
4. Distância entre centros e comprimento padronizado da correia.
5. Potência por correia (tabela) × fatores de correção de comprimento e de ângulo de abraçamento.
6. Número de correias = $P_d$ / potência corrigida por correia (arredondar para cima).

### Correntes de rolos

- **Normalizadas pela ISO 606** (série europeia "B" e série americana "A"), designadas pelo passo (por exemplo, 16B: passo de 25,4 mm).
- **Simples, dupla, tripla** (múltiplas carreiras).
- **Efeito poligonal:** a corrente envolve a roda como um polígono, o que faz a velocidade oscilar. A variação diminui com mais dentes: use **pelo menos 17 dentes** na roda menor (19 a 21 em rotações maiores), de preferência número ímpar.
- **Comprimento em número de passos** (deve ser inteiro, de preferência par, para evitar elo de redução):

$$
L_p = \frac{2C}{p} + \frac{z_1 + z_2}{2} + \frac{p\,(z_2 - z_1)^2}{4\pi^2 C}
$$

- **Lubrificação** conforme a velocidade: manual, gotejamento, banho ou jato. É decisiva para a vida.

### Comparação

| Critério | Correia em V | Corrente de rolos |
|---|---|---|
| Sincronismo | Não (desliza ~1–2 %) | Sim |
| Absorção de choques | Boa | Baixa |
| Rotação | Média e alta | Baixa e média |
| Torque em rotação baixa | Limitado | Alto |
| Lubrificação | Não precisa | Precisa |
| Ambiente quente, úmido ou oleoso | Sensível | Tolerante (com lubrificação adequada) |
| Ruído | Baixo | Maior |

## Por que importa no projeto

- **Acionamentos de transportadores, bombas, ventiladores e misturadores** usam correias; **transportadores de arraste, esteiras e acionamentos lentos e pesados** usam correntes.
- **Tensão inicial** errada em correias causa deslizamento (pouca tensão) ou sobrecarga nos rolamentos (muita tensão).
- **Alinhamento das polias e rodas dentadas** define a vida.

## Como aplicar (passo a passo / regras práticas)

1. Escolha entre correia e corrente pela rotação, torque, ambiente e necessidade de sincronismo.
2. Siga o roteiro de seleção do catálogo (fator de serviço, perfil ou passo, número de correias ou carreiras).
3. Verifique a **carga radial** nas pontas de eixo (motor, redutor). Ver [[Redutores]].
4. Preveja **ajuste de tensão** (base deslizante do motor, esticador).
5. Especifique proteções (NR-12). Ver [[09-metodologia-de-projeto/index|Metodologia de projeto]].

## Norma relacionada

- **ISO 4184**: correias em V clássicas e estreitas (comprimentos).
- **ISO 5292**: cálculo de potência de transmissões por correia em V. ⚠️ verificar.
- **ISO 606**: correntes de rolos de precisão e rodas dentadas.

## Exemplo prático

**Situação:** transmissão por correias em V entre um motor (polia de **125 mm**) e um ventilador (polia de **315 mm**), com distância entre centros de **600 mm**.

- Relação: $315/125 = 2{,}52$
- Comprimento: $L \approx 2 \times 600 + \dfrac{\pi(315 + 125)}{2} + \dfrac{(315 - 125)^2}{4 \times 600} \approx 1200 + 691{,}2 + 15{,}0 \approx 1906$ mm → escolher o comprimento padronizado mais próximo e recalcular $C$.
- Ângulo de abraçamento: $\theta = 180° - 2\arcsin\!\left(\dfrac{190}{1200}\right) \approx 161{,}8°$ → aplicar o fator de correção de abraçamento do catálogo (pouco abaixo de 1).

> [!question] Exercício
>
> Uma corrente de passo 25,4 mm liga rodas de 19 e 57 dentes, com distância entre centros de 762 mm. Quantos passos deve ter a corrente?
>
> > [!success]- Resolução
> >
> > $\dfrac{2C}{p} = \dfrac{2 \times 762}{25{,}4} = 60$
> > $\dfrac{z_1 + z_2}{2} = \dfrac{19 + 57}{2} = 38$
> > $\dfrac{p(z_2 - z_1)^2}{4\pi^2 C} = \dfrac{25{,}4 \times 38^2}{4\pi^2 \times 762} = \dfrac{36\,678}{30\,083} \approx 1{,}22$
> > $L_p \approx 60 + 38 + 1{,}22 = 99{,}2$ → usar **100 passos** (par) e recalcular a distância entre centros (ou prever esticador).

## Erros comuns

- **Polia menor que o diâmetro mínimo** do perfil (a correia aquece e trinca).
- **Misturar correias novas e velhas** no mesmo jogo.
- **Corrente sem lubrificação** ou com número de dentes muito pequeno.
- **Ignorar a carga radial** nos mancais do motor.

## Ver também

- [[Redutores]]
- [[Acoplamentos]]
- [[Molas helicoidais]] (tensores)
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
