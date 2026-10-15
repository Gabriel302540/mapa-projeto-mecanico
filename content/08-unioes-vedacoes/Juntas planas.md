---
title: Juntas planas
tags: [vedacoes, flanges]
fontes: [ASME Seção VIII Div. 1 Apêndice 2 (projeto de flanges — fatores m e y), ASME B16.5 (flanges de tubulação), ASME B16.20 (juntas metálicas), EN 1591-1 (cálculo de uniões flangeadas) ⚠️ verificar, Bickford An Introduction to the Design and Behavior of Bolted Joints (cap. de juntas)]
status: rascunho
---

**Resumo:** juntas planas vedam a união entre duas faces (flanges, tampas, carcaças), preenchendo as irregularidades entre elas. Para vedar, a junta precisa ser primeiro "assentada" com uma pressão mínima e, em operação, manter uma pressão residual maior que a pressão do fluido. Isso define a força mínima dos parafusos e o acabamento das faces.

## O que é

### Tipos

| Tipo | Aplicação |
|---|---|
| **Papelão hidráulico / fibras comprimidas** | Uso geral, água, óleo, vapor de baixa pressão |
| **Borracha** (NBR, EPDM) | Pressões baixas, tampas, flanges de baixa pressão |
| **PTFE** (puro ou expandido) | Produtos químicos; tende a fluir sob carga (fluência) |
| **Grafite flexível** | Temperaturas altas, vapor |
| **Espiralada metálica** (fita metálica + enchimento) | Pressões e temperaturas altas, flanges de tubulação (ASME B16.20) |
| **Anel metálico (*ring joint*)** | Pressões muito altas |
| **Juntas líquidas** (silicones, anaeróbicos) | Faces usinadas de carcaças, tampas de redutores |

### Fatores de projeto (método ASME, simplificado)

- **y — tensão de assentamento:** pressão mínima sobre a junta para que ela preencha as irregularidades.
- **m — fator de manutenção:** a pressão residual na junta em operação deve ser pelo menos $m$ vezes a pressão do fluido.

Forças mínimas dos parafusos (para uma junta de diâmetro efetivo $G$ e largura efetiva $b$):

$$
W_{m2} = \pi\,b\,G\,y \qquad \text{(assentamento)}
$$
$$
W_{m1} = \underbrace{\frac{\pi}{4}\,G^2\,P}_{H} + \underbrace{2\pi\,b\,G\,m\,P}_{H_p} \qquad \text{(operação)}
$$

A força total dos parafusos deve ser **maior que o maior dos dois**. Os valores de $m$ e $y$ são tabelados por tipo de junta. ⚠️ verificar no código ASME ou no fabricante (métodos mais modernos usam outros parâmetros, como na EN 1591).

### Acabamento das faces

Juntas macias precisam de alguma rugosidade para "agarrar" e não escorregar; juntas metálicas precisam de faces mais lisas. Flanges com face ressaltada (RF) costumam ter **acabamento ranhurado espiral** com Ra da ordem de 3,2–6,3 µm. ⚠️ verificar na ASME B16.5 e com o fabricante da junta.

## Por que importa no projeto

- **Vazamentos em flanges e tampas** quase sempre vêm de força de parafuso insuficiente, aperto desigual ou junta inadequada.
- **Tampas de carcaças** com faces usinadas e juntas líquidas exigem planeza e rigidez da tampa.
- **Fluência (relaxação)** de juntas macias reduz a pré-carga com o tempo; reaperto pode ser necessário.

## Como aplicar (passo a passo / regras práticas)

1. **Escolha a junta** pelo fluido, pressão e temperatura.
2. **Calcule a força mínima** de parafusos para assentar e para operar.
3. **Dimensione os parafusos** e a pré-carga com margem (ver [[Uniões parafusadas]]).
4. **Especifique o acabamento** e a planeza das faces.
5. **Defina o procedimento de aperto:** sequência cruzada em várias etapas (por exemplo, 30 %, 60 %, 100 % do torque, e uma volta final de conferência).
6. **Use juntas novas** a cada montagem.

## Norma relacionada

- **ASME Seção VIII Div. 1, Apêndice 2**: projeto de flanges com fatores m e y.
- **ASME B16.5**: flanges de tubulação e acabamento de faces.
- **ASME B16.20**: juntas metálicas (espiraladas, ring joint).
- **EN 1591-1**: cálculo de uniões flangeadas com juntas. ⚠️ verificar.

## Exemplo prático

**Situação:** flange com junta de fibras comprimidas, diâmetro efetivo **G = 150 mm**, largura efetiva **b = 8 mm**, pressão de **1 MPa**. Valores adotados (ilustrativos ⚠️): **y = 11 MPa**, **m = 2**.

- Assentamento: $W_{m2} = \pi \times 8 \times 150 \times 11 \approx 41{,}5$ kN
- Operação: $H = \dfrac{\pi}{4} \times 150^2 \times 1 \approx 17{,}7$ kN; $H_p = 2\pi \times 8 \times 150 \times 2 \times 1 \approx 15{,}1$ kN → $W_{m1} \approx 32{,}8$ kN
- **Força mínima total: 41,5 kN** (assentamento governa). Com 4 parafusos: ≈ 10,4 kN cada, no mínimo. Parafusos M12 8.8 com pré-carga de ≈ 37 kN (75 % da carga de prova de 84,3 × 580 ≈ 49 kN) dão margem confortável, mesmo considerando a dispersão do aperto.

> [!question] Exercício
>
> Por que o aperto dos parafusos de um flange deve ser feito em sequência cruzada e em etapas?
>
> > [!success]- Resolução
> >
> > Para **comprimir a junta por igual**. Se um parafuso for apertado todo de uma vez, o flange inclina, a junta é esmagada de um lado e fica frouxa do outro, e os parafusos apertados depois "aliviam" os primeiros (interação elástica). A sequência cruzada em etapas distribui a carga de forma uniforme.

## Erros comuns

- **Reutilizar juntas** já comprimidas.
- **Aperto desigual** ou sem sequência.
- **Junta inadequada** à temperatura ou ao fluido.
- **Face do flange muito lisa** para junta macia (escorrega) ou muito rugosa para junta metálica.
- **Ignorar a relaxação** de juntas de PTFE e borracha.

## Ver também

- [[Uniões parafusadas]]
- [[O-rings]]
- [[Rugosidade pela função]]
- [[08-unioes-vedacoes/index|Índice do módulo 08]]
