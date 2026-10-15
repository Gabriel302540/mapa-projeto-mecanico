---
title: Processos de soldagem
tags: [fabricacao, soldagem]
fontes: [Marques, Modenesi e Bracarense Soldagem: Fundamentos e Tecnologia (caps. de processos), AWS Welding Handbook vol. 2 (processos), AWS A5.1 e A5.18 e A5.20 (classificação de consumíveis), AWS D1.1 (estruturas de aço), ASME Seção IX (qualificação)]
status: rascunho
---

**Resumo:** a soldagem a arco une peças metálicas fundindo localmente o metal de base e um metal de adição, protegidos da atmosfera por gás ou escória. Os processos mais usados na caldeiraria e na manutenção são eletrodo revestido, MIG/MAG, arame tubular, TIG e arco submerso. Cada um tem vantagens de produtividade, posição, qualidade e uso em campo.

## O que é

### Principais processos a arco

| Processo | Sigla | Proteção | Pontos fortes | Limitações | Uso típico |
|---|---|---|---|---|---|
| **Eletrodo revestido** | SMAW | Escória e gases do revestimento | Versátil, equipamento simples, **campo**, todas as posições | Baixa produtividade, troca de eletrodos, escória | Manutenção, montagem em campo, estruturas |
| **MIG/MAG** (arame sólido) | GMAW | Gás (Ar, CO₂, misturas) | Alta produtividade, sem escória | Sensível a vento (campo), equipamento mais complexo | Caldeiraria em oficina |
| **Arame tubular** | FCAW | Fluxo interno (+ gás ou autoprotegido) | Alta produtividade, boa penetração, versões para campo | Escória, fumos | Estruturas, revestimento duro |
| **TIG** | GTAW | Gás inerte (argônio) | **Qualidade alta**, controle fino, inox e alumínio, passes de raiz | Lento, exige habilidade | Tubulações, inox, raízes de juntas críticas |
| **Arco submerso** | SAW | Fluxo granulado | **Altíssima produtividade**, ótima qualidade em chapas grossas | Só posição plana/horizontal, automatizado | Vigas, vasos, revestimento de rolos |

### Consumíveis — exemplos de classificação AWS

- **E7018** (eletrodo revestido): **70** ksi de resistência mínima (≈ 480 MPa), **1** = todas as posições, **8** = revestimento básico de baixo hidrogênio (precisa ser mantido em estufa).
- **E6013**: 60 ksi, todas as posições, rutílico; fácil de usar, para serviços leves.
- **ER70S-6** (MIG/MAG): arame sólido de 70 ksi com desoxidantes.
- **E71T-1** (arame tubular): 70 ksi, todas as posições, com proteção gasosa.

### Aporte térmico

A energia entregue por unidade de comprimento do cordão afeta a microestrutura, a distorção e a tenacidade:

$$
H = \eta\,\frac{U\,I\,60}{1000\,v} \quad [\text{kJ/mm}]
$$

com $U$ em volts, $I$ em ampères, $v$ em mm/min e $\eta$ o rendimento térmico do processo (≈ 0,8 para SMAW e GMAW; ≈ 1,0 para SAW; ≈ 0,6 para TIG). ⚠️ verificar os rendimentos na norma de referência.

### Qualificação

- **EPS (especificação de procedimento de soldagem / WPS):** documento com os parâmetros a seguir.
- **RQPS (registro de qualificação do procedimento / PQR):** prova de que o procedimento gera soldas com as propriedades exigidas (ensaios mecânicos).
- **Qualificação de soldadores:** teste prático para cada processo, posição e faixa de espessura.

Códigos como **AWS D1.1** (estruturas) e **ASME IX** (vasos, caldeiras, tubulações) definem as regras.

## Por que importa no projeto

- **O processo influencia o projeto da junta** (chanfro, acesso, posição). Ver [[Juntas e chanfros]].
- **Distorção:** soldas grandes e assimétricas empenam a peça. O projeto deve equilibrar soldas e prever sobremetal ou sequência.
- **Manutenção em campo:** eletrodo revestido e arame tubular autoprotegido são os mais usados.
- **Equipamentos sob pressão** exigem procedimentos e soldadores qualificados.

## Como aplicar (passo a passo / regras práticas)

1. **Escolha o processo** pelo material, espessura, posição, local (oficina ou campo) e volume de solda.
2. **Escolha o consumível** compatível com a resistência do metal de base (normalmente igual ou levemente superior).
3. **Defina pré-aquecimento** pelo carbono equivalente e espessura (ver [[Aços estruturais]]).
4. **Exija EPS qualificada** para soldas estruturais e de pressão.
5. **Indique a solda no desenho** pela simbologia (ver [[Simbologia de soldagem]]).

## Norma relacionada

- **AWS D1.1**: soldagem de estruturas de aço.
- **ASME Seção IX**: qualificação de procedimentos e soldadores (pressão).
- **AWS A5.1** (eletrodos de aço carbono), **A5.18** (arames sólidos), **A5.20** (arames tubulares).
- **ISO 4063**: numeração dos processos de soldagem (111 = eletrodo revestido; 135 = MAG; 136 = arame tubular; 141 = TIG; 121 = arco submerso). ⚠️ verificar.

## Exemplo prático

**Situação:** soldagem MAG de uma estrutura com **28 V**, **250 A** e velocidade de **300 mm/min**, rendimento 0,8.

$$
H = 0{,}8 \times \frac{28 \times 250 \times 60}{1000 \times 300} = 1{,}12\ \text{kJ/mm}
$$

Esse valor é registrado na EPS e comparado com os limites do procedimento qualificado (aporte muito alto reduz a tenacidade da zona afetada pelo calor em alguns aços; muito baixo aumenta o risco de trincas em aços temperáveis).

> [!question] Exercício
>
> O que significam os números de um eletrodo E7018 e por que ele precisa ser guardado em estufa?
>
> > [!success]- Resolução
> >
> > - **70**: resistência à tração mínima do metal depositado de 70 ksi (≈ 480 MPa).
> > - **1**: soldável em todas as posições.
> > - **8**: revestimento básico, de **baixo hidrogênio**, com pó de ferro.
> >
> > O revestimento absorve **umidade** do ar; a umidade se decompõe no arco e libera **hidrogênio**, que causa **trincas a frio** na solda e na zona afetada pelo calor. Por isso ele é mantido em estufa e ressecado conforme o fabricante.

## Erros comuns

- **E7018 sem estufa** ou reaproveitado depois de exposto à umidade.
- **MIG/MAG em campo com vento** (porosidade).
- **Soldar sem pré-aquecimento** aços de CE alto.
- **Ignorar a qualificação** em soldas estruturais e de pressão.

## Ver também

- [[Simbologia de soldagem]]
- [[Juntas e chanfros]]
- [[Aços estruturais]]
- [[Revestimento duro]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
