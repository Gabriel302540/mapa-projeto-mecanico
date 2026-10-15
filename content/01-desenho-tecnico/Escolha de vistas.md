---
title: Escolha de vistas
tags: [desenho-tecnico, vistas]
fontes: [ABNT NBR 10067:1995, ISO 128-30 e ISO 128-34, French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de projeções ortográficas), Silva et al. Desenho Técnico Moderno (cap. de vistas)]
status: rascunho
---

**Resumo:** escolher vistas é decidir quantas e quais projeções mostrar para que a peça fique definida sem ambiguidade e sem excesso. Inclui as simplificações aceitas pela norma: vistas parciais, vistas locais, peças interrompidas e meia vista de peças simétricas.

## O que é

A [[Projeções ortográficas|projeção ortográfica]] oferece seis vistas, mas um bom desenho usa **o mínimo necessário**. Escolher vistas envolve três decisões:

1. **Qual é a vista principal (frontal).**
2. **Quantas vistas adicionais** são realmente necessárias.
3. **Quais simplificações** usar para economizar espaço sem perder informação.

### Simplificações aceitas

| Recurso | O que é | Quando usar |
|---|---|---|
| **Vista parcial** | Só uma parte da vista, limitada por linha à mão livre ou ziguezague | Quando só uma região da vista acrescenta informação |
| **Vista local** | Desenho só de um elemento (um rasgo, um furo) na posição da vista correspondente, ligado à vista principal por linha de centro | Rasgos de chaveta, furos isolados em eixos |
| **Peça interrompida (vista encurtada)** | Retira-se um trecho longo e uniforme; as partes restantes são aproximadas e limitadas por linhas de interrupção | Eixos, tubos, perfis e barras longas de seção constante |
| **Meia vista ou quarto de vista** | Desenha-se só metade (ou um quarto) de uma peça simétrica; o eixo de simetria recebe dois traços curtos paralelos em cada ponta | Flanges, tampas, peças simétricas grandes |
| **Elementos repetidos** | Desenha-se um ou dois elementos e indica-se o número total na cota ("12× Ø18") | Furações de flange, dentes, aletas |
| **Vista fora de posição** | Vista desenhada longe da posição normal, identificada por seta com letra na vista principal e por "VISTA A" | Quando falta espaço na posição normal |

**Importante:** numa peça interrompida, a **cota é do comprimento total real**, mesmo com o desenho encurtado.

## Por que importa no projeto

- **Vistas demais criam contradições.** A mesma medida aparece em duas vistas, alguém revisa uma e esquece a outra.
- **Vistas de menos geram dúvida.** Uma peça desenhada só de frente pode ter vários formatos possíveis na profundidade.
- **Simplificações deixam o desenho grande legível.** Um eixo de 4 m desenhado interrompido cabe em escala maior, mostrando melhor os ressaltos e rasgos.

## Como aplicar (passo a passo / regras práticas)

1. **Vista frontal = a que mais mostra a forma**, com menos arestas ocultas, na posição de fabricação ou de montagem.
2. **Teste de ambiguidade:** cubra as outras vistas e pergunte "só com estas, consigo imaginar mais de uma peça diferente?". Se sim, falta vista.
3. **Peças de revolução (eixos, buchas, polias):** uma vista basta, com símbolos Ø nas cotas. Acrescente vistas locais ou cortes transversais para rasgos e furos.
4. **Peças planas (chapas cortadas):** uma vista com nota de espessura ("CHAPA # 12,5 mm").
5. **Peças prismáticas:** normalmente duas ou três vistas, preferindo cortes a vistas cheias de tracejadas. Ver [[Cortes e seções]].
6. **Faces inclinadas:** use [[Vistas auxiliares]] em vez de cotar formas deformadas.
7. **Interrompa peças longas** e cote o comprimento total.

## Norma relacionada

- **ABNT NBR 10067:1995**: vistas, vistas parciais e locais, peças interrompidas, representação de peças simétricas. ⚠️ verificar edição vigente.
- **ISO 128-30** (convenções básicas para vistas) e **ISO 128-34** (vistas em desenho mecânico). ⚠️ verificar se a ISO 128-34 foi incorporada às partes novas da ISO 128.

## Exemplo prático

**Situação:** desenho de fabricação de um **eixo de acionamento** com 3200 mm de comprimento, ressaltos para rolamentos, um rasgo de chaveta em cada ponta e um furo de centro em cada extremidade.

| Decisão | Justificativa |
|---|---|
| **Uma vista principal**, eixo na horizontal | Peça de revolução; é a posição no torno |
| **Vista interrompida** no trecho central liso (por exemplo, 2000 mm sem detalhes) | Permite usar 1:5 em vez de 1:10, dobrando o tamanho dos detalhes |
| **Seções transversais** nos rasgos de chaveta | Mostram a profundidade do rasgo, que não aparece na vista longitudinal |
| **Detalhes ampliados** (2:1) dos raios de concordância e dos furos de centro | Elementos pequenos e críticos para fadiga e fabricação |
| **Cota total 3200** escrita normalmente | Mesmo com o desenho interrompido |

> [!question] Exercício 1
>
> Uma flange circular tem 8 furos iguais distribuídos num círculo, um furo central e um rebaixo na face. Quantas vistas são necessárias e quais?
>
> > [!success]- Resolução
> >
> > **Duas:** uma vista frontal (olhando a face da flange), que mostra o contorno circular, o círculo de furação e a posição dos 8 furos, e uma **vista lateral em corte** (meio corte ou corte total) pelo centro, que mostra a espessura, o furo central e a profundidade do rebaixo. Como a flange é simétrica, a vista frontal pode até ser feita como meia vista. Os furos são cotados uma vez só: "8× Ø18 EQS" sobre o círculo de furação.

> [!question] Exercício 2
>
> Por que, numa vista interrompida, a cota do comprimento total é escrita com o valor real, mesmo que o desenho esteja visivelmente "encurtado"?
>
> > [!success]- Resolução
> >
> > Porque a **cota sempre informa a medida real da peça**, nunca a do desenho. A interrupção é só um recurso gráfico para economizar espaço; quem fabrica precisa do comprimento verdadeiro. O mesmo raciocínio vale para as [[Escalas]].

## Erros comuns

- **Desenhar as três vistas por hábito**, mesmo em eixos e chapas.
- **Vista frontal na posição errada**, por exemplo um eixo na vertical.
- **Peça interrompida com cota do trecho desenhado** em vez do comprimento real.
- **Esquecer os traços de simetria** em meia vista, o que faz parecer que a peça termina ali.
- **Vista fora de posição sem identificação** (sem seta e letra).

## Ver também

- [[Projeções ortográficas]]
- [[Vistas auxiliares]]
- [[Cortes e seções]]
- [[Cotagem]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
