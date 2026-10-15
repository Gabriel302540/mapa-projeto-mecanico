---
title: Escalas
tags: [desenho-tecnico, escalas]
fontes: [ABNT NBR 16752:2020, ABNT NBR 8196, ISO 5455, Silva et al. Desenho Técnico Moderno (cap. de normalização), Provenza Desenhista de Máquinas (cap. de escalas)]
status: rascunho
---

**Resumo:** escala é a relação entre o tamanho do desenho e o tamanho real da peça. Usa-se 1:1 quando a peça cabe na folha, redução (1:2, 1:5, 1:10...) para peças grandes e ampliação (2:1, 5:1...) para detalhes pequenos. As cotas são sempre os valores reais, qualquer que seja a escala.

## O que é

A escala é a razão entre uma medida **no desenho** e a medida correspondente **na peça real**:

$$
E = \frac{\text{medida no desenho}}{\text{medida real}}
$$

Ela é escrita como uma razão com um dos lados igual a 1:

| Tipo | Forma | Exemplo | Significado |
|---|---|---|---|
| **Natural** | 1:1 | 1:1 | 10 mm no desenho = 10 mm na peça |
| **Redução** | 1:X | 1:10 | 10 mm no desenho = 100 mm na peça |
| **Ampliação** | X:1 | 5:1 | 10 mm no desenho = 2 mm na peça |

O primeiro número sempre se refere ao **desenho** e o segundo à **peça**.

### Escalas recomendadas

As escalas normalizadas seguem a sequência **1, 2, 5** multiplicada por potências de 10:

- **Ampliação:** 2:1, 5:1, 10:1, 20:1, 50:1
- **Natural:** 1:1
- **Redução:** 1:2, 1:5, 1:10, 1:20, 1:50, 1:100, 1:200, 1:500, 1:1000

Em casos especiais, a série pode ser estendida multiplicando ou dividindo esses valores por 10. Escalas fora da série (1:3, 1:4, 1:15...) devem ser evitadas, porque dificultam a leitura e a verificação com escalímetro. ⚠️ verificar a tabela de escalas na NBR 16752.

### A regra mais importante

**A cota é sempre o valor real.** Um eixo de 600 mm desenhado em escala 1:10 ocupa 60 mm na folha, mas a cota escrita é **600**. A escala muda o desenho, nunca o número da cota. Ângulos não mudam com a escala.

## Por que importa no projeto

- **Faz a peça caber na folha** sem perder legibilidade. A escolha da escala e do formato da folha é feita em conjunto (ver [[Formatos de folha]]).
- **Mostra detalhes pequenos.** Um raio de concordância de 2 mm, um canal de anel elástico ou um rasgo de chaveta não são legíveis em 1:10; num detalhe 2:1 ou 5:1, ficam claros.
- **Dá noção de proporção a quem lê.** Em 1:1, o desenho tem o tamanho da peça, o que ajuda a perceber dimensões e folgas.
- **Evita erros de interpretação.** Ninguém deve medir um desenho com régua para fabricar, mas, num desenho em escala correta, uma cota errada costuma "saltar aos olhos" porque não combina com o tamanho desenhado.

## Como aplicar (passo a passo / regras práticas)

1. **Prefira 1:1** sempre que a peça couber em um formato razoável.
2. **Para escolher a redução**, divida a maior dimensão da peça pela largura útil da folha que você pretende usar e arredonde **para cima** até a próxima escala normalizada.

   $$
   \text{fator mínimo} = \frac{\text{maior dimensão real}}{\text{espaço disponível no papel}}
   $$

   Exemplo: peça de 1300 mm e espaço útil de 380 mm numa A3 → $1300/380 \approx 3{,}4$ → a próxima escala normalizada é **1:5** (1:3 e 1:4 não são recomendadas).
3. **Deixe espaço para as cotas.** Na prática, reserve uns 20 a 30 % a mais do que o contorno da peça.
4. **Detalhes em escala maior:** circule a região na vista principal, identifique com uma letra ("A") e desenhe o "Detalhe A" ampliado na mesma folha, com a escala embaixo (por exemplo, "DETALHE A — ESCALA 2:1").
5. **Indicação:** a escala principal vai na legenda. Se houver mais de uma escala, cada vista ou detalhe recebe a sua logo abaixo, e a legenda indica a principal (ver [[Legenda]]).
6. **Em CAD**, desenhe sempre em 1:1 no espaço do modelo e aplique a escala só na **viewport** do layout. Ajuste textos e cotas com estilos *annotative* para que tenham a mesma altura no papel em qualquer escala. Ver [[10-cad/index|CAD]].

## Norma relacionada

- **ABNT NBR 16752:2020**: inclui o emprego de escalas entre seus requisitos de apresentação em folhas de desenho. ⚠️ verificar a tabela de escalas e as regras de indicação.
- **ABNT NBR 8196** (*Desenho técnico: emprego de escalas*, edição de 1999, baseada na ISO 5455): por muito tempo foi a norma de escalas no Brasil. Fontes indicam que foi **cancelada sem substituição em 2016**, e o assunto passou a ser tratado na NBR 16752. ⚠️ verificar a situação no catálogo da ABNT.
- **ISO 5455**: norma internacional de escalas, com a mesma série 1-2-5.

## Exemplo prático

**Situação 1 — peça grande.** Desenhar a **bagaceira** de uma moenda (a peça curva que conduz o bagaço do rolo de entrada ao rolo de saída), com cerca de 2100 mm de comprimento (largura da moenda) e 700 mm de largura na vista lateral. Valores aproximados, só para o exemplo.

- Folha A1: espaço útil horizontal ≈ 811 mm (841 menos as margens de 20 mm e 10 mm).
- Fator mínimo: $2100 / 811 \approx 2{,}6$ → escala **1:5**.
- Conferência: em 1:5, a peça ocupa $2100/5 = 420$ mm na horizontal, deixando mais de 300 mm para a segunda vista e as cotas. ✔
- Em 1:2 ela ocuparia 1050 mm e não caberia; 1:3 não é escala normalizada.

**Situação 2 — detalhe pequeno.** O **perfil do frisado** de uma camisa de rolo de moenda, com frisos (ranhuras em V) de passo da ordem de 50 mm e ângulo de flanco próximo de 55°. Valores típicos, ⚠️ verificar no desenho da camisa.

- Na vista geral da camisa em 1:10, cada friso teria só 5 mm no papel, ilegível para cotar raio de fundo e ângulo.
- Solução: "DETALHE B — ESCALA 1:1" mostrando dois ou três frisos, com o ângulo, o passo, a profundidade e o raio do fundo cotados.
- A cota do passo continua sendo **50**, tanto na vista geral quanto no detalhe.

## Erros comuns

- **Cotar com o valor medido no papel** em vez do valor real. Num desenho 1:5, escrever "120" para uma peça de 600 mm.
- **Usar escalas fora da série** (1:3, 1:4, 1:15) para "encaixar" o desenho na folha.
- **Imprimir com "ajustar à página"** e manter a escala original na legenda. Na cópia, a escala real fica diferente da escrita.
- **Esquecer a escala dos detalhes**, deixando só a da legenda.
- **Inverter a notação:** escrever 2:1 querendo dizer redução à metade. O primeiro número é sempre o do desenho.
- **Em CAD, desenhar já reduzido** no espaço do modelo. As medidas do arquivo deixam de ser reais e qualquer cota associativa sai errada.

## Ver também

- [[Formatos de folha]]
- [[Legenda]]
- [[Tipos de linha]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
