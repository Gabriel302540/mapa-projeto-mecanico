---
title: Dimensão nominal, desvios e tolerância
tags: [tolerancias, fundamentos]
fontes: [ISO 286-1:2010, ABNT NBR 6158:1995, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. de tolerâncias e ajustes), Agostinho, Rodrigues e Lirani Tolerâncias, Ajustes, Desvios e Análise de Dimensões (cap. 1)]
status: rascunho
---

**Resumo:** nenhuma peça é fabricada com a medida exata. A tolerância é a faixa de variação aceitável em torno da medida desejada. Para falar disso sem ambiguidade, existe um vocabulário próprio: dimensão nominal, dimensões limites, desvios superior e inferior, tolerância e linha zero.

## O que é

### Vocabulário

Considere um eixo especificado como $\varnothing 50^{-0{,}009}_{-0{,}025}$.

| Termo | Definição | No exemplo |
|---|---|---|
| **Dimensão nominal** ($N$) | A medida "de referência", a partir da qual se definem os limites | 50 mm |
| **Desvio superior** ($es$ no eixo, $ES$ no furo) | Diferença entre a dimensão máxima e a nominal | −0,009 mm |
| **Desvio inferior** ($ei$ no eixo, $EI$ no furo) | Diferença entre a dimensão mínima e a nominal | −0,025 mm |
| **Dimensão máxima** | $N + \text{desvio superior}$ | 49,991 mm |
| **Dimensão mínima** | $N + \text{desvio inferior}$ | 49,975 mm |
| **Tolerância** ($IT$, $T$) | Máxima − mínima = desvio superior − desvio inferior. É sempre positiva | 0,016 mm = 16 µm |
| **Dimensão efetiva (real)** | A medida que a peça realmente tem, obtida por medição | por exemplo 49,983 mm |
| **Linha zero** | Linha que representa a dimensão nominal num diagrama de tolerâncias | — |

A peça está **aprovada** se a dimensão efetiva estiver entre a mínima e a máxima (inclusive).

**Convenção de letras:** **minúsculas para eixos** (es, ei; posições a, b, ..., h, ..., z) e **maiúsculas para furos** (ES, EI; A, B, ..., H, ..., Z). "Eixo" e "furo" valem para qualquer elemento externo e interno: a largura de uma chaveta é um "eixo"; a largura do rasgo é um "furo".

### Fórmulas

$$
T = d_{\max} - d_{\min} = es - ei \qquad\text{(eixo)}
$$
$$
T = D_{\max} - D_{\min} = ES - EI \qquad\text{(furo)}
$$

### Diagrama de tolerâncias

O jeito mais claro de visualizar é desenhar a linha zero na horizontal e, acima ou abaixo dela, um retângulo para cada campo de tolerância (altura = tolerância, posição = desvios). Desvio positivo fica acima da linha zero; negativo, abaixo. Esse diagrama é a base para entender os [[Tipos de ajuste]].

### Por que a tolerância é inevitável

Toda máquina e todo processo têm variação: folgas e desgaste do torno, deflexão da peça e da ferramenta, dilatação térmica, desgaste do gume, erro do instrumento de medição. Mesmo que a variação fosse eliminada, **não seria possível provar** que a peça tem a medida exata, porque a medição também tem incerteza.

## Por que importa no projeto

- **Custo:** quanto menor a tolerância, mais cara a peça. Tolerâncias apertadas exigem máquinas melhores, mais passes, retificação, controle de temperatura e inspeção mais demorada. Em termos práticos, o custo cresce muito rápido abaixo de uns 20 µm.
- **Função:** tolerâncias largas demais geram folga excessiva, vibração, vazamentos e desgaste prematuro.
- **Intercambiabilidade:** só com tolerâncias definidas é possível trocar uma peça de reposição sem ajuste manual na montagem. Isso é fundamental para manutenção com peças de estoque.
- **Contrato:** a tolerância define o que é peça boa e peça ruim entre o projetista, o fabricante e o inspetor.

## Como aplicar (passo a passo / regras práticas)

1. **Defina a função** da medida: ela monta com outra peça? Gira? Veda? Ou é só uma medida livre?
2. **Medidas livres** ficam com a tolerância geral do desenho. Ver [[Tolerâncias gerais]].
3. **Medidas funcionais** recebem tolerância própria, de preferência pelo sistema ISO (H7, g6...). Ver [[Graus IT]] e [[Posições de tolerância]].
4. **Escolha a maior tolerância que ainda garanta a função.** Esse é o princípio econômico do projeto.
5. **Pense na inspeção:** a tolerância deve ser pelo menos umas 5 a 10 vezes maior que a incerteza do instrumento que vai medi-la. Um paquímetro com resolução de 0,02 mm não serve para controlar uma tolerância de 16 µm; precisa de micrômetro ou calibrador.

## Norma relacionada

- **ISO 286-1:2010**: sistema ISO de codificação de tolerâncias para dimensões lineares — bases, tolerâncias, desvios e ajustes. Define o vocabulário desta nota.
- **ABNT NBR 6158:1995**: sistema de tolerâncias e ajustes (baseada em versão anterior da ISO 286). ⚠️ verificar edição vigente.

## Exemplo prático

**Situação:** o assento de um rolamento num eixo de transmissão é especificado como **Ø80 k6**. Pela tabela ISO 286-2, para a faixa de 50 a 80 mm: $ei = +0{,}002$ mm e $IT6 = 19$ µm. ⚠️ verificar na ISO 286-2.

- $es = ei + IT6 = +0{,}002 + 0{,}019 = +0{,}021$ mm
- Dimensão máxima: 80,021 mm; mínima: 80,002 mm.
- O torneiro (ou retificador) precisa deixar o diâmetro entre esses valores. Um eixo medido com 80,025 mm é **refugo** (ou retrabalho, se ainda houver material para retirar); um com 79,998 mm é **refugo** (não dá para "pôr material de volta" sem recuperação por metalização ou cromo duro).

> [!question] Exercício 1
>
> Um furo é especificado como $\varnothing 40^{+0{,}039}_{0}$. Quais são as dimensões máxima e mínima, a tolerância e os desvios?
>
> > [!success]- Resolução
> >
> > - $ES = +0{,}039$ mm; $EI = 0$
> > - $D_{\max} = 40{,}039$ mm; $D_{\min} = 40{,}000$ mm
> > - $T = 0{,}039 - 0 = 0{,}039$ mm = 39 µm (é um furo Ø40 H8).

> [!question] Exercício 2
>
> Um eixo deve ter diâmetro entre 29,980 e 29,993 mm, com nominal 30 mm. Escreva a especificação com desvios e calcule a tolerância.
>
> > [!success]- Resolução
> >
> > - $es = 29{,}993 - 30 = -0{,}007$ mm; $ei = 29{,}980 - 30 = -0{,}020$ mm
> > - Especificação: $\varnothing 30^{-0{,}007}_{-0{,}020}$
> > - $T = -0{,}007 - (-0{,}020) = 0{,}013$ mm = 13 µm. É exatamente um **Ø30 g6** (g: $es = -7$ µm; IT6 = 13 µm).

## Erros comuns

- **Confundir desvio com tolerância:** o desvio pode ser negativo; a tolerância nunca.
- **Escrever desvios sem sinal** ou com o maior embaixo.
- **Apertar a tolerância "por segurança"**, sem necessidade funcional. Só aumenta o custo.
- **Especificar uma tolerância menor que a capacidade de medição** disponível.

## Ver também

- [[Graus IT]]
- [[Posições de tolerância]]
- [[Tipos de ajuste]]
- [[Tolerâncias gerais]]
- [[02-tolerancias-ajustes/index|Índice do módulo 02]]
