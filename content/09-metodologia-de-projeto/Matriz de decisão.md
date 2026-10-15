---
title: Concepção e matriz de decisão
tags: [metodologia, concepcao]
fontes: [Pahl, Beitz, Feldhusen e Grote Projeto na Engenharia (caps. de projeto conceitual e avaliação de soluções), Back, Ogliari, Dias e Silva Projeto Integrado de Produtos (cap. de seleção de concepções), Pugh Total Design, Ullman The Mechanical Design Process]
status: rascunho
---

**Resumo:** na concepção, geram-se várias soluções possíveis para o problema, decompondo a função principal em subfunções e combinando soluções parciais (matriz morfológica). A escolha entre as alternativas é feita com uma matriz de decisão: critérios com pesos, notas para cada alternativa e uma soma ponderada, que torna a decisão explícita e discutível.

## O que é

### Geração de alternativas

1. **Função global:** o que o sistema faz, de forma abstrata ("transmitir torque do motor ao tambor com redução de 70:1").
2. **Subfunções:** reduzir rotação, acoplar eixos, absorver desalinhamento, apoiar o eixo, proteger contra sobrecarga.
3. **Matriz morfológica:** para cada subfunção, listar soluções possíveis (redutor helicoidal, planetário, sem-fim, correia + redutor...). Combinações coerentes formam **concepções**.
4. **Técnicas de criatividade:** brainstorming, analogias, pesquisa de soluções existentes (catálogos, patentes, equipamentos de outros setores).

### Matriz de decisão ponderada

1. Defina **critérios** a partir dos requisitos (custo, confiabilidade, manutenção, espaço, prazo, segurança...).
2. Atribua **pesos** que somem 1 (ou 100 %), refletindo a importância.
3. Dê **notas** a cada alternativa em cada critério (por exemplo, 1 a 5).
4. Calcule a **soma ponderada**:

$$
S_j = \sum_i w_i\,n_{ij}
$$

5. Analise o resultado: a diferença é significativa? Uma alternativa é eliminada por algum critério obrigatório? A escolha muda com pesos razoavelmente diferentes (análise de sensibilidade)?

### Matriz de Pugh (alternativa simples)

Compara cada alternativa com uma **referência** (a solução atual ou uma escolhida), critério a critério, com **+** (melhor), **−** (pior) ou **S** (igual). Útil nas primeiras rodadas, para eliminar e combinar ideias.

**Importante:** exigências (requisitos obrigatórios) **não entram como critério ponderado**: alternativas que não as atendem são eliminadas antes.

## Por que importa no projeto

- **Decisão documentada:** mostra por que uma solução foi escolhida, útil para revisões e auditorias.
- **Discussão em equipe:** os pesos e notas expõem divergências de forma objetiva.
- **Evita a "paixão pela primeira ideia".**

## Como aplicar (passo a passo / regras práticas)

1. Parta da [[Levantamento de requisitos|lista de requisitos]].
2. Elimine alternativas que não atendem às exigências.
3. Escolha de 4 a 7 critérios relevantes (muitos critérios diluem a decisão).
4. Defina pesos **antes** de dar as notas.
5. Dê notas com base em dados (custos de catálogo, cálculos, histórico de falhas), não só opinião.
6. Faça uma análise de sensibilidade nos pesos mais discutíveis.

## Norma relacionada

Não há norma obrigatória; os métodos vêm da **literatura de metodologia de projeto** (Pahl e Beitz, Pugh, Back et al.).

## Exemplo prático

**Situação:** escolher a concepção de acionamento de um transportador (já eliminadas as que não cabem no espaço).

- **A:** motor + acoplamento elástico + redutor helicoidal de eixos paralelos + acoplamento de engrenagens
- **B:** motor + redutor de eixo oco montado no eixo do tambor (com braço de torção)
- **C:** motor + correias em V + redutor menor

| Critério | Peso | A | B | C |
|---|---|---|---|---|
| Confiabilidade | 0,30 | 4 | 5 | 3 |
| Custo de aquisição | 0,25 | 3 | 4 | 5 |
| Facilidade de manutenção | 0,20 | 4 | 3 | 4 |
| Espaço ocupado | 0,15 | 3 | 4 | 5 |
| Padronização com o parque | 0,10 | 5 | 3 | 2 |
| **Total** | 1,00 | **3,70** | **4,00** | **3,90** |

A concepção **B** fica à frente, mas a diferença para C é pequena. Uma análise de sensibilidade (por exemplo, aumentar o peso da manutenção) e o detalhamento de custos ajudariam a confirmar.

> [!question] Exercício
>
> Recalcule a matriz acima trocando os pesos de "confiabilidade" (para 0,20) e "manutenção" (para 0,30). A escolha muda?
>
> > [!success]- Resolução
> >
> > - A: $0{,}20 \times 4 + 0{,}25 \times 3 + 0{,}30 \times 4 + 0{,}15 \times 3 + 0{,}10 \times 5 = 0{,}8 + 0{,}75 + 1{,}2 + 0{,}45 + 0{,}5 = 3{,}70$
> > - B: $0{,}20 \times 5 + 0{,}25 \times 4 + 0{,}30 \times 3 + 0{,}15 \times 4 + 0{,}10 \times 3 = 1{,}0 + 1{,}0 + 0{,}9 + 0{,}6 + 0{,}3 = 3{,}80$
> > - C: $0{,}20 \times 3 + 0{,}25 \times 5 + 0{,}30 \times 4 + 0{,}15 \times 5 + 0{,}10 \times 2 = 0{,}6 + 1{,}25 + 1{,}2 + 0{,}75 + 0{,}2 = 4{,}00$
> >
> > Agora **C** vence. A decisão é **sensível** aos pesos de confiabilidade e manutenção, e esses pesos precisam ser discutidos com a equipe de manutenção antes de fechar a escolha.

## Erros comuns

- **Definir os pesos depois** de ver as notas (viés).
- **Colocar exigências como critério ponderado.**
- **Critérios demais** ou redundantes (contando a mesma coisa duas vezes).
- **Não fazer análise de sensibilidade** quando os totais são próximos.

## Ver também

- [[Etapas do projeto]]
- [[Levantamento de requisitos]]
- [[Redutores]]
- [[09-metodologia-de-projeto/index|Índice do módulo 09]]
