---
title: Formatos e folhas de desenho
tags: [desenho-tecnico, folha]
fontes: [ABNT NBR 16752:2020, ISO 216, ISO 5457, Silva et al. Desenho Técnico Moderno (cap. de normalização), Provenza Desenhista de Máquinas (cap. de folhas e formatos)]
status: rascunho
---

**Resumo:** desenhos técnicos são feitos em folhas de tamanho padronizado, da série A (A0 a A4). A norma define o tamanho de cada folha, as margens, o quadro e onde fica a legenda, para que qualquer desenho possa ser impresso, dobrado e arquivado do mesmo jeito.

## O que é

**Formato** é o tamanho da folha. No Brasil e na maior parte do mundo usa-se a **série A** da ISO 216. Ela foi pensada a partir de duas regras simples:

1. A folha **A0** tem área de $1\ \text{m}^2$.
2. A proporção entre o lado maior e o menor é sempre $\sqrt{2} \approx 1{,}414$.

A consequência da segunda regra é elegante: **cortar uma folha ao meio, no lado maior, gera a folha seguinte da série com a mesma proporção**. Uma A1 cortada ao meio dá duas A2, uma A2 dá duas A3, e assim por diante. Por isso um desenho pode ser reduzido de A1 para A2 na impressora e continuar "encaixado" na folha.

Por que $\sqrt{2}$? Se a folha tem lados $a$ (maior) e $b$ (menor), e queremos que a metade dela (lados $b$ e $a/2$) tenha a mesma proporção:

$$
\frac{a}{b} = \frac{b}{a/2} \quad\Rightarrow\quad a^2 = 2b^2 \quad\Rightarrow\quad \frac{a}{b} = \sqrt{2}
$$

Com área de $1\ \text{m}^2$ ($a \cdot b = 1$) e $a = \sqrt{2}\, b$, resulta $b \approx 0{,}841\ \text{m}$ e $a \approx 1{,}189\ \text{m}$, que são exatamente as medidas da A0.

| Formato | Dimensões (mm) | Área aproximada |
|---|---|---|
| A0 | 841 × 1189 | 1 m² |
| A1 | 594 × 841 | 0,5 m² |
| A2 | 420 × 594 | 0,25 m² |
| A3 | 297 × 420 | 0,125 m² |
| A4 | 210 × 297 | 0,0625 m² |

Além do tamanho, a folha de desenho tem **elementos gráficos fixos**:

- **Margem:** faixa em branco entre a borda do papel e o quadro. A margem esquerda é maior, porque é ali que a folha é furada ou presa em pasta.
- **Quadro (moldura):** linha contínua larga que delimita a área útil do desenho.
- **Legenda:** o "carimbo" no canto inferior direito, com a identificação do desenho. Ver [[Legenda]].
- **Marcas de centro e de dobra:** pequenos traços nas bordas que ajudam a centralizar a cópia e a dobrar a folha.
- **Sistema de referência por zonas (opcional):** letras e números nas bordas, como num mapa, para localizar detalhes ("ver zona C4").

## Por que importa no projeto

- **Arquivo e consulta:** uma empresa grande tem milhares de desenhos. Se cada um tivesse tamanho e legenda em lugares diferentes, encontrar o número do desenho ou a revisão seria lento e sujeito a erro.
- **Impressão e redução:** por causa da proporção $\sqrt{2}$, imprimir um A1 numa folha A3 dá uma redução exata de 50 % em escala linear, sem cortar nada. Na oficina é comum circular a cópia reduzida.
- **Dobra padronizada:** desenhos grandes são dobrados até o tamanho A4 com a legenda visível por fora, para caber em pastas e no arquivo técnico.
- **Escolha consciente:** usar uma folha maior do que o necessário dificulta o manuseio no chão de fábrica. Usar uma folha pequena demais força uma escala muito reduzida e deixa o desenho ilegível.

## Como aplicar (passo a passo / regras práticas)

1. **Defina a vista principal e a escala primeiro.** O formato é consequência do tamanho da peça na escala escolhida, e não o contrário. Ver [[Escalas]].
2. **Estime a área ocupada.** Some o espaço das vistas, dos cortes, das cotas (as cotas "abrem" o desenho em uns 20 a 30 mm para cada lado) e das notas.
3. **Escolha o menor formato que acomode tudo com folga**, sem sobrepor a legenda.
4. **Use a folha na horizontal (paisagem)** para A0 a A3. A A4 normalmente é usada na vertical (retrato). ⚠️ verificar na NBR 16752 as posições admitidas para cada formato.
5. **Respeite as margens e a legenda do modelo da empresa.** Em CAD, isso vem pronto no *template* da folha. Ver [[10-cad/index|CAD]].
6. **Para desenhos com várias folhas**, use o mesmo formato em todas, quando possível, e numere "folha 1 de 3" na legenda.

## Norma relacionada

- **ABNT NBR 16752:2020**, *Desenho técnico: requisitos para apresentação em folhas de desenho*. Reúne formato da folha, elementos gráficos, posição da legenda, dobramento de cópias e emprego de escalas. É a referência atual e substituiu a NBR 10582. ⚠️ verificar se também cancelou a NBR 10068 (folha de desenho: leiaute e dimensões) e a NBR 13142 (dobramento de cópias); fontes secundárias indicam que sim, mas não foi possível confirmar no catálogo da ABNT.
- **ISO 216**: define as dimensões da série A.
- **ISO 5457**: equivalente internacional para o leiaute da folha de desenho (margens, quadro, marcas).

**Valores de margem — atenção.** Materiais didáticos baseados na NBR 16752 citam margem esquerda de 20 mm e demais margens de 10 mm em todos os formatos A, com legenda de 180 mm de largura. A norma antiga (NBR 10068) usava margem esquerda de 25 mm e demais margens de 10 mm (A0, A1) ou 7 mm (A2 a A4), e muitas apostilas ainda trazem esses números. ⚠️ verificar os valores na NBR 16752 e no *template* oficial da empresa antes de criar uma folha nova.

## Exemplo prático

**Situação:** detalhar o **eixo de um rolo de moenda**. Em uma moenda de 42" × 84" (diâmetro nominal da camisa de cerca de 1067 mm e comprimento de cerca de 2134 mm), o eixo completo, com as pontas de mancal e a ponta de acionamento, passa facilmente de 4 m de comprimento. Os números são apenas para ordem de grandeza.

Vamos supor um eixo de 4500 mm de comprimento e diâmetro máximo de 600 mm.

| Escala | Comprimento no papel | Cabe em |
|---|---|---|
| 1:5 | 900 mm | Não cabe nem em A1 (largura útil ≈ 811 mm) |
| 1:10 | 450 mm | A2 (largura útil ≈ 564 mm) com boa folga para cotas |
| 1:20 | 225 mm | A3, mas os detalhes ficariam pequenos demais |

A largura útil foi estimada como lado maior menos as margens de 20 mm e 10 mm.

**Decisão típica:** vista principal em **1:10 numa folha A2**, com **detalhes ampliados** (rasgo de chaveta, raio de concordância nos ressaltos, centros) em 1:2 ou 1:1, desenhados na mesma folha e identificados como "Detalhe A — escala 1:2". Assim a folha continua fácil de manusear na oficina e os pontos críticos, onde se concentram as tensões e as falhas por fadiga, ficam legíveis.

## Erros comuns

- **Escolher a folha antes da escala** e depois "espremer" o desenho numa escala não normalizada (1:7, 1:15).
- **Desenhar por cima da legenda** ou colar notas e tabelas fora do quadro.
- **Usar margens de modelos antigos** misturadas com modelos novos na mesma empresa, o que gera cópias que não fecham na dobra.
- **Imprimir "ajustado à página"** sem avisar: a escala real deixa de ser a escrita na legenda. Na cópia reduzida, sempre anote "cópia reduzida, não medir".
- **Dobrar com a legenda para dentro:** quem procura o desenho no arquivo precisa abrir cada um.

## Ver também

- [[Legenda]]
- [[Escalas]]
- [[Tipos de linha]] (o quadro é feito com linha contínua larga)
- [[01-desenho-tecnico/index|Índice do módulo 01]]
