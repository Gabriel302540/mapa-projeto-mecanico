---
title: "Cotagem: furos, raios, chanfros e roscas"
tags: [desenho-tecnico, cotagem]
fontes: [ABNT NBR 10126:1987, ISO 129-1, ISO 6410-1, DIN 6885-1, French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de cotagem), Telecurso 2000 Leitura e Interpretação de Desenho Técnico Mecânico]
status: rascunho
---

**Resumo:** elementos comuns de peças mecânicas (diâmetros, raios, chanfros, furos, furações em círculo, roscas, rasgos de chaveta) têm formas próprias de cotagem, com símbolos que encurtam o desenho e evitam ambiguidade. Esta nota reúne as convenções e os casos práticos mais frequentes.

## O que é

### Símbolos antes do valor da cota

| Símbolo | Significado | Exemplo |
|---|---|---|
| **Ø** | Diâmetro | Ø50 |
| **R** | Raio | R5 |
| **SØ** | Diâmetro de esfera | SØ30 |
| **SR** | Raio de esfera | SR15 |
| **□** | Quadrado (lado) | □40 |
| **⌒** (sobre o valor) | Comprimento de arco | ⌒120 |
| **t =** ou **#** | Espessura de chapa | t = 6,3 |

O símbolo Ø é usado mesmo quando o círculo aparece desenhado, sempre que a cota for de diâmetro. Isso permite cotar uma peça de revolução numa única vista.

### Raios

- A linha de cota parte do centro (ou da direção dele) e tem **uma seta só**, encostada no arco.
- Se o centro estiver muito longe, a linha de cota pode ser quebrada em ziguezague, com o centro deslocado.
- **Raios iguais e pequenos** podem ser indicados numa nota geral ("RAIOS NÃO COTADOS R3").

### Chanfros

- Chanfro a 45°: "2 × 45°" (cateto × ângulo). Algumas normas e empresas usam "C2" para o mesmo chanfro. ⚠️ verificar a notação admitida na ISO 129-1 e no padrão da empresa.
- Chanfro com ângulo diferente de 45°: cote o comprimento e o ângulo separadamente.
- Notas gerais resolvem os casos repetitivos: "QUEBRAR CANTOS VIVOS 0,5 × 45°".

### Furos

| Caso | Como cotar |
|---|---|
| Furo passante | Ø e posição do centro |
| Furo cego | Ø × profundidade (a profundidade é a da parte cilíndrica, sem a ponta cônica da broca) |
| Furo com rebaixo (para cabeça de parafuso Allen) | Ø do furo, Ø do rebaixo e profundidade do rebaixo |
| Furo escareado (para parafuso de cabeça chata) | Ø do furo, Ø externo do escareado e ângulo (90° é o comum) |
| Vários furos iguais | Número de furos × diâmetro: "6× Ø18" |
| Furação em círculo | Diâmetro do círculo de furação (linha traço e ponto) e "n× Øx EQS" (*equally spaced*, igualmente espaçados) ou os ângulos entre furos |

Existem símbolos gráficos para profundidade, rebaixo e escareado, muito usados em desenhos no padrão americano. ⚠️ verificar se a ISO 129-1 e a empresa os adotam.

### Roscas

- **Rosca métrica de passo grosso:** "M20" (o passo grosso é implícito; para M20 é 2,5 mm).
- **Passo fino:** "M20 × 1,5".
- **Classe de tolerância:** "M20 × 1,5 - 6g" (rosca externa) ou "-6H" (rosca interna). 6g/6H é a classe média, a mais usada.
- **Rosca à esquerda:** acrescentar "LH".
- **Comprimento:** cota-se o comprimento de **rosca útil** (completa). Em furo cego roscado, cotam-se também o diâmetro e a profundidade do furo de broca.
- **Furo de broca para rosca métrica** (regra prática): $D_{\text{broca}} \approx d - P$. Para M20 (P = 2,5): 17,5 mm. Para M12 (P = 1,75): 10,2 mm (arredondado para broca comercial).

A representação gráfica das roscas está em [[Representação de roscas]].

### Rasgos de chaveta

A profundidade do rasgo **não** é cotada a partir da superfície do eixo, porque ela é curva e a medição seria imprecisa. Cota-se:

- **No eixo:** a distância do fundo do rasgo até a geratriz oposta do eixo, ou seja, $d - t_1$.
- **No cubo:** a distância do fundo do rasgo até a geratriz oposta do furo, ou seja, $d + t_2$.

Assim, a medição é feita com paquímetro ou micrômetro diretamente sobre duas superfícies.

## Por que importa no projeto

- **Símbolos padronizados eliminam vistas.** Com Ø, um eixo inteiro é cotado numa vista só.
- **Cotar como se mede.** O rasgo de chaveta é o exemplo clássico: a cota $d - t_1$ é a que o inspetor consegue medir.
- **Furações em círculo** mal cotadas geram flanges que não montam no par.

## Como aplicar (passo a passo / regras práticas)

1. **Diâmetros em vista longitudinal**, não no círculo, sempre que possível (menos poluição na vista circular).
2. **Raios no arco**, com uma seta e o símbolo R.
3. **Furos:** prefira cotá-los na vista em que aparecem como círculo (posição) e no corte (profundidade).
4. **Furações em círculo:** cote o diâmetro do círculo de furação na vista frontal e escreva "n× Øx EQS". Se um furo tiver de ficar alinhado com algo (um rasgo, um eixo de simetria), cote o ângulo desse furo.
5. **Roscas:** use a designação completa (tipo, diâmetro, passo se fino, classe). Em furos cegos, cote também o furo de broca e sua profundidade.
6. **Rasgos de chaveta:** cote largura (com tolerância), comprimento e a medida $d - t_1$ (eixo) ou $d + t_2$ (cubo).

## Norma relacionada

- **ABNT NBR 10126:1987**: cotagem, incluindo raios, diâmetros e elementos especiais. ⚠️ verificar se continua vigente.
- **ISO 129-1**: indicação de dimensões e símbolos.
- **ISO 6410-1**: designação e representação de roscas no desenho.
- **DIN 6885-1**: dimensões de chavetas paralelas e rasgos. ⚠️ verificar a norma de chavetas adotada (ISO, DIN ou ABNT).

## Exemplo prático

**Situação:** ponta de um eixo de Ø50 mm que recebe o cubo de um acoplamento, com chaveta paralela.

Para a faixa de diâmetro de 44 a 50 mm, tabelas de chavetas paralelas indicam chaveta 14 × 9, profundidade no eixo $t_1 = 5{,}5$ mm e no cubo $t_2 = 3{,}8$ mm. ⚠️ verificar na DIN 6885-1 ou na norma adotada.

- **Cota no eixo:** $50 - 5{,}5 = 44{,}5$ mm (do fundo do rasgo à geratriz oposta).
- **Cota no cubo:** $50 + 3{,}8 = 53{,}8$ mm (do fundo do rasgo à geratriz oposta do furo).
- **Largura do rasgo:** 14 mm, com tolerância conforme o tipo de ajuste da chaveta (por exemplo, N9 no eixo e JS9 no cubo para ajuste normal). Ver [[02-tolerancias-ajustes/index|Tolerâncias e ajustes]].

> [!question] Exercício 1
>
> Como cotar 8 furos de Ø22 igualmente espaçados num círculo de Ø300 mm, com o primeiro furo alinhado com o eixo vertical de simetria?
>
> > [!success]- Resolução
> >
> > - Desenhe o **círculo de furação** em traço e ponto e cote **Ø300** sobre ele.
> > - Escreva **"8× Ø22 EQS"** com linha de chamada para um dos furos.
> > - Como o primeiro furo fica sobre o eixo vertical, a posição angular fica definida pelo próprio eixo de simetria (e o espaçamento é $360°/8 = 45°$). Se o primeiro furo estivesse defasado, seria preciso cotar o ângulo, por exemplo 22,5° em relação ao eixo vertical.

> [!question] Exercício 2
>
> Um furo cego deve receber uma rosca M16 com 24 mm de rosca útil. Qual broca usar e que profundidade de furo indicar, considerando 6 mm a mais para a saída da ferramenta?
>
> > [!success]- Resolução
> >
> > - Passo grosso do M16: $P = 2$ mm.
> > - Broca: $16 - 2 = 14$ mm.
> > - Profundidade do furo (parte cilíndrica): $24 + 6 = 30$ mm.
> > - Indicação: **"M16 × 24 / Ø14 × 30"** (rosca útil de 24 mm, furo de broca Ø14 com 30 mm de profundidade).

## Erros comuns

- **Cotar a profundidade do rasgo de chaveta a partir da superfície do eixo.**
- **Esquecer o símbolo Ø**, deixando dúvida se a cota é de diâmetro.
- **Raio cotado com duas setas** ou com o valor do diâmetro.
- **Furo cego sem profundidade** ou com profundidade incluindo a ponta cônica.
- **Rosca sem classe de tolerância** em peças que serão compradas de terceiros.
- **Furação em círculo sem referência angular** quando a orientação importa.

## Ver também

- [[Cotagem]]
- [[Representação de roscas]]
- [[Cortes e seções]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
