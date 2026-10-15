---
title: Aços inoxidáveis
tags: [materiais, acos, corrosao]
fontes: [ASTM A240 (chapas inoxidáveis), ASTM A276 (barras inoxidáveis), Chiaverini Aços e Ferros Fundidos (cap. de aços inoxidáveis), Callister e Rethwisch Ciência e Engenharia de Materiais (cap. de corrosão), ASM Handbook vol. 13 (corrosão)]
status: rascunho
---

**Resumo:** aços inoxidáveis contêm pelo menos cerca de 10,5 % de cromo, que forma na superfície uma película fina de óxido que se regenera sozinha e protege contra a corrosão. Há cinco famílias — austeníticos, ferríticos, martensíticos, duplex e endurecíveis por precipitação — com combinações diferentes de resistência à corrosão, resistência mecânica e soldabilidade.

## O que é

### Famílias

| Família | Exemplos | Composição típica | Pontos fortes | Limitações |
|---|---|---|---|---|
| **Austeníticos** | **304, 304L, 316, 316L** | 18 % Cr, 8–10 % Ni (316: + 2–3 % Mo) | Excelente resistência à corrosão, soldabilidade, tenacidade; não magnéticos | Resistência mecânica moderada; não endurecem por têmpera; sujeitos a corrosão sob tensão em cloretos |
| **Ferríticos** | 430 | 16–18 % Cr, sem Ni | Baratos, resistentes à corrosão sob tensão | Soldabilidade e tenacidade limitadas |
| **Martensíticos** | **410, 420**, 440C | 12–18 % Cr, carbono mais alto | **Temperáveis**: dureza alta | Corrosão inferior aos austeníticos |
| **Duplex** | **2205** | 22 % Cr, 5 % Ni, 3 % Mo, N | Resistência mecânica ≈ 2× a dos austeníticos; ótima contra cloretos | Soldagem com controle; mais caro |
| **Endurecíveis por precipitação** | **17-4PH** | 17 % Cr, 4 % Ni, Cu | Alta resistência com boa corrosão | Caro; tratamento específico |

**"L"** (304L, 316L): baixo carbono (≤ 0,03 %), que evita a **sensitização** na soldagem.

### Formas de corrosão importantes

- **Sensitização:** entre cerca de 450 e 850 °C (zona afetada pela solda), o cromo forma carbonetos nos contornos de grão e deixa regiões sem proteção → corrosão intergranular. Prevenção: graus L ou estabilizados (321, 347).
- **Pite (*pitting*):** furos localizados em meios com cloretos. O molibdênio (316, duplex) aumenta a resistência.
- **Frestas:** corrosão em espaços estreitos e estagnados (sob juntas, parafusos).
- **Corrosão sob tensão:** trincas em austeníticos sob tensão em meios com cloretos e temperatura.
- **Corrosão galvânica:** quando o inox está em contato elétrico com um metal menos nobre (aço carbono, alumínio) num eletrólito, o metal menos nobre corrói mais rápido.

### Contaminação

Ferramentas, escovas e discos que já trabalharam aço carbono deixam partículas de ferro no inox, que enferrujam e iniciam corrosão. Usa-se ferramental exclusivo e, se necessário, **decapagem e passivação** após a fabricação.

## Por que importa no projeto

- **Indústrias de alimentos, bebidas, química e de processamento de produtos ácidos** usam muito inox em tubulações, tanques, peneiras e eixos de bombas.
- **Eixos de bombas e agitadores** em meios corrosivos: 410/420 temperados (resistência) ou 316/duplex (corrosão).
- **Custo:** inox custa várias vezes mais que aço carbono; usar só onde a corrosão justifica (ou como revestimento/chapa de desgaste).

## Como aplicar (passo a passo / regras práticas)

1. **Meio pouco agressivo, sem cloretos:** 304 (ou 304L se soldado).
2. **Cloretos, ácidos orgânicos, ambiente marinho:** 316L.
3. **Precisa de dureza (eixos, facas, sedes):** 410 ou 420 temperado.
4. **Cloretos + alta resistência mecânica:** duplex 2205.
5. **Projete evitando frestas** e pontos de acúmulo; prefira soldas contínuas.
6. **Evite contato direto com aço carbono** (isolar ou usar o mesmo material); especifique **decapagem e passivação**.

## Norma relacionada

- **ASTM A240**: chapas e tiras de aço inoxidável.
- **ASTM A276 / A479**: barras e perfis.
- **ASTM A380 / A967**: limpeza, decapagem e passivação. ⚠️ verificar.

## Exemplo prático

**Situação:** escolher material para uma **peneira de caldo** e seus suportes, em contato com um líquido ácido e quente, com lavagens frequentes.

- **Tela e estrutura molhada:** 304L, ou **316L** se houver cloretos ou acidez mais forte (conferir a análise do fluido).
- **Soldas** com metal de adição compatível (308L para 304L; 316L para 316L), seguidas de decapagem.
- **Parafusos:** inox A4 (316) para evitar par galvânico com a estrutura.
- **Suportes secos e afastados do fluido:** aço carbono pintado, isolado eletricamente do inox.

> [!question] Exercício
>
> Por que, ao soldar uma chapa de 304 comum, a região ao lado do cordão pode corroer mais rápido que o resto da chapa? Como evitar?
>
> > [!success]- Resolução
> >
> > A região aquecida entre cerca de 450 e 850 °C sofre **sensitização**: o carbono se combina com o cromo formando carbonetos nos contornos de grão, e o entorno fica com pouco cromo, sem proteção. Resultado: corrosão intergranular ao lado da solda. **Prevenção:** usar **304L** (baixo carbono) ou aço estabilizado (321, 347), e controlar o aporte de calor.

## Erros comuns

- **Achar que inox não enferruja em nenhuma condição.**
- **Usar 304 em meios com cloretos** (pite, corrosão sob tensão).
- **Ferramentas contaminadas com aço carbono.**
- **Par galvânico inox–aço carbono** sem isolamento.
- **Inox martensítico em meio muito agressivo**, esperando a resistência à corrosão de um austenítico.

## Ver também

- [[Classificação dos aços]]
- [[Seleção de materiais]]
- [[07-processos-fabricacao/index|Processos de fabricação]]
- [[06-materiais/index|Índice do módulo 06]]
