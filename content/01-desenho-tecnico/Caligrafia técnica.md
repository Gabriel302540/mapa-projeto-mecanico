---
title: Caligrafia técnica
tags: [desenho-tecnico, escrita]
fontes: [ABNT NBR 16861:2020, ISO 3098-1, ABNT NBR 8402 (histórica), French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de letreiros)]
status: rascunho
---

**Resumo:** a escrita em desenho técnico (cotas, notas, legenda) segue uma forma padronizada de letras e algarismos, com alturas de uma série fixa. O objetivo é um só: que qualquer pessoa leia cada número sem chance de confusão, mesmo numa cópia reduzida ou suja de óleo.

## O que é

**Caligrafia técnica** é o conjunto de regras para letras, algarismos e sinais escritos no desenho. Ela define:

- **A forma dos caracteres:** simples, sem enfeites, com traços de espessura constante. Normalmente se usa a **escrita tipo B**, vertical ou inclinada a 75°.
- **A altura nominal $h$:** altura das letras maiúsculas e dos algarismos, escolhida numa série normalizada.
- **As proporções:** espessura do traço, altura das minúsculas, espaço entre caracteres e entre linhas, todas como frações de $h$.

### Série de alturas

As alturas seguem a mesma progressão de razão $\sqrt{2}$ dos [[Formatos de folha|formatos]] e das [[Tipos de linha|larguras de linha]]:

$$
h = 2{,}5 \;\to\; 3{,}5 \;\to\; 5 \;\to\; 7 \;\to\; 10 \;\to\; 14 \;\to\; 20\ \text{mm}
$$

Isso garante que, ao reduzir um desenho de A1 para A3, um texto de 5 mm vire 2,5 mm, que continua sendo um valor da série e, portanto, legível.

### Proporções da escrita tipo B

| Grandeza | Relação com $h$ | Para $h = 3{,}5$ mm |
|---|---|---|
| Altura das maiúsculas e algarismos | $h$ | 3,5 mm |
| Altura das minúsculas (sem haste) | $0{,}7\,h$ | 2,5 mm |
| Espessura do traço | $h/10$ | 0,35 mm |
| Espaço mínimo entre caracteres | $0{,}2\,h$ | 0,7 mm |
| Espaço mínimo entre linhas (base a base) | $1{,}4\,h$ | 5 mm |

⚠️ verificar as proporções na NBR 16861 / ISO 3098-1. A escrita tipo A, mais estreita, usa traço de $h/14$.

Repare que a espessura do traço de um texto de 3,5 mm (0,35 mm) coincide com uma largura de linha normalizada. Em CAD, isso define a espessura de plotagem dos textos.

## Por que importa no projeto

- **Números confundíveis geram peça errada.** "1" e "7", "3" e "8", "5" e "6", "0" e "6" se confundem facilmente em letra corrida ou em fonte decorativa. Uma cota de 18 lida como 13 é um erro de 5 mm.
- **Cópias reduzidas.** Desenhos A1 circulam em A3. Um texto de 2,5 mm no original vira 1,25 mm na cópia, abaixo do legível.
- **Padrão da equipe.** Fontes e alturas iguais em todos os desenhos deixam o arquivo técnico com cara de um só autor, o que facilita a leitura.

## Como aplicar (passo a passo / regras práticas)

1. **Altura mínima de cotas e notas: 3,5 mm** em A0 a A2; 2,5 mm é aceitável em A3 e A4. ⚠️ verificar os mínimos na norma.
2. **Título na legenda:** 5 ou 7 mm. **Número do desenho:** 7 ou 10 mm, para ser lido de longe no arquivo.
3. **Use maiúsculas** em títulos e notas. Minúsculas só onde a norma exige (por exemplo, símbolos de tolerância como `g6`, `H7`, e unidades como `mm`).
4. **Em CAD, use uma fonte técnica de traço simples** (como a ISOCP ou equivalente) e crie **estilos de texto** para cada altura. Não use fontes decorativas.
5. **Vírgula decimal:** no Brasil, escreve-se 12,5 e não 12.5. Desenhos para o exterior podem usar ponto, mas nunca misture os dois no mesmo desenho.
6. **Notas gerais** ficam agrupadas, numeradas, perto da legenda ("NOTAS: 1. Quebrar cantos vivos 0,5 × 45°. 2. ...").
7. **Nunca sobreponha texto a linhas** do desenho. Se não houver espaço, use uma linha de chamada.

## Norma relacionada

- **ABNT NBR 16861:2020**: requisitos de linhas **e escrita**. ⚠️ verificar se substituiu formalmente a NBR 8402 (*Execução de caracteres para escrita em desenho técnico*), que trazia as mesmas regras.
- **ISO 3098** (série): escrita em documentação técnica de produto. A parte 1 trata dos requisitos gerais.

## Exemplo prático

**Situação:** uma prancha A1 de arranjo de uma transmissão (motor, redutor, acoplamentos) vai ser impressa em A3 para a equipe de montagem.

- Redução linear de A1 para A3: $\dfrac{420}{841} \approx 0{,}5$.
- Cotas de 3,5 mm no A1 → 1,75 mm no A3: no limite da leitura.
- Cotas de 5 mm no A1 → 2,5 mm no A3: legíveis.

**Decisão:** em pranchas grandes que certamente serão reduzidas, use cotas de **5 mm**. Em desenhos de fabricação A3/A4, que são impressos no tamanho real, 3,5 mm basta.

## Erros comuns

- **Texto pequeno demais** porque "no monitor dá para ler". O zoom do CAD engana.
- **Fontes TrueType decorativas** ou em negrito, que entopem na impressão.
- **Misturar vírgula e ponto decimal.**
- **Alturas diferentes para a mesma função** (cotas com 2,5, 3 e 3,5 mm no mesmo desenho), quase sempre resultado de escalar o texto à mão no CAD.

## Ver também

- [[Tipos de linha]]
- [[Cotagem]]
- [[Legenda]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
