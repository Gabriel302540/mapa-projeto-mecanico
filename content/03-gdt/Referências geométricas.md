---
title: Referências (datums)
tags: [gdt, referencias]
fontes: [ISO 5459:2011, ISO 1101:2017, ASME Y14.5-2018, Henzold Geometrical Dimensioning and Tolerancing for Design, Manufacturing and Inspection (cap. de referências)]
status: rascunho
---

**Resumo:** referências (datums) são elementos ideais — planos, eixos, pontos — estabelecidos a partir de superfícies reais da peça, que servem de "zero" para medir orientação, posição e batimento. A ordem das referências (primária, secundária, terciária) reproduz a forma como a peça é apoiada e travada na montagem.

## O que é

### Elemento de referência × referência

- **Elemento de referência (*datum feature*):** a superfície **real** da peça, imperfeita, indicada no desenho por um triângulo com uma letra.
- **Referência (*datum*):** o elemento **ideal** (plano, eixo, ponto) obtido a partir dela, na prática pelo contato com uma superfície de máquina, mesa de desempeno, mandril ou dispositivo.

Uma face levemente empenada apoiada num desempeno define como plano de referência o plano do desempeno, que toca os pontos altos da face.

### Indicação

Um **triângulo** (cheio ou vazio) ligado a um quadrado com a letra maiúscula. Assim como no quadro de tolerância:

- Triângulo **na superfície** (ou na linha auxiliar, afastado da cota): a referência é a superfície (um **plano**).
- Triângulo **alinhado com a linha de cota** de um diâmetro ou largura: a referência é o **eixo** do cilindro ou o **plano médio**.

### Sistema de referências (3-2-1)

Uma peça no espaço tem 6 graus de liberdade (3 translações e 3 rotações). Para travá-la completamente:

| Referência | Contato típico (plano) | Graus de liberdade travados |
|---|---|---|
| **Primária (A)** | 3 pontos | 3 (uma translação e duas rotações) |
| **Secundária (B)** | 2 pontos | 2 |
| **Terciária (C)** | 1 ponto | 1 |

Por isso a **ordem** no quadro importa: a peça encosta primeiro em A (com mais contato), depois desliza até encostar em B, e por último em C. Mudar a ordem muda a posição da peça no dispositivo e, portanto, a medição.

Para peças cilíndricas, é comum usar um **eixo** como referência primária (que trava 4 graus de liberdade) e uma face como secundária.

### Referências comuns e alvos

- **Referência comum (A–B):** um eixo definido por dois elementos ao mesmo tempo, por exemplo os dois munhões de um eixo apoiados em dois blocos em V. Escrita "A–B" num único compartimento do quadro.
- **Alvos de referência (*datum targets*):** pontos, linhas ou pequenas áreas específicas da superfície que serão usadas como apoio. Úteis em peças fundidas, forjadas ou soldadas, cuja superfície é irregular demais para apoiar inteira.

## Por que importa no projeto

- **Projetista, fabricante e inspetor medem do mesmo jeito.** Sem referências claras, cada um apoia a peça de uma forma e obtém resultados diferentes.
- **As referências devem imitar a montagem.** Se a peça monta apoiada numa face e centralizada num diâmetro, essas devem ser as referências A e B.
- **Também orientam a fabricação:** o torneiro e o fresador procuram usinar a peça fixando-a pelas mesmas superfícies.

## Como aplicar (passo a passo / regras práticas)

1. **Pergunte como a peça é montada:** onde ela apoia (primária), o que a centraliza ou alinha (secundária), o que impede a rotação (terciária).
2. **Escolha elementos estáveis e acessíveis:** faces usinadas grandes, diâmetros de encaixe.
3. **Controle a forma das referências** (planeza da face A, cilindricidade do eixo B), porque uma referência ruim contamina todas as medições.
4. **Em eixos com dois mancais**, use a **referência comum A–B** dos assentos dos rolamentos: é o eixo real de rotação.
5. **Em peças brutas**, use alvos de referência.

## Norma relacionada

- **ISO 5459:2011**: referências e sistemas de referência para especificações geométricas.
- **ISO 1101:2017**: uso das referências nos quadros de tolerância.

## Exemplo prático

**Situação:** um **eixo de rolo** gira apoiado em dois mancais de rolamento. Os assentos dos rolamentos ficam nas duas extremidades; entre eles há o corpo do rolo e, numa ponta, o assento do acoplamento.

- **A:** assento do rolamento lado acionamento (eixo do cilindro).
- **B:** assento do rolamento lado oposto (eixo do cilindro).
- **A–B:** referência comum, o eixo de rotação real.
- O batimento do corpo do rolo, do assento do acoplamento e das faces de encosto é especificado em relação a **A–B**.
- Na inspeção, o eixo é apoiado em **dois blocos em V** (ou em dois rolamentos de inspeção) sob os assentos A e B, e o relógio comparador mede o batimento.

> [!question] Exercício
>
> Uma flange é aparafusada apoiando-se na face posterior e centralizada por um ressalto cilíndrico de Ø120 h7. Os furos dos parafusos devem ser controlados por posição. Quais seriam as referências primária e secundária, e por quê?
>
> > [!success]- Resolução
> >
> > - **Primária (A): a face posterior** de apoio, porque é o que a flange encosta primeiro e trava a inclinação.
> > - **Secundária (B): o eixo do ressalto Ø120**, que centraliza a flange.
> >
> > O quadro dos furos ficaria: ⌖ | Ø… Ⓜ | A | B. Uma terciária só seria necessária se a posição angular dos furos importasse em relação a algum outro elemento (um pino, um rasgo).

## Erros comuns

- **Escolher referências pela conveniência da medição** e não pela montagem.
- **Usar como referência uma superfície bruta** (fundida, cortada a plasma) sem alvos de referência.
- **Inverter a ordem** primária e secundária.
- **Referência de eixo único** num eixo apoiado em dois mancais, em vez da referência comum A–B.

## Ver também

- [[Quadro de tolerância]]
- [[Batimento]]
- [[Tolerâncias de localização]]
- [[03-gdt/index|Índice do módulo 03]]
