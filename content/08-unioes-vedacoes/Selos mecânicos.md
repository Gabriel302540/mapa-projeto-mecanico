---
title: Selos mecânicos
tags: [vedacoes, bombas]
fontes: [API 682 (selos mecânicos para bombas centrífugas e rotativas), ISO 21049 (equivalente ISO da API 682) ⚠️ verificar, Müller e Nau Fluid Sealing Technology (cap. de selos mecânicos), Mattos e Falco Bombas Industriais (cap. de vedação), catálogos técnicos de fabricantes de selos]
status: rascunho
---

**Resumo:** o selo mecânico veda um eixo girante por meio de duas faces planas, muito lisas, pressionadas uma contra a outra: uma gira com o eixo, a outra fica parada na carcaça. Entre elas forma-se um filme microscópico de fluido. Vazam muito menos que gaxetas e quase não exigem ajuste, mas são mais caros, sensíveis a funcionamento a seco, sólidos e desalinhamentos.

## O que é

### Componentes

- **Face rotativa** e **face estacionária** (sede): pares típicos de materiais duros e autolubrificantes — **carbono-grafite × carbeto de silício** (uso geral) ou **carbeto de silício × carbeto de silício / carbeto de tungstênio** (fluidos com sólidos).
- **Elementos de pressão:** mola única, múltiplas molas ou fole metálico.
- **Vedações secundárias:** o-rings ou foles entre as faces e o eixo/carcaça.
- **Sobreposta** (tampa do selo) e **luva** (no eixo).

As faces são **lapidadas** com planeza de poucas bandas de luz (cada banda ≈ 0,3 µm, medida com plano óptico). ⚠️ verificar valores com o fabricante.

### Classificações

- **Balanceado × não balanceado:** no balanceado, a geometria reduz a força hidráulica que empurra as faces, permitindo pressões maiores com menos calor e desgaste.
- **Simples × duplo:** o duplo tem dois pares de faces com um fluido de barreira entre eles (para fluidos perigosos, tóxicos ou que cristalizam).
- **Cartucho:** selo pré-montado numa luva, que se instala sem ajustes de medida no campo (reduz erros de montagem).

### Planos de lavagem (API 682)

A API 682 numera os arranjos de circulação de fluido na câmara do selo ("planos"): recirculação do próprio fluido da descarga (plano 11), injeção de líquido limpo externo (plano 32), fluido de barreira pressurizado em selos duplos (plano 53), entre outros. Eles mantêm as faces limpas e frias. ⚠️ verificar a descrição de cada plano na norma.

## Por que importa no projeto

- **Bombas de processo** com fluidos quentes, tóxicos, inflamáveis ou caros exigem selo mecânico (vazamento quase nulo).
- **Fluidos com sólidos ou que cristalizam** (caldas, xaropes, polpas) exigem faces duras e lavagem com líquido limpo.
- **Principais causas de falha:** **funcionamento a seco** (as faces queimam em segundos), sólidos entre as faces, vibração e desalinhamento, montagem errada (medida de compressão da mola), choque térmico.

## Como aplicar (passo a passo / regras práticas)

1. **Caracterize o fluido:** pressão, temperatura, sólidos, viscosidade, tendência a cristalizar, toxicidade.
2. **Escolha o tipo** (simples/duplo, balanceado, cartucho) e os materiais das faces e elastômeros.
3. **Escolha o plano de lavagem** compatível.
4. **Garanta as condições mecânicas** do equipamento: batimento do eixo, deflexão, perpendicularidade da câmara (ver [[Batimento]]).
5. **Proteja contra funcionamento a seco** (instrumentação de nível, procedimento de escorva).
6. **Prefira selos cartucho** em manutenção de campo.

## Norma relacionada

- **API 682 / ISO 21049**: selos mecânicos para bombas centrífugas e rotativas (seleção, planos, testes). ⚠️ verificar edições.

## Exemplo prático

**Situação:** uma bomba de **líquido açucarado quente com sólidos finos** vaza muito pelas gaxetas, com perda de produto e sujeira na área.

- **Proposta:** selo mecânico **cartucho**, faces **carbeto de silício × carbeto de silício** (resistentes a sólidos), elastômeros compatíveis com a temperatura (por exemplo, FKM ou EPDM conforme o fluido ⚠️).
- **Lavagem com água limpa externa** (plano de injeção) para impedir que o produto cristalize e que sólidos entrem nas faces.
- **Procedimento:** nunca partir a bomba sem escorva; conferir batimento do eixo antes da instalação.

> [!question] Exercício
>
> Compare gaxeta e selo mecânico em três critérios: vazamento, manutenção e custo inicial.
>
> > [!success]- Resolução
> >
> > | Critério | Gaxeta | Selo mecânico |
> > |---|---|---|
> > | Vazamento | Gotejamento necessário | Praticamente nulo |
> > | Manutenção | Reaperto e troca frequentes, simples | Pouca manutenção, mas troca mais complexa (ou cartucho) |
> > | Custo inicial | Baixo | Alto |
> >
> > Além disso, o selo consome menos potência por atrito e não desgasta a luva, mas é sensível a funcionamento a seco e a condições mecânicas ruins.

## Erros comuns

- **Partir a bomba a seco.**
- **Faces macias** (carbono) com fluidos abrasivos.
- **Sem lavagem** em fluidos que cristalizam.
- **Ignorar o batimento** e a vibração do eixo.
- **Ajustar a compressão da mola errado** em selos de componentes (não cartucho).

## Ver também

- [[Gaxetas]]
- [[Retentores]]
- [[O-rings]]
- [[Batimento]]
- [[08-unioes-vedacoes/index|Índice do módulo 08]]
