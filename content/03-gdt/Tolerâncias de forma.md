---
title: Tolerâncias de forma
tags: [gdt, forma]
fontes: [ISO 1101:2017, ISO 12780 (retitude), ISO 12781 (planeza), ISO 12181 (circularidade), ISO 12180 (cilindricidade), Henzold Geometrical Dimensioning and Tolerancing for Design, Manufacturing and Inspection]
status: rascunho
---

**Resumo:** tolerâncias de forma controlam o quanto um elemento pode se afastar da forma geométrica perfeita — reta, plano, círculo ou cilindro — sem referência a nenhum outro elemento. São quatro: retitude, planeza, circularidade e cilindricidade.

## O que é

| Símbolo | Característica | Zona de tolerância | Aplicação típica |
|---|---|---|---|
| ⏤ | **Retitude** | Entre duas retas paralelas (linha numa superfície) ou dentro de um cilindro Ø t (eixo de um cilindro) | Guias, eixos longos, réguas |
| ⏥ | **Planeza** | Entre dois planos paralelos afastados de t | Faces de apoio, faces de vedação, bases de máquinas |
| ○ | **Circularidade** | Em cada seção transversal, entre dois círculos concêntricos com diferença de raios t | Assentos de rolamentos, pistões, buchas |
| ⌭ | **Cilindricidade** | Entre dois cilindros coaxiais com diferença de raios t | Assentos de rolamentos, cilindros hidráulicos |

**Características:**

- **Não têm referência:** a zona "flutua" e se ajusta ao próprio elemento.
- **Valor sempre positivo**, sem Ø (exceto retitude de eixo, que usa Ø).
- **Hierarquia:** cilindricidade inclui circularidade e retitude das geratrizes; planeza inclui a retitude das linhas do plano. Não faz sentido dar circularidade maior que cilindricidade no mesmo elemento.
- **Relação com o tamanho:** a tolerância de forma deve ser **menor** que a tolerância dimensional do mesmo elemento, senão não acrescenta nada (com envoltória, a forma já está limitada pelo tamanho; ver [[Independência e envoltória]]).

### Como se mede (ideia geral)

- **Planeza:** peça sobre três apoios ajustáveis no desempeno, relógio comparador varrendo a face; ou máquina de medir por coordenadas (MMC).
- **Circularidade:** em equipamento de medição de circularidade (mesa rotativa de precisão) ou, de forma aproximada, com blocos em V e relógio (método que pode falhar para certas formas lobuladas).
- **Retitude:** régua de precisão e apalpador, ou nível eletrônico em peças grandes.

## Por que importa no projeto

- **Rolamentos:** o anel do rolamento é fino e copia a forma do assento. Um assento ovalizado deforma a pista e reduz a vida. Fabricantes recomendam tolerâncias de forma para os assentos em função da classe do rolamento. ⚠️ verificar no catálogo.
- **Vedação:** faces de flange e tampas com juntas precisam de planeza para não vazar.
- **Bases de máquinas:** a planeza dos apoios de motor e redutor evita o "pé manco" (*soft foot*), que deforma a carcaça ao apertar os chumbadores e desalinha o conjunto.

## Como aplicar (passo a passo / regras práticas)

1. **Use forma só onde a função pede** (assentos, vedações, apoios, guias).
2. **Escolha o valor** como uma fração da tolerância dimensional: uma regra prática comum é usar entre 1/4 e 1/2 da tolerância de tamanho (para assentos de rolamento, os catálogos costumam indicar valores da ordem de IT3 a IT5).
3. **Prefira cilindricidade** a circularidade quando o comprimento do assento também importa.
4. **Aplique planeza nas referências primárias**, já que elas definem todas as outras medições.

## Norma relacionada

- **ISO 1101:2017**: definição das zonas de tolerância de forma.
- **ISO 12780, 12781, 12181 e 12180**: definições e métodos de avaliação de retitude, planeza, circularidade e cilindricidade.

## Exemplo prático

**Situação:** a base usinada de um **conjunto motor + redutor** tem quatro sapatas de apoio do motor. Depois da montagem, o motor vibra e a carcaça trinca próximo a um pé.

**Diagnóstico:** as quatro sapatas não estavam no mesmo plano (diferença de 0,4 mm). Ao apertar os chumbadores, a carcaça foi deformada para encostar.

**Especificação correta:** usinar as quatro sapatas numa mesma operação e indicar **planeza comum** das quatro faces:

<span class="fcf"><span>⏥</span><span>0,05 CZ</span></span>

com "4×" e o modificador CZ (zona combinada), significando que as quatro faces devem estar juntas entre dois planos afastados de 0,05 mm. ⚠️ verificar valores recomendados pelos fabricantes de motores e as normas de alinhamento de máquinas.

> [!question] Exercício 1
>
> Um assento de rolamento Ø60 k6 (tolerância de 19 µm) recebe tolerância de circularidade de 0,03 mm. Essa indicação faz sentido?
>
> > [!success]- Resolução
> >
> > **Não.** A circularidade (30 µm) é maior que a própria tolerância de tamanho (19 µm). Se o desenho usar envoltória, a forma já está limitada pelo tamanho e a indicação não acrescenta nada; se usar independência, permitir 30 µm de ovalização num assento de rolamento é excessivo. Um valor coerente estaria na faixa de 0,005 a 0,008 mm (verificar no catálogo do rolamento).

> [!question] Exercício 2
>
> Por que uma tolerância de planeza nunca tem referência no quadro?
>
> > [!success]- Resolução
> >
> > Porque a planeza só compara a superfície com um **plano ideal que se ajusta a ela mesma**. Ela não diz nada sobre a posição ou a inclinação da face em relação a outra parte da peça. Se for preciso controlar isso, usa-se **paralelismo** ou **perpendicularidade**, que têm referência e também limitam a planeza.

## Erros comuns

- **Tolerância de forma maior que a tolerância de tamanho.**
- **Referência em tolerância de forma.**
- **Circularidade medida só com paquímetro ou micrômetro**: a medição de dois pontos não detecta formas de três ou cinco lóbulos.
- **Esquecer a planeza das faces de referência**.

## Ver também

- [[Por que GD&T]]
- [[Tolerâncias de orientação]]
- [[Independência e envoltória]]
- [[04-acabamento-superficial/index|Acabamento superficial]]
- [[03-gdt/index|Índice do módulo 03]]
