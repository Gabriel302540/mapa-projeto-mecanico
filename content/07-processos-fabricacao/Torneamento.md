---
title: Torneamento
tags: [fabricacao, usinagem]
fontes: [Diniz, Marcondes e Coppini Tecnologia da Usinagem dos Materiais (caps. de torneamento e parâmetros de corte), Ferraresi Fundamentos da Usinagem dos Metais, Kalpakjian e Schmid Manufacturing Engineering and Technology (cap. de torneamento), Machinery's Handbook (seção de velocidades e avanços), catálogos técnicos de ferramentas de metal duro]
status: rascunho
---

**Resumo:** no torneamento, a peça gira e uma ferramenta de corte avança ao longo dela, gerando superfícies de revolução: cilindros, cones, faces, roscas, canais. É o processo básico para eixos, buchas, flanges e pinos. Os parâmetros de corte (velocidade, avanço e profundidade) definem a produtividade, o acabamento e a potência necessária.

## O que é

### Operações

- **Cilindragem** (diâmetros externos), **faceamento** (faces planas), **sangramento** (cortar ou fazer canais), **torneamento cônico**, **perfilamento**, **rosqueamento**, **furação e mandrilamento** no centro da peça.

### Fixação

| Fixação | Uso |
|---|---|
| Placa de 3 castanhas (universal) | Peças cilíndricas curtas; centraliza automaticamente |
| Placa de 4 castanhas independentes | Peças irregulares ou que exigem centragem fina |
| **Entre pontas** | Eixos: garante concentricidade entre os diâmetros, porque todos são feitos com a mesma referência (os furos de centro) |
| Placa + ponta | Eixos médios |
| **Luneta** (fixa ou móvel) | Eixos longos e esbeltos (L/D acima de ≈ 10–12), para evitar flexão e vibração |

### Parâmetros de corte

| Parâmetro | Símbolo | Unidade | Relação |
|---|---|---|---|
| Velocidade de corte | $v_c$ | m/min | $v_c = \dfrac{\pi\,D\,n}{1000}$ |
| Rotação | $n$ | rpm | $n = \dfrac{1000\,v_c}{\pi\,D}$ |
| Avanço | $f$ | mm/volta | Define o acabamento: $Ra \approx 0{,}032\,f^2/r$ |
| Profundidade de corte | $a_p$ | mm | Desbaste: alta; acabamento: baixa |
| Taxa de remoção | $Q$ | cm³/min | $Q = v_c\,f\,a_p$ |
| Potência de corte | $P_c$ | kW | $P_c = \dfrac{v_c\,f\,a_p\,k_c}{60\,000}$ |

$k_c$ é a **força específica de corte** (N/mm²): da ordem de 1500 a 2500 para aços, menor para ferros fundidos e alumínio. ⚠️ verificar no catálogo da ferramenta para o material e o avanço.

**Velocidades de corte de referência** (metal duro revestido): aços de baixo e médio carbono, ≈ 150–300 m/min; aços ligados beneficiados, ≈ 100–200 m/min; inox austenítico, ≈ 100–200 m/min; ferro fundido cinzento, ≈ 150–300 m/min. Ferramentas de aço rápido (HSS) usam velocidades cerca de 5 a 10 vezes menores. ⚠️ verificar no catálogo.

### Tolerâncias e acabamento típicos

Desbaste: IT11–IT13, Ra 6,3–25. Acabamento: IT7–IT9, Ra 0,8–3,2. Ver [[Tolerâncias por processo]] e [[Rugosidade por processo]].

## Por que importa no projeto

- **Eixos e peças de revolução** são desenhados pensando no torno: posição horizontal, furos de centro nas pontas, diâmetros escalonados acessíveis.
- **Concentricidade:** todos os diâmetros que precisam girar juntos devem, de preferência, ser usinados **na mesma fixação** (ou entre pontas).
- **Peças grandes** (eixos de vários metros, rolos) exigem tornos grandes e lunetas; o projetista deve conhecer a capacidade disponível (diâmetro sobre o barramento, distância entre pontas, peso).

## Como aplicar (passo a passo / regras práticas)

1. **Preveja furos de centro** normalizados nas pontas dos eixos (e especifique se podem ou não permanecer na peça).
2. **Use raios e chanfros compatíveis** com os insertos padrão (raios de ponta de 0,4; 0,8; 1,2; 1,6 mm).
3. **Canais de saída de rosca e de rebolo** onde houver rosca ou retificação junto a um ressalto.
4. **Evite paredes muito finas** em buchas longas (deformam na placa).
5. **Indique as superfícies de referência** (assentos de rolamento) e as tolerâncias de batimento em relação a elas.

## Norma relacionada

- **ISO 6411** (furos de centro — representação) e **DIN 332** (dimensões de furos de centro). ⚠️ verificar.
- **ISO 1832**: designação de insertos intercambiáveis.
- **ISO 3685**: ensaio de vida de ferramentas de tornear. (Os dados de corte práticos vêm dos catálogos.)

## Exemplo prático

**Situação:** desbastar um eixo de **SAE 4140 beneficiado** de Ø100 com inserto de metal duro.

- $v_c$ = 180 m/min → $n = \dfrac{1000 \times 180}{\pi \times 100} \approx 573$ rpm
- $f$ = 0,3 mm/volta; $a_p$ = 3 mm
- $Q = 180 \times 0{,}3 \times 3 = 162$ cm³/min
- Com $k_c \approx 2000$ N/mm²: $P_c = \dfrac{180 \times 0{,}3 \times 3 \times 2000}{60\,000} = 5{,}4$ kW (o motor do torno precisa de margem para o rendimento, ≈ 7 kW)

No acabamento, com $f$ = 0,15 e raio de ponta 0,8: $Ra \approx 0{,}032 \times 0{,}15^2/0{,}8 \approx 0{,}9$ µm (teórico).

> [!question] Exercício
>
> Um eixo de Ø250 deve ser torneado a $v_c$ = 150 m/min. Qual a rotação? E se o diâmetro fosse 25 mm, com a mesma velocidade de corte?
>
> > [!success]- Resolução
> >
> > - Ø250: $n = 1000 \times 150/(\pi \times 250) \approx 191$ rpm.
> > - Ø25: $n \approx 1910$ rpm.
> >
> > A rotação é inversamente proporcional ao diâmetro: peças grandes giram devagar.

## Erros comuns

- **Eixos longos sem luneta**, com vibração e conicidade.
- **Diâmetros concêntricos usinados em fixações diferentes** sem controle de batimento.
- **Esquecer os furos de centro** em eixos que serão retificados.
- **Raios no desenho incompatíveis com ferramentas** padrão.

## Ver também

- [[Fresamento]]
- [[Furação e mandrilamento]]
- [[Tolerâncias por processo]]
- [[Rugosidade por processo]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
