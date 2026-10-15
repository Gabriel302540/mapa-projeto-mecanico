---
title: Quadro de tolerância
tags: [gdt, simbologia]
fontes: [ISO 1101:2017, ISO 5459:2011, ASME Y14.5-2018, Krulikowski Fundamentals of Geometric Dimensioning and Tolerancing (cap. de quadro de controle)]
status: rascunho
---

**Resumo:** toda tolerância geométrica é escrita num quadro retangular dividido em compartimentos: o símbolo da característica, o valor da tolerância (com Ø se a zona for cilíndrica e com modificadores) e as letras das referências, em ordem de prioridade. O quadro é ligado ao elemento controlado por uma linha de chamada com seta.

## O que é

### Estrutura do quadro

O quadro é lido da esquerda para a direita:

<span class="fcf"><span>⌖</span><span>Ø0,1 Ⓜ</span><span>A</span><span>B</span><span>C</span></span>

| Compartimento | Conteúdo | No exemplo |
|---|---|---|
| 1º | **Símbolo da característica** | ⌖ (posição) |
| 2º | **Valor da tolerância**, precedido de Ø se a zona for cilíndrica (ou SØ se esférica), seguido de modificadores | Ø0,1 Ⓜ |
| 3º, 4º, 5º | **Referências** (datums), em ordem de prioridade: primária, secundária, terciária | A, B, C |

### Símbolos das características (ISO 1101)

| Símbolo | Característica | Família | Referência |
|---|---|---|---|
| ⏤ | Retitude | Forma | Não |
| ⏥ | Planeza | Forma | Não |
| ○ | Circularidade | Forma | Não |
| ⌭ | Cilindricidade | Forma | Não |
| ⌒ | Perfil de linha | Forma, orientação ou localização | Opcional |
| ⌓ | Perfil de superfície | Forma, orientação ou localização | Opcional |
| ∥ | Paralelismo | Orientação | Sim |
| ⊥ | Perpendicularidade | Orientação | Sim |
| ∠ | Inclinação (angularidade) | Orientação | Sim |
| ⌖ | Posição | Localização | Em geral sim |
| ◎ | Concentricidade / coaxialidade | Localização | Sim |
| ⌯ | Simetria | Localização | Sim |
| ↗ | Batimento circular | Batimento | Sim |
| ⌰ | Batimento total | Batimento | Sim |

### Modificadores comuns

| Símbolo | Significado |
|---|---|
| Ⓜ | Requisito de máximo material (MMR). Ver [[Requisito de máximo material]] |
| Ⓛ | Requisito de mínimo material (LMR) |
| Ⓟ | Zona de tolerância projetada (acima da superfície, para pinos e parafusos) |
| Ⓕ | Estado livre (peças flexíveis) |
| CZ | Zona combinada (vários elementos dentro de uma zona única) |
| Ⓔ | Envoltória (vai junto da cota de tamanho, não no quadro). Ver [[Independência e envoltória]] |
| [caixa] | Cota teoricamente exata (TED): valor ideal, sem tolerância, que define a posição ou forma teórica |

### Como o quadro aponta para o elemento

Isso muda o significado:

- **Seta na superfície (ou na linha auxiliar, afastada da linha de cota):** a tolerância vale para a **superfície**.
- **Seta alinhada com a linha de cota de um tamanho (diâmetro, largura):** a tolerância vale para o **elemento derivado**: o **eixo** do cilindro ou o **plano médio** da largura.

O mesmo vale para os triângulos de referência (ver [[Referências geométricas]]).

### Cotas teoricamente exatas (TED)

São cotas escritas dentro de uma caixa retangular, como $\boxed{100}$. Elas não têm tolerância própria: definem a posição **ideal** do elemento, e a tolerância geométrica (posição, perfil) define o quanto ele pode se afastar dessa posição ideal. Isso elimina o acúmulo de tolerâncias das cadeias de cotas.

## Por que importa no projeto

- O quadro é uma "frase" precisa: **o que** é controlado, **quanto** e **em relação a quê**.
- Um erro de posição da seta (superfície × eixo) muda completamente a inspeção.
- A ordem das referências define como a peça é apoiada para medir, o que pode mudar o resultado.

## Como aplicar (passo a passo / regras práticas)

1. Escolha a característica pela função (ver [[Por que GD&T]]).
2. Defina se a zona é cilíndrica (Ø) ou entre planos (sem Ø). Eixos e furos controlados em posição normalmente têm zona **Ø**.
3. Escreva o valor e, se fizer sentido, o modificador (Ⓜ para montagem de parafusos e pinos).
4. Liste as referências na ordem em que a peça se apoia na montagem.
5. Aponte a seta para a superfície ou alinhe com a cota, conforme o elemento controlado.
6. Localize com **cotas em caixa** os elementos controlados por posição ou perfil.

## Norma relacionada

- **ISO 1101:2017**: símbolos, quadro e regras de indicação.
- **ISO 5459:2011**: indicação de referências.
- **ASME Y14.5-2018**: usa um quadro equivalente (*feature control frame*). A edição de 2018 eliminou concentricidade e simetria, que a ISO mantém.

## Exemplo prático

**Situação:** a tampa de um mancal tem um furo central de Ø100 H7 (para o retentor) e seis furos passantes Ø14 para os parafusos M12. A tampa apoia na face (A) e centraliza pelo diâmetro externo de encaixe (B).

**Furo central — perpendicularidade em relação à face de apoio:**

<span class="fcf"><span>⊥</span><span>Ø0,03</span><span>A</span></span>

Seta alinhada com a cota Ø100 → controla o **eixo** do furo, dentro de um cilindro de Ø0,03 perpendicular à face A.

**Seis furos de fixação — posição:**

<span class="fcf"><span>⌖</span><span>Ø0,2 Ⓜ</span><span>A</span><span>B</span></span>

Com "6× Ø14" e o círculo de furação em cota teoricamente exata $\boxed{Ø150}$ e ângulos em caixa. Ver [[Tolerâncias de localização]].

> [!question] Exercício
>
> Interprete o quadro abaixo, aplicado a uma face plana de uma peça:
>
> <span class="fcf"><span>∥</span><span>0,05</span><span>A</span></span>
>
> > [!success]- Resolução
> >
> > A face deve estar contida entre **dois planos paralelos afastados de 0,05 mm**, ambos **paralelos à referência A**. Não há Ø, então a zona é entre planos. A referência A é uma superfície indicada por um triângulo em outro lugar da peça.

## Erros comuns

- **Seta na posição errada** (superfície × eixo), mudando o elemento controlado.
- **Ø na frente de tolerância de planeza** (a zona é entre planos, não cilíndrica).
- **Referência em tolerância de forma** (forma nunca tem referência).
- **Cotas de posição com ±** junto com tolerância de posição, gerando dupla tolerância. As cotas de localização devem estar em caixa.

## Ver também

- [[Por que GD&T]]
- [[Referências geométricas]]
- [[Requisito de máximo material]]
- [[Leitura de GD&T]]
- [[03-gdt/index|Índice do módulo 03]]
