---
title: Seleção de materiais
tags: [materiais, metodologia]
fontes: [Ashby Materials Selection in Mechanical Design (caps. 4 a 6), Callister e Rethwisch Ciência e Engenharia de Materiais (cap. de seleção de materiais), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 2 — materiais), Chiaverini Aços e Ferros Fundidos]
status: rascunho
---

**Resumo:** selecionar um material é traduzir a função da peça em requisitos (resistência, rigidez, desgaste, corrosão, temperatura, soldabilidade, custo), eliminar os materiais que não atendem e classificar os restantes. O método de Ashby formaliza isso com índices de mérito; no dia a dia, um roteiro de perguntas e uma tabela de escolhas usuais resolvem a maioria dos casos.

## O que é

### Método de Ashby (resumo)

1. **Tradução:** função (o que a peça faz), restrições (o que não pode acontecer), objetivo (o que minimizar ou maximizar: peso, custo) e variáveis livres.
2. **Triagem:** eliminar materiais que violam restrições (temperatura máxima, corrosão, soldabilidade).
3. **Classificação:** ordenar pelos **índices de mérito**. Exemplos:

| Objetivo | Índice a maximizar |
|---|---|
| Tirante leve e rígido | $E/\rho$ |
| Viga leve e rígida (flexão) | $E^{1/2}/\rho$ |
| Viga leve e resistente | $\sigma_f^{2/3}/\rho$ |
| Mola que armazena muita energia por volume | $\sigma_f^2/E$ |
| Peça barata e resistente em tração | $\sigma_f/(C_m\,\rho)$ ($C_m$ = custo por kg) |

4. **Documentação:** verificar disponibilidade, histórico de uso, fornecimento, normas, processos.

### Roteiro prático de perguntas

1. Que **cargas** a peça sofre (estática, fadiga, choque)?
2. Há **desgaste**? De que tipo?
3. Há **corrosão** (umidade, ácidos, cloretos)?
4. Qual a **temperatura** de operação?
5. Como a peça será **fabricada** (usinada, soldada, fundida, conformada)?
6. Precisa de **tratamento térmico**?
7. **Quantas** peças? (fundição compensa em série; usinagem de barra em peças únicas)
8. O material está **disponível** em estoque ou no mercado, nas bitolas necessárias?
9. Qual o **custo total** (material + fabricação + manutenção + parada)?

### Escolhas usuais em equipamentos industriais

| Peça | Material típico | Observação |
|---|---|---|
| Estrutura, base, chute | ASTM A36 | Soldável e barato. Ver [[Aços estruturais]] |
| Eixo de transmissão médio/grande | SAE 4140 ou 4340 beneficiado | Fadiga. Ver [[Aços para construção mecânica]] |
| Eixo simples, pouco solicitado | SAE 1045 | |
| Pino com desgaste | 4140 beneficiado + indução | Ver [[Tratamentos superficiais]] |
| Engrenagem muito carregada | 8620 cementado ou 4140 nitretado | |
| Bucha de deslizamento | Bronze (SAE 660 e similares) ou autolubrificante | Ver [[Mancais de deslizamento]] |
| Carcaça, base com vibração | Ferro fundido cinzento ou chapa soldada | Ver [[Ferros fundidos]] |
| Peça em meio ácido ou úmido | Inox 304L / 316L | Ver [[Aços inoxidáveis]] |
| Superfície de desgaste abrasivo | Revestimento duro sobre aço tenaz, chapas antidesgaste (≈ 400–500 HB) | Ver [[Revestimento duro]] |
| Mola | Arame de aço para molas, Cr-Si | Ver [[Molas helicoidais]] |

## Por que importa no projeto

- **O material é responsável por boa parte do custo** e da vida da peça.
- **Material errado é causa frequente de falha**, principalmente em peças de reposição feitas "com o que tinha".
- **Padronizar materiais** simplifica compras, estoque e especificações.

## Como aplicar (passo a passo / regras práticas)

1. Escreva a **função** e os **requisitos** da peça.
2. Responda ao roteiro de perguntas.
3. Liste 2 ou 3 candidatos e compare propriedades, processos e custo.
4. Prefira materiais **padronizados no estoque** e conhecidos pela oficina.
5. Especifique material, condição e tratamento no desenho e na lista de materiais. Ver [[Classificação dos aços]].
6. Para peças críticas, peça **certificado de material** e ensaios.

## Norma relacionada

Não há norma única de seleção. Os dados vêm das **normas dos materiais** (SAE, ASTM, EN, ISO), de **catálogos de produtores** e de **bancos de dados** de materiais.

## Exemplo prático

**Situação:** escolher o material de uma **chapa de desgaste** que reveste um chute por onde passa material abrasivo, com impacto leve.

| Candidato | Prós | Contras |
|---|---|---|
| A36 comum | Barato, fácil de soldar e cortar | Desgasta rápido |
| Chapa antidesgaste (≈ 400 HB, temperada) | 3 a 5 vezes mais vida que o A36 em abrasão (ordem de grandeza ⚠️) | Mais cara; exige cuidado na soldagem e na dobra |
| A36 com revestimento duro de carbonetos de cromo | Vida ainda maior em abrasão pura | Mais caro; trincas de alívio; difícil de conformar |
| Inox 304 | Resiste à corrosão | Não resiste bem à abrasão; caro |

**Escolha:** **chapa antidesgaste ≈ 400 HB**, parafusada (parafusos de cabeça escareada) para troca fácil. Se o desgaste ainda for alto, avaliar revestimento duro nas regiões de impacto do fluxo.

> [!question] Exercício
>
> Pelo índice de mérito $E^{1/2}/\rho$, compare aço ($E$ = 205 GPa, $\rho$ = 7850 kg/m³) e alumínio ($E$ = 70 GPa, $\rho$ = 2700 kg/m³) para uma viga leve e rígida.
>
> > [!success]- Resolução
> >
> > - Aço: $\sqrt{205}/7850 = 14{,}3/7850 \approx 1{,}82\times10^{-3}$
> > - Alumínio: $\sqrt{70}/2700 = 8{,}37/2700 \approx 3{,}10\times10^{-3}$
> >
> > O alumínio tem índice cerca de **70 % maior**: para a mesma rigidez à flexão, a viga de alumínio (com seção maior) fica mais leve. Se o objetivo fosse custo, e não peso, o aço provavelmente venceria.

## Erros comuns

- **Escolher pelo hábito** ("sempre usamos 1045").
- **Olhar só a resistência** e esquecer desgaste, corrosão e fabricação.
- **Especificar materiais difíceis de encontrar** nas bitolas necessárias.
- **Não considerar o custo da parada** do equipamento na comparação.

## Ver também

- [[Aços para construção mecânica]]
- [[Classificação dos aços]]
- [[09-metodologia-de-projeto/index|Metodologia de projeto]]
- [[06-materiais/index|Índice do módulo 06]]
