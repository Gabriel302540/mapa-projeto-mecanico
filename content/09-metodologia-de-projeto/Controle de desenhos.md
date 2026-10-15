---
title: Revisão e controle de desenhos
tags: [metodologia, documentacao]
fontes: [ISO 7200:2004 (campos de legenda), ISO 11442 (gestão de documentos técnicos de produto) ⚠️ verificar, ISO 10007 (gestão de configuração), Pahl, Beitz, Feldhusen e Grote Projeto na Engenharia (cap. de documentação)]
status: rascunho
---

**Resumo:** controlar desenhos é garantir que todos — projeto, compras, fabricação, montagem, manutenção — usem sempre a versão válida de cada documento. Isso exige numeração única, estados de aprovação, revisões registradas, solicitações formais de mudança e controle das cópias em circulação.

## O que é

### Ciclo de vida de um desenho

| Estado | Significado |
|---|---|
| **Em elaboração** | Rascunho; não pode ser usado para fabricar |
| **Em verificação** | Revisão por outro projetista ou engenheiro |
| **Aprovado / liberado** | Válido para uso (fabricação, compra, montagem) |
| **Revisado** | Nova versão liberada; a anterior fica obsoleta |
| **Cancelado / obsoleto** | Não deve mais ser usado; mantido só como histórico |

### Revisões

- Cada alteração liberada gera uma **nova revisão** (letra ou número), registrada no **quadro de revisões** do desenho: o que mudou, por quê, quem fez, quem aprovou e quando. Ver [[Legenda]].
- A região alterada é marcada no desenho (triângulo com a letra da revisão, ou nuvem).
- **Pequenas mudanças também são revisões.** Não existe "corrigi só uma cota, não precisa revisar".

### Gestão de mudanças

1. **Solicitação de mudança (SM / ECR):** alguém identifica a necessidade (erro, melhoria, problema de fabricação).
2. **Análise de impacto:** que outros documentos, peças em estoque, peças em fabricação e equipamentos instalados são afetados? A peça antiga ainda pode ser usada (intercambiável)?
3. **Aprovação** pela responsabilidade técnica.
4. **Ordem de mudança (OM / ECN):** emissão das novas revisões de todos os documentos afetados.
5. **Comunicação** às áreas e **recolhimento das cópias antigas**.

### Cópias controladas

- **Cópia controlada:** distribuída com registro; quando há nova revisão, a antiga é recolhida e substituída.
- **Cópia não controlada:** para informação; marcada como tal ("cópia não controlada — verificar revisão antes de usar").
- Com sistemas digitais (PDM/GED), a consulta deve ser feita sempre no sistema, e as impressões tratadas como não controladas.

### *As built* (como construído)

Durante a montagem, alterações de campo acontecem. Ao final, os desenhos devem ser atualizados para refletir o que foi **realmente** instalado, senão a manutenção futura trabalha com informação errada.

## Por que importa no projeto

- **A peça errada fabricada** a partir de uma cópia antiga é um dos erros mais caros e mais comuns.
- **Intercambiabilidade:** saber se a revisão B e a C da mesma peça são intercambiáveis decide se o estoque antigo pode ser usado.
- **Rastreabilidade e responsabilidade técnica.**

## Como aplicar (passo a passo / regras práticas)

1. **Numeração única** para cada desenho, nunca reaproveitada.
2. **Nenhum desenho sai** sem verificação e aprovação registradas.
3. **Toda alteração = nova revisão**, com descrição clara no quadro.
4. **Se a mudança altera forma, encaixe ou função** (não intercambiável), considere **novo número de peça**, não só nova revisão. ⚠️ verificar a regra adotada pela empresa.
5. **Controle as cópias** em circulação e recolha as obsoletas.
6. **Atualize o *as built*** ao final de cada obra.

## Norma relacionada

- **ISO 7200**: campos da legenda (incluindo revisão e situação do documento).
- **ISO 11442**: gestão de documentação técnica de produto. ⚠️ verificar.
- **ISO 10007**: gestão de configuração.

## Exemplo prático

**Situação:** a oficina fabricou 4 eixos pela revisão B de um desenho, enquanto a revisão C (com raio de concordância maior e material diferente) já estava liberada há duas semanas.

- **Causa:** cópias impressas da revisão B continuavam na oficina; a distribuição da C não recolheu as antigas.
- **Consequências:** 4 eixos com o defeito que motivou a revisão C (risco de fadiga) e custo de refabricação.
- **Ações:** recolher e destruir cópias obsoletas; carimbar impressões como "não controlada"; incluir na ordem de fabricação o número **e a revisão** do desenho, conferidos com o sistema no momento da liberação.

> [!question] Exercício
>
> Uma peça teve o furo de fixação alterado de Ø14 para Ø18, e as peças antigas não montam mais no conjunto novo. Basta uma nova revisão do desenho?
>
> > [!success]- Resolução
> >
> > Provavelmente **não**. A peça nova **não é intercambiável** com a antiga (forma e encaixe mudaram). Muitas empresas exigem, nesse caso, um **novo número de peça** (ou um sufixo), para que estoques, listas de sobressalentes e equipamentos instalados não misturem as duas versões. Além disso, é preciso avaliar o impacto no conjunto, nas peças em estoque e nos equipamentos em campo.

## Erros comuns

- **Alterar o desenho sem mudar a revisão.**
- **Cópias antigas circulando** na oficina.
- **Revisão sem descrição** do que mudou.
- **Mudança não intercambiável com o mesmo número de peça.**
- **Não atualizar o *as built*.**

## Ver também

- [[Legenda]]
- [[Lista de materiais]]
- [[Memorial de cálculo]]
- [[09-metodologia-de-projeto/index|Índice do módulo 09]]
