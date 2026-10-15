---
title: Classificação dos aços (SAE/AISI)
tags: [materiais, acos]
fontes: [SAE J403 (aços carbono — composição), SAE J404 (aços ligados — composição), ABNT NBR NM 87 (aços carbono e ligados para construção mecânica — designação e composição) ⚠️ verificar, Chiaverini Aços e Ferros Fundidos (cap. de classificação), ASM Handbook vol. 1]
status: rascunho
---

**Resumo:** os aços para construção mecânica são designados no Brasil principalmente pelo sistema SAE/AISI, de quatro dígitos: os dois primeiros indicam a família (carbono, Cr-Mo, Ni-Cr-Mo...) e os dois últimos, o teor de carbono em centésimos de por cento. Outros sistemas (DIN/EN, ASTM, UNS) aparecem em desenhos estrangeiros e para aplicações específicas.

## O que é

### Sistema SAE/AISI

**XXYY**: XX = família; YY = carbono × 100.

| Família | Elementos principais | Exemplos | Uso típico |
|---|---|---|---|
| **10XX** | Aço carbono comum | 1010, 1020, 1045, 1060 | Peças gerais, eixos, chapas |
| **11XX** | Carbono ressulfurado | 1117, 1141 | Usinagem fácil (automáticos) |
| **12XX** | Ressulfurado e refosforado | 12L14 (com chumbo) | Usinagem muito fácil, pouca solicitação |
| **13XX** | Manganês (≈ 1,75 %) | 1340 | Peças com temperabilidade média |
| **41XX** | Cromo-molibdênio | **4140**, 4130 | Eixos, engrenagens, parafusos de alta resistência |
| **43XX** | Níquel-cromo-molibdênio | **4340** | Eixos grandes e muito solicitados, alta tenacidade |
| **51XX** | Cromo | 5160 | Molas, peças temperadas |
| **52XXX** | Cromo, alto carbono | **52100** | Rolamentos |
| **61XX** | Cromo-vanádio | 6150 | Molas, ferramentas |
| **86XX** | Níquel-cromo-molibdênio (baixo) | **8620**, 8640 | Engrenagens cementadas |
| **92XX** | Silício-manganês | 9260 | Molas |

Letras no meio: **B** (boro, aumenta a temperabilidade), **L** (chumbo, usinabilidade). Prefixo **E**: aço de forno elétrico.

### Outros sistemas

| Sistema | Exemplo | Equivalente aproximado |
|---|---|---|
| EN/DIN (nome) | C45, 42CrMo4, 34CrNiMo6 | SAE 1045, 4140, ≈ 4340 |
| EN (número) | 1.0503, 1.7225 | C45, 42CrMo4 |
| UNS | G10450, G41400 | SAE 1045, 4140 |
| ASTM (produtos) | A36, A572, A516 | Aços estruturais e de vasos, por **propriedade**, não por composição |

As equivalências são **aproximadas**: faixas de composição e exigências de propriedades diferem. ⚠️ verificar sempre a norma de cada material.

### Composição × propriedade

- **SAE/AISI** define principalmente a **composição química**. As propriedades mecânicas dependem do **estado** (laminado a quente, trefilado a frio, normalizado, beneficiado). Por isso, no desenho, especifica-se material **e** condição: "SAE 4140 temperado e revenido 28–32 HRC".
- **ASTM A36, A572** etc. especificam **propriedades mínimas** (escoamento, ruptura) e composição máxima.

## Por que importa no projeto

- **Especificação inequívoca** no desenho e na compra.
- **Peças de reposição de equipamentos importados** vêm com designações DIN, EN, JIS; é preciso saber traduzir.
- **Disponibilidade:** no mercado brasileiro, 1020, 1045, 4140 e 4340 são os aços de construção mecânica mais fáceis de encontrar em barras; 8620 é comum para engrenagens.

## Como aplicar (passo a passo / regras práticas)

1. Escolha o material pela função (ver [[Seleção de materiais]] e [[Aços para construção mecânica]]).
2. Especifique a **designação** e a **condição** (tratamento, dureza).
3. Para equivalências estrangeiras, confira a composição nas duas normas.
4. Peça **certificado de material** (composição e ensaios) em peças críticas.

## Norma relacionada

- **SAE J403 / J404**: composição química de aços carbono e ligados.
- **ABNT NBR NM 87**: aços carbono e ligados para construção mecânica (designação e composição). ⚠️ verificar edição vigente.
- **EN 10083**: aços para têmpera e revenido (C45, 42CrMo4, 34CrNiMo6...).

## Exemplo prático

**Situação:** um eixo importado tem no desenho o material **42CrMo4 V** (beneficiado). Qual aço nacional usar na reposição?

- 42CrMo4 é equivalente aproximado ao **SAE 4140** (Cr-Mo, 0,38–0,45 % C).
- "V" (*vergütet*) = **beneficiado** (temperado e revenido).
- Especificação: **SAE 4140 temperado e revenido**, com a faixa de resistência ou dureza do desenho original (por exemplo, 900–1100 MPa ou ≈ 28–34 HRC ⚠️ verificar), e certificado de material.

> [!question] Exercício
>
> Decodifique: SAE 1045, SAE 4340, SAE 8620 e SAE 52100.
>
> > [!success]- Resolução
> >
> > - **1045:** aço carbono comum, 0,45 % C.
> > - **4340:** Ni-Cr-Mo, 0,40 % C. Alta temperabilidade e tenacidade.
> > - **8620:** Ni-Cr-Mo (baixo teor), 0,20 % C. Aço para cementação.
> > - **52100:** Cr, 1,00 % C (aqui os três últimos dígitos indicam o carbono). Aço para rolamentos.

## Erros comuns

- **Especificar só "SAE 4140"** sem a condição (pode chegar recozido, mole).
- **Tratar equivalências como idênticas.**
- **Confundir ASTM A36** (estrutural, propriedade) com SAE 1020 (composição): são parecidos, mas não iguais.

## Ver também

- [[Aços para construção mecânica]]
- [[Aços estruturais]]
- [[Diagrama ferro-carbono]]
- [[06-materiais/index|Índice do módulo 06]]
