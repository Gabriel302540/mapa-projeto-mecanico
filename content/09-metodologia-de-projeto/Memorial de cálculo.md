---
title: Memorial de cálculo
tags: [metodologia, documentacao]
fontes: [Pahl, Beitz, Feldhusen e Grote Projeto na Engenharia (cap. de documentação), ABNT NBR 14724 (trabalhos acadêmicos — estrutura de documentos, referência geral) ⚠️ verificar aplicabilidade, Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 1 — incerteza, coeficientes de segurança e unidades)]
status: rascunho
---

**Resumo:** o memorial de cálculo é o documento que registra como o equipamento foi dimensionado: dados de entrada, premissas, normas, métodos, cálculos, resultados e conclusões. Ele permite que outra pessoa verifique o projeto, que alterações futuras partam de uma base conhecida e que a responsabilidade técnica fique documentada.

## O que é

### Estrutura recomendada

1. **Identificação:** título, número do documento, revisão, equipamento, autor, verificador, data.
2. **Objetivo e escopo:** o que é dimensionado e o que não é.
3. **Dados de entrada:** cargas, rotações, potências, dimensões impostas, propriedades do material processado, condições ambientais — **com a origem de cada um** (medição, catálogo, cliente, norma).
4. **Premissas e hipóteses:** simplificações adotadas (ex.: "carga considerada estática", "eixo simplesmente apoiado nos centros dos rolamentos").
5. **Normas e referências:** normas, livros e catálogos usados, com edição.
6. **Materiais:** especificação e propriedades adotadas.
7. **Cálculos:** em ordem lógica, com fórmulas, substituição dos valores, unidades e resultados intermediários. Cada verificação termina com uma comparação explícita (tensão × admissível; vida × requerida).
8. **Resultados e conclusões:** tabela-resumo com os coeficientes de segurança e as decisões (diâmetros, componentes escolhidos).
9. **Anexos:** croquis, diagramas de esforços, folhas de catálogo, saídas de software.
10. **Histórico de revisões.**

### Boas práticas

- **Unidades consistentes** (SI) e explícitas em todas as equações.
- **Fórmula → valores → resultado**, para que o verificador consiga refazer.
- **Coeficientes de segurança justificados** pela incerteza das cargas, dos materiais e das consequências da falha.
- **Ordens de grandeza conferidas** ("o eixo de 90 mm é coerente com eixos similares?").
- **Verificação independente** por outro engenheiro em itens críticos.
- **Planilhas e softwares** devem ser documentados (versão, dados de entrada), não apenas o resultado final.

## Por que importa no projeto

- **Rastreabilidade:** em caso de falha, o memorial mostra se o problema foi de premissa, de cálculo, de fabricação ou de operação.
- **Alterações futuras:** aumentar a capacidade de um equipamento exige saber com que cargas ele foi projetado.
- **Responsabilidade técnica:** o memorial sustenta a anotação de responsabilidade técnica do projeto.
- **Aprendizado da equipe:** memoriais bem feitos viram referência para os próximos projetos.

## Como aplicar (passo a passo / regras práticas)

1. Comece o memorial **junto com o projeto**, não no fim.
2. Registre a **origem de cada dado** de entrada.
3. Escreva as premissas antes dos cálculos.
4. Use um **modelo padrão** da equipe (seções fixas).
5. Faça a **tabela-resumo** de resultados e coeficientes de segurança.
6. Peça **verificação** e registre quem verificou.
7. **Revise** o memorial sempre que o projeto mudar, com a mesma numeração de revisão dos desenhos.

## Norma relacionada

Não há uma norma única para memoriais de equipamentos mecânicos; o formato costuma ser definido pela empresa ou pelo cliente. Normas técnicas específicas (ISO 281, ISO 6336, DIN 743, AWS D1.1 etc.) definem os **métodos** usados dentro dele.

## Exemplo prático

**Situação:** trecho de memorial para a verificação de um eixo (ver [[Fadiga de eixos]]).

> **4.3 Verificação à fadiga — seção do ressalto do mancal (seção C)**
>
> **Dados:** $M_a$ = 3000 N·m (diagrama do anexo A); $T_m$ = 2387,5 N·m (75 kW a 300 rpm, item 3.1); material SAE 1045 trefilado, $S_{ut}$ = 630 MPa (certificado, item 2.2); $K_f$ = 1,6 e $K_{fs}$ = 1,4 (Shigley, tab. 7-1, raio R5 / d = 90 → r/d ≈ 0,06).
>
> **Limite de fadiga:** $S_e = k_a k_b k_e S_e' = 0{,}82 \times 0{,}745 \times 0{,}868 \times 315 = 167$ MPa.
>
> **Critério DE-Goodman:** $n = 2{,}1$ para d = 90 mm.
>
> **Conclusão:** atende ($n$ ≥ 2,0 adotado no item 1.4).

> [!question] Exercício
>
> Cite três informações que, se faltarem num memorial, impedem a verificação independente.
>
> > [!success]- Resolução
> >
> > Exemplos: (1) a **origem dos dados de entrada** (de onde veio a carga); (2) as **premissas** (como o eixo foi modelado, que carga foi considerada); (3) as **propriedades de material** e a norma ou fonte; (4) as **fórmulas com os valores substituídos** e as unidades; (5) o **critério de aceitação** (coeficiente de segurança mínimo).

## Erros comuns

- **Só os resultados**, sem fórmulas nem dados de entrada.
- **Unidades misturadas** (kgf, N, MPa e psi no mesmo cálculo).
- **Premissas implícitas.**
- **Memorial desatualizado** em relação aos desenhos.

## Ver também

- [[Etapas do projeto]]
- [[Controle de desenhos]]
- [[Fadiga de eixos]]
- [[09-metodologia-de-projeto/index|Índice do módulo 09]]
