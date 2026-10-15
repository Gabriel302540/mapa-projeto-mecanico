---
title: Ajustes recomendados por aplicação
tags: [tolerancias, ajustes]
fontes: [ISO 286-1:2010 (ajustes preferenciais), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. de tolerâncias e ajustes), Niemann Elementos de Máquinas (cap. de tolerâncias e ajustes), catálogos técnicos de rolamentos (seção de ajustes)]
status: rascunho
---

**Resumo:** em vez de inventar uma combinação de furo e eixo a cada projeto, usa-se um conjunto pequeno de ajustes preferenciais, já testados na prática. Esta nota reúne os mais usados no sistema furo-base, com a aplicação típica de cada um e as recomendações especiais para rolamentos.

## O que é

### Ajustes preferenciais (furo-base)

| Ajuste | Tipo | Característica | Aplicações típicas |
|---|---|---|---|
| **H11/c11** | Folga grande | Montagem muito livre | Peças de máquinas agrícolas, articulações grosseiras, peças sujeitas a sujeira e dilatação |
| **H9/d9** | Folga livre | Giro livre, folga generosa | Mancais com rotação alta e temperaturas variáveis, polias loucas, articulações |
| **H8/f7** | Folga de giro | Folga média, giro com lubrificação | Mancais de deslizamento comuns, buchas, eixos de bombas |
| **H7/g6** | Folga deslizante | Folga pequena, posicionamento preciso com movimento | Engrenagens deslizantes, guias, êmbolos, pinos de articulação precisos |
| **H7/h6** | Folga de posicionamento | Folga mínima zero; monta à mão | Centralização de peças fixas desmontáveis, tampas, flanges |
| **H7/k6** | Incerto | Montagem com martelo de borracha; desmontável | Engrenagens, polias e acoplamentos com chaveta; anel interno de rolamentos com carga moderada |
| **H7/n6** | Incerto (tendendo a interferência) | Montagem com prensa leve | Buchas, engrenagens com chaveta sob impacto; posicionamento muito preciso |
| **H7/p6** | Interferência leve | Montagem com prensa; desmontável com cuidado | Buchas de bronze em carcaças, peças que não devem girar mas podem ser trocadas |
| **H7/s6** | Interferência média | Montagem térmica ou prensa pesada | Cubos e coroas que transmitem torque sem chaveta, buchas permanentes |
| **H7/u6** | Interferência forte | Montagem térmica | Uniões permanentes de alto torque (aros sobre cubos, coroas montadas) |

⚠️ verificar as recomendações na ISO 286-1 e nas normas ou catálogos usados pela empresa. Os nomes "deslizante", "de giro" etc. variam entre autores.

### Ajustes de rolamentos

Rolamentos são um caso especial: os anéis já têm tolerâncias próprias (normalmente com **desvio negativo** no furo do anel interno), e a escolha depende de **qual anel gira em relação à carga**:

- **Anel que gira em relação à direção da carga** (carga "rotativa" para ele) → ajuste **com interferência**, senão o anel "caminha" (*creep*) e desgasta o assento.
- **Anel parado em relação à carga** → pode ter **folga** ou ajuste incerto, o que facilita a montagem e permite a dilatação axial (rolamento livre).

Caso mais comum em transmissões: **eixo gira, carga fixa** (peso, tração de correia).

| Assento | Situação típica | Classe usual |
|---|---|---|
| Eixo (anel interno gira) | Carga leve | j6, js6 |
| Eixo (anel interno gira) | Carga normal | k5, k6, m5, m6 |
| Eixo (anel interno gira) | Carga pesada ou choque | n6, p6 |
| Alojamento inteiriço (anel externo parado) | Rolamento livre (deslocamento axial) | H7, G7 |
| Alojamento (anel externo parado) | Carga normal | H7, J7 |
| Alojamento bipartido | Geral | H7 (evitar interferência, que deforma o anel) |
| Rolamento em bucha de fixação (eixo liso) | Eixos de transmissão | h9 ou h10 com tolerância de cilindricidade |

⚠️ verificar sempre o catálogo do fabricante do rolamento, que traz tabelas por tipo, tamanho e carga. Ver [[05-elementos-de-maquinas/index|Rolamentos]].

## Por que importa no projeto

- **Experiência acumulada:** os ajustes preferenciais já foram validados em milhões de aplicações.
- **Ferramental e estoque:** usar poucos ajustes significa menos alargadores, calibradores e tabelas para a oficina.
- **Manutenção:** um ajuste coerente com a função define se a peça sai com saca-polia, com prensa ou com maçarico.

## Como aplicar (passo a passo / regras práticas)

1. **Classifique a função** (gira, desliza, posiciona, transmite torque, permanente).
2. **Escolha na tabela** o ajuste mais folgado que ainda atenda a função.
3. **Para rolamentos**, identifique qual anel gira em relação à carga e siga o catálogo.
4. **Calcule os extremos** de folga e interferência e verifique a função (ver [[Tipos de ajuste]]).
5. **Considere a temperatura de operação:** materiais diferentes (aço e bronze, aço e alumínio) mudam a folga ao aquecer.
6. **Registre o ajuste no desenho de conjunto** (Ø80 H7/k6) e a classe em cada desenho de detalhe (Ø80 H7 no furo; Ø80 k6 no eixo). Ver [[Indicação de tolerâncias]].

## Norma relacionada

- **ISO 286-1:2010**: apresenta uma seleção de classes de tolerância e ajustes preferenciais.
- **ISO 492**: tolerâncias dos rolamentos (anéis). ⚠️ verificar.
- **Catálogos de rolamentos**: tabelas de ajustes recomendados para eixos e alojamentos.

## Exemplo prático

**Situação:** especificar os ajustes de um **eixo intermediário de redutor** com: uma engrenagem com chaveta, dois rolamentos de rolos cônicos, um espaçador e uma bucha de bronze de apoio para um pinhão louco.

| Ligação | Função | Ajuste escolhido |
|---|---|---|
| Engrenagem no eixo | Posicionar; torque pela chaveta; desmontável | **H7/k6** |
| Anel interno do rolamento no eixo | Anel gira com o eixo; carga normal | **k6** no eixo (ou m6 se a carga for alta) |
| Anel externo no alojamento da carcaça | Anel parado; carga normal | **H7** |
| Espaçador entre engrenagem e rolamento | Só posicionar axialmente | **H8/h7** (folga) |
| Pinhão louco na bucha de bronze | Girar com lubrificação | **H8/f7** |
| Bucha de bronze no pinhão | Não girar; trocável | **H7/p6** |

> [!question] Exercício
>
> Uma polia de correia em V é montada com chaveta numa ponta de eixo. Precisa ser centralizada com precisão (para não bater) e desmontada em toda manutenção. Que ajuste escolher e por quê?
>
> > [!success]- Resolução
> >
> > **H7/k6** (ou H7/js6 se a desmontagem frequente for prioridade). É um ajuste incerto: centraliza bem, pode ser montado e desmontado sem prensa pesada, e o torque é transmitido pela **chaveta**, não pelo ajuste. Um ajuste com folga (H7/g6) deixaria a polia batendo; um com interferência (H7/s6) dificultaria a manutenção.

## Erros comuns

- **Rolamento com anel rotativo em ajuste com folga:** o anel desliza no assento e desgasta o eixo (marca de "creep").
- **Interferência em alojamento bipartido:** deforma o anel externo e reduz a vida do rolamento.
- **Ajuste com interferência sem verificar a tensão no cubo**, sobretudo em cubos de ferro fundido.
- **Copiar ajustes de outro projeto** sem conferir a função.

## Ver também

- [[Tipos de ajuste]]
- [[Sistema furo-base]]
- [[Graus IT]]
- [[05-elementos-de-maquinas/index|Elementos de máquinas]]
- [[02-tolerancias-ajustes/index|Índice do módulo 02]]
