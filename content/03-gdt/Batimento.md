---
title: Batimento circular e total
tags: [gdt, batimento]
fontes: [ISO 1101:2017, ISO 5459:2011, Henzold Geometrical Dimensioning and Tolerancing for Design, Manufacturing and Inspection, catálogos técnicos de rolamentos e acoplamentos (seções de montagem e alinhamento)]
status: rascunho
---

**Resumo:** batimento é a variação lida por um relógio comparador encostado numa superfície enquanto a peça gira 360° em torno de um eixo de referência. É a tolerância mais natural para peças que giram, porque mede exatamente o que a máquina "sente": excentricidade e erros de forma combinados. O batimento circular é medido seção por seção; o total, varrendo a superfície inteira.

## O que é

| Símbolo | Característica | Como se mede | O que controla |
|---|---|---|---|
| ↗ | **Batimento circular** | Relógio parado numa posição; peça gira uma volta; repete-se em várias seções | Em cada seção: circularidade + coaxialidade (radial) ou oscilação axial (face) |
| ⌰ | **Batimento total** | Relógio desliza ao longo de toda a superfície enquanto a peça gira | Toda a superfície: cilindricidade + coaxialidade (radial) ou planeza + perpendicularidade (face) |

### Radial e axial

- **Radial:** o relógio fica perpendicular ao eixo, sobre uma superfície cilíndrica. Mede o "bater" do diâmetro.
- **Axial (de face):** o relógio fica paralelo ao eixo, sobre uma face. Mede o "empeno" ou a oscilação da face.

### Leitura

O valor do batimento é a **diferença entre a maior e a menor leitura** do relógio (leitura total do indicador, TIR ou FIM). Atenção: se um diâmetro está excêntrico de $e$ (distância entre o centro real e o eixo de rotação), o batimento radial lido é aproximadamente:

$$
\text{batimento} \approx 2e
$$

Um batimento de 0,10 mm corresponde a uma excentricidade de cerca de 0,05 mm.

### Referência

Quase sempre é o **eixo de rotação real** da peça: a referência comum **A–B** dos dois assentos de mancal. Ver [[Referências geométricas]]. Em fabricação, o eixo também pode ser referenciado pelos **furos de centro** (pontas do torno), desde que eles sejam coerentes com os assentos.

## Por que importa no projeto

- **Vibração e desbalanceamento:** um rotor com batimento gera força centrífuga proporcional à excentricidade e ao quadrado da rotação.
- **Vedações:** retentores e selos mecânicos toleram batimentos pequenos; acima do limite, vazam e desgastam rapidamente. Fabricantes de retentores indicam o batimento admissível em função da rotação. ⚠️ verificar no catálogo.
- **Acoplamentos e polias:** batimento de cubos e polias gera vibração e desalinhamento no acionamento.
- **Faces de encosto de rolamentos:** batimento axial da face inclina o rolamento.
- **Fácil de medir:** blocos em V (ou pontas) e um relógio comparador. Por isso é preferido à coaxialidade na prática.

## Como aplicar (passo a passo / regras práticas)

1. **Defina a referência** pelos assentos dos mancais (A–B).
2. **Aplique batimento radial** nos diâmetros que recebem peças girantes (acoplamentos, engrenagens, polias, rotores, pistas de vedação).
3. **Aplique batimento axial** nas faces de encosto de rolamentos e engrenagens.
4. **Use batimento total** quando o comprimento todo da superfície importa (assentos longos, cilindros de laminação, rolos).
5. **Valor:** conforme a rotação e a função; consulte catálogos de rolamentos, vedações e acoplamentos.

## Norma relacionada

- **ISO 1101:2017**: definição de batimento circular e total.
- **ISO 5459:2011**: referências comuns (A–B).
- Para alinhamento de máquinas montadas (eixos acoplados), há guias e normas específicas de alinhamento; ⚠️ verificar normas e manuais do fabricante.

## Exemplo prático

**Situação:** um **rolo de transporte** (cilindro de 600 mm de diâmetro e 2000 mm de comprimento) gira apoiado em mancais nas pontas do eixo. Deve-se especificar o controle geométrico da superfície do rolo.

- **Referência A–B:** assentos dos rolamentos nas duas pontas do eixo.
- **Batimento total radial** na superfície do rolo:

<span class="fcf"><span>⌰</span><span>0,2</span><span>A–B</span></span>

- **Batimento circular axial** nas faces de encosto dos rolamentos:

<span class="fcf"><span>↗</span><span>0,02</span><span>A–B</span></span>

Com batimento total de 0,2 mm, a excentricidade máxima do rolo é da ordem de 0,1 mm, compatível com um equipamento de transporte de baixa rotação. ⚠️ verificar os valores de acordo com a função e a rotação.

> [!question] Exercício 1
>
> Ao girar um eixo nas pontas, o relógio sobre um assento de engrenagem marca entre −0,03 e +0,05 mm. Qual o batimento e qual a excentricidade aproximada?
>
> > [!success]- Resolução
> >
> > Batimento = $0{,}05 - (-0{,}03) = 0{,}08$ mm. Excentricidade aproximada = $0{,}08/2 = 0{,}04$ mm (se o erro for todo de excentricidade, sem erro de forma).

> [!question] Exercício 2
>
> Por que o batimento circular de uma superfície cilíndrica não garante a sua retitude ao longo do comprimento?
>
> > [!success]- Resolução
> >
> > Porque o batimento **circular** é avaliado **seção por seção**, com o relógio parado em cada posição axial. Uma superfície levemente cônica ou "em barril" pode ter batimento pequeno em cada seção, já que cada círculo é concêntrico ao eixo, mas variar de diâmetro ao longo do comprimento. Para controlar o comprimento todo, usa-se o **batimento total**.

## Erros comuns

- **Referência num único assento** quando o eixo gira em dois mancais.
- **Confundir batimento com excentricidade** (o batimento é o dobro).
- **Medir com a peça apoiada em superfícies diferentes das referências.**
- **Batimento circular quando a função depende da superfície toda** (deveria ser total).

## Ver também

- [[Referências geométricas]]
- [[Tolerâncias de localização]]
- [[Tolerâncias de forma]]
- [[05-elementos-de-maquinas/index|Elementos de máquinas]]
- [[03-gdt/index|Índice do módulo 03]]
