---
title: Gaxetas
tags: [vedacoes]
fontes: [Fluid Sealing Association Compression Packing Technical Manual ⚠️ verificar, Müller e Nau Fluid Sealing Technology (cap. de gaxetas), catálogos técnicos de fabricantes de gaxetas, Mattos e Falco Bombas Industriais (cap. de vedação de eixos)]
status: rascunho
---

**Resumo:** gaxetas são anéis de material trançado (fibras impregnadas) comprimidos numa caixa em volta de um eixo ou haste, para vedar bombas, válvulas e agitadores. São simples, robustas e baratas, mas exigem um pequeno vazamento controlado para lubrificar e refrigerar, e precisam de reaperto periódico.

## O que é

### Componentes do engaxetamento

- **Caixa de gaxetas (*stuffing box*):** cavidade em volta do eixo.
- **Anéis de gaxeta:** normalmente 4 a 6, de seção quadrada.
- **Anel lanterna** (opcional): anel vazado no meio do conjunto, por onde se injeta líquido limpo de lavagem ou refrigeração (*flushing*).
- **Sobreposta (preme-gaxeta):** peça apertada por prisioneiros, que comprime os anéis axialmente; a compressão axial vira pressão radial contra o eixo.
- **Luva protetora do eixo:** peça substituível sobre o eixo, onde a gaxeta trabalha.

### Materiais

| Material | Uso |
|---|---|
| Fibras de PTFE | Produtos químicos, alimentos |
| Grafite flexível / fibras de grafite | Temperaturas altas, vapor |
| Aramida | Fluidos com sólidos (abrasivos) |
| Fibras sintéticas com PTFE | Uso geral, água |

### Por que precisa vazar

O atrito entre a gaxeta e o eixo gera calor. Um **gotejamento controlado** (da ordem de dezenas de gotas por minuto em bombas, conforme o fabricante ⚠️) lubrifica e refrigera o contato. Apertar até zerar o vazamento queima a gaxeta e desgasta a luva.

## Por que importa no projeto

- **Bombas de água, de produtos com sólidos e agitadores** usam gaxetas pela simplicidade e tolerância a sujeira e desalinhamentos.
- **Manutenção simples** e barata, mas frequente.
- **Para fluidos perigosos ou onde o vazamento é inaceitável**, usam-se selos mecânicos. Ver [[Selos mecânicos]].

## Como aplicar (passo a passo / regras práticas)

1. **Escolha o material** pelo fluido, temperatura, pressão e velocidade periférica.
2. **Corte os anéis** na medida do eixo (luva), com corte a 45° ou reto conforme o fabricante.
3. **Monte anel por anel**, assentando cada um, com as **juntas defasadas** de 90° a 120°.
4. **Posicione o anel lanterna** alinhado com a conexão de lavagem.
5. **Aperte a sobreposta levemente**, dê partida e ajuste aos poucos até o gotejamento recomendado.
6. **Preveja luva substituível** no eixo e conexão de lavagem quando o fluido tiver sólidos.

## Norma relacionada

Não há norma dimensional amplamente adotada para engaxetamentos industriais comuns; as referências são os **catálogos** e guias técnicos de associações de fabricantes. ⚠️ verificar normas específicas (por exemplo, para válvulas).

## Exemplo prático

**Situação:** uma bomba que transporta água com areia apresenta desgaste rápido da luva do eixo na região das gaxetas.

- **Causa provável:** partículas abrasivas entram entre a gaxeta e a luva.
- **Soluções:** gaxeta de aramida (resistente a abrasivos); **lavagem com água limpa** pelo anel lanterna, a pressão um pouco maior que a da caixa, impedindo a entrada de areia; luva com revestimento duro (cerâmica ou carbonetos por aspersão térmica).

> [!question] Exercício
>
> Por que as juntas dos anéis de gaxeta devem ficar defasadas, e por que não se deve apertar até zerar o vazamento?
>
> > [!success]- Resolução
> >
> > **Defasagem:** se as juntas ficarem alinhadas, formam um caminho direto para o vazamento. Defasando 90°–120°, o fluido precisa percorrer um labirinto.
> > **Vazamento zero:** sem o gotejamento, não há lubrificação nem refrigeração no contato; a gaxeta aquece, endurece e queima, e a luva se desgasta rapidamente.

## Erros comuns

- **Apertar demais a sobreposta.**
- **Juntas dos anéis alinhadas.**
- **Enrolar a gaxeta em espiral contínua** em vez de anéis cortados.
- **Sem lavagem** em fluidos com sólidos.

## Ver também

- [[Selos mecânicos]]
- [[Retentores]]
- [[08-unioes-vedacoes/index|Índice do módulo 08]]
