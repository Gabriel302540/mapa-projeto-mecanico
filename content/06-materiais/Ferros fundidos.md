---
title: Ferros fundidos cinzento e nodular
tags: [materiais, ferros-fundidos]
fontes: [ISO 185 (ferro fundido cinzento), ISO 1083 (ferro fundido nodular), ABNT NBR 6589 e NBR 6916 ⚠️ verificar, ASTM A48 e A536, Chiaverini Aços e Ferros Fundidos (cap. de ferros fundidos), Callister e Rethwisch Ciência e Engenharia de Materiais]
status: rascunho
---

**Resumo:** ferros fundidos são ligas de ferro com mais de 2 % de carbono, fáceis de fundir em formas complexas. No cinzento, o carbono forma lamelas de grafita, que dão boa usinabilidade e amortecimento de vibrações, mas fragilidade em tração. No nodular, a grafita forma esferas, e o material ganha resistência e ductilidade próximas às de um aço.

## O que é

### Tipos

| Tipo | Forma do carbono | Propriedades principais | Uso típico |
|---|---|---|---|
| **Cinzento** | Grafita em **lamelas** | Boa resistência à compressão, ótimo amortecimento, ótima usinabilidade, baixa resistência à tração e **ductilidade quase nula** | Bases e barramentos de máquinas, carcaças de redutores e bombas, polias, discos de freio, camisas e rolos |
| **Nodular (dúctil)** | Grafita em **esferas** | Resistência e alongamento próximos aos de aços; boa tenacidade | Engrenagens grandes, cubos, virabrequins, carcaças sujeitas a impacto, tubos |
| **Branco** | Carbono como **cementita** | Muito duro e frágil, resistente à abrasão | Peças de desgaste (ou camada coquilhada) |
| **Branco ligado (alto cromo)** | Carbonetos de cromo | Altíssima resistência à abrasão | Revestimentos de moinhos, martelos, bombas de polpa |
| **Maleável** | Grafita em nódulos irregulares (por recozimento do branco) | Dúctil | Conexões, peças pequenas (uso decrescente) |

### Classes (designação pela resistência)

| Cinzento (ISO 185) | $S_{ut}$ mín. (MPa) | Nodular (ISO 1083) | $S_{ut}$ (MPa) / alongamento (%) |
|---|---|---|---|
| 150 | 150 | 400-15 | 400 / 15 |
| 200 | 200 | 450-10 | 450 / 10 |
| **250** | 250 | **500-7** | 500 / 7 |
| 300 | 300 | 600-3 | 600 / 3 |
| 350 | 350 | 700-2 | 700 / 2 |

No Brasil: cinzento **FC 200, FC 250**... (NBR 6589) e nodular **FE 42012, FE 50007, FE 60003**... (NBR 6916). ⚠️ verificar as designações e valores nas normas.

### Particularidades de projeto

- **Resistência depende da espessura:** paredes finas resfriam rápido e ficam mais duras (até coquilhadas); paredes grossas ficam mais moles.
- **Projeto para fundição:** espessuras uniformes, raios generosos, ângulos de saída, sobremetal de usinagem. Ver [[07-processos-fabricacao/index|Processos de fabricação]].
- **Soldagem:** possível, mas difícil (eletrodos de níquel, pré-aquecimento); o cinzento é especialmente sensível a trincas.
- **Módulo de elasticidade do cinzento** é menor e não linear (≈ 80 a 140 GPa conforme a classe), contra ≈ 170 GPa do nodular e 205 GPa do aço.

## Por que importa no projeto

- **Carcaças e bases:** o amortecimento do cinzento reduz vibração e ruído.
- **Rolos e camisas** de equipamentos de esmagamento e moagem são comumente de ferro fundido, pela fundibilidade em peças grandes, pela resistência à compressão e pela facilidade de usinar frisos.
- **Substituir uma peça soldada por fundida** (ou o contrário) muda completamente as regras de projeto.

## Como aplicar (passo a passo / regras práticas)

1. **Cinzento** para peças em compressão, com vibração a amortecer e sem impacto severo.
2. **Nodular** quando houver tração, flexão, impacto, ou quando se quiser um "aço fundido" mais barato e usinável.
3. **Branco ligado** para abrasão severa.
4. **Especifique a classe** e as superfícies de referência para usinagem (alvos de referência; ver [[Referências geométricas]]).
5. **Evite soldas de reparo** em peças críticas de cinzento sem procedimento especializado.

## Norma relacionada

- **ISO 185 / ASTM A48**: ferro fundido cinzento.
- **ISO 1083 / ASTM A536**: ferro fundido nodular.
- **ASTM A532**: ferros fundidos brancos resistentes à abrasão.
- **ABNT NBR 6589 / NBR 6916**: cinzento e nodular. ⚠️ verificar.

## Exemplo prático

**Situação:** a carcaça de um redutor pequeno trincou após um travamento do equipamento (choque). Ela era de **ferro fundido cinzento FC 200**.

- O cinzento tem alongamento praticamente nulo: sob choque, não deforma, trinca.
- **Opções de reprojeto:** carcaça de **nodular FE 50007** (mesmo modelo de fundição, com 7 % de alongamento) ou carcaça **soldada** de chapas de A36.
- Mesmo com material melhor, é preciso proteger o acionamento contra o pico de torque (acoplamento com limitador de torque, ou acoplamento hidráulico).

> [!question] Exercício
>
> Cite duas vantagens e duas desvantagens do ferro fundido cinzento em relação ao aço para uma base de máquina.
>
> > [!success]- Resolução
> >
> > **Vantagens:** excelente **amortecimento de vibrações**; ótima **usinabilidade**; fácil de obter **formas complexas** por fundição; boa resistência à compressão; custo baixo em série.
> > **Desvantagens:** **frágil** (não suporta choques nem tração alta); **difícil de soldar** em reparos; exige modelo de fundição (custo inicial e prazo); módulo de elasticidade menor (mais flexível que uma base de aço de mesma forma).

## Erros comuns

- **Usar cinzento em peças sob impacto ou tração alta.**
- **Soldar cinzento** como se fosse aço.
- **Ignorar a variação de propriedades com a espessura** da parede.
- **Especificar só "ferro fundido"** sem a classe.

## Ver também

- [[Diagrama ferro-carbono]]
- [[Revestimento duro]]
- [[Seleção de materiais]]
- [[06-materiais/index|Índice do módulo 06]]
