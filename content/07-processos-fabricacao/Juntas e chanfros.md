---
title: Juntas e chanfros
tags: [fabricacao, soldagem]
fontes: [AWS D1.1 (juntas pré-qualificadas), ISO 9692-1 (preparação de juntas para soldagem de aços) ⚠️ verificar, Marques, Modenesi e Bracarense Soldagem: Fundamentos e Tecnologia (cap. de juntas), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 9 — soldagem e uniões)]
status: rascunho
---

**Resumo:** a junta soldada é definida pelo tipo de ligação entre as peças (topo, T, sobreposta, canto) e pela preparação das bordas (chanfro). O chanfro permite que a solda penetre na espessura; sua forma define o volume de metal depositado, a distorção e o custo. Filetes são dimensionados pela garganta.

## O que é

### Tipos de junta

| Junta | Arranjo | Soldas usuais |
|---|---|---|
| **De topo** | Peças no mesmo plano, encostadas pelas bordas | Chanfro (I, V, X, U) |
| **Em T** | Uma peça perpendicular à outra | Filete ou chanfro (bisel, K) |
| **Sobreposta** | Peças sobrepostas | Filete |
| **De canto** | Bordas formando um canto | Filete ou chanfro |
| **De aresta** | Bordas paralelas lado a lado | Chapas finas |

### Chanfros para juntas de topo

| Chanfro | Espessura típica (SMAW/GMAW) | Características |
|---|---|---|
| **I** (bordas retas) | até ≈ 3–6 mm | Sem preparação; abertura de raiz controlada |
| **V simples** (60°) | ≈ 6–20 mm | Simples de preparar; distorção angular |
| **X (duplo V)** | > ≈ 20 mm | Cerca de metade do metal depositado do V; distorção equilibrada; exige acesso aos dois lados |
| **U / J** | Chapas grossas | Menos metal depositado; preparação usinada |
| **Bisel / K** (juntas T) | Conforme espessura | Penetração total em juntas em T |

Elementos do chanfro: **ângulo do chanfro**, **abertura de raiz** (folga entre as peças), **nariz** (face de raiz não chanfrada) e, às vezes, **cobre-junta** (tira no fundo). ⚠️ verificar dimensões das juntas pré-qualificadas na AWS D1.1 ou ISO 9692-1.

### Penetração total × parcial

- **Penetração total:** a solda ocupa toda a espessura; resistência igual à da chapa (com metal de adição compatível).
- **Penetração parcial:** só parte da espessura; mais barata, mas com resistência e comportamento à fadiga menores.

### Dimensionamento simplificado de filetes

A tensão no filete é calculada na **garganta**:

$$
\tau = \frac{F}{a\,L}
$$

com $a = 0{,}707\,z$ (garganta) e $L$ o comprimento total de solda efetiva. Compara-se com a tensão admissível do metal de solda conforme o código (por exemplo, na AWS D1.1, 0,30 × a resistência do eletrodo para filetes, em projeto por tensões admissíveis). ⚠️ verificar no código aplicável.

**Regras práticas para filetes:**
- Perna mínima em função da espessura da chapa mais grossa (para garantir fusão).
- Perna máxima ao longo de bordas: espessura da chapa menos ≈ 2 mm (para chapas ≥ 6 mm).
- Filetes maiores que o necessário aumentam distorção e custo sem ganho.

## Por que importa no projeto

- **Volume de solda = custo e distorção.** O volume cresce com o quadrado da espessura em chanfros em V.
- **Fadiga:** juntas soldadas são pontos críticos em estruturas vibrantes (peneiras, transportadores). Penetração total, acabamento do cordão e posição da junta fora das zonas de tensão máxima ajudam.
- **Acesso:** chanfros em X exigem acesso pelos dois lados; o projeto deve permitir.

## Como aplicar (passo a passo / regras práticas)

1. **Defina se a junta precisa de penetração total** (cargas altas, fadiga, estanqueidade).
2. **Escolha o chanfro** pela espessura e acesso: I (finas), V (médias), X (grossas com acesso), U/J (muito grossas).
3. **Dimensione filetes** pela garganta; não exagere.
4. **Equilibre soldas** em torno do eixo neutro para reduzir distorção.
5. **Indique pela simbologia** e referencie a EPS. Ver [[Simbologia de soldagem]].

## Norma relacionada

- **AWS D1.1**: juntas pré-qualificadas, tamanhos mínimos de filetes, tensões admissíveis.
- **ISO 9692-1**: tipos de preparação de juntas para aços. ⚠️ verificar.
- **ISO 13920**: tolerâncias gerais de construções soldadas.

## Exemplo prático

**Situação 1 — volume de solda:** junta de topo em chapa de **25 mm**, abertura de raiz de 2 mm e nariz de 2 mm.

- **V simples de 60°:** área ≈ $2 \times 25 + 23^2 \tan 30° \approx 50 + 305 = 355$ mm²
- **X simétrico (60° dos dois lados):** área ≈ $50 + 2 \times 11{,}5^2 \tan 30° \approx 50 + 153 = 203$ mm²

O chanfro em X reduz o metal depositado em **cerca de 43 %** e equilibra a distorção. (Cálculo simplificado, sem reforço do cordão.)

**Situação 2 — filete:** um suporte transmite **60 kN** por dois filetes de **150 mm** com perna de **6 mm**.

- $a = 0{,}707 \times 6 \approx 4{,}24$ mm
- $\tau = \dfrac{60\,000}{4{,}24 \times 300} \approx 47$ MPa

Para eletrodo E70 (≈ 480 MPa), a admissível na AWS (0,30 × 480 ≈ 144 MPa) dá folga ampla. ⚠️ verificar o critério do código e eventuais combinações de esforços.

> [!question] Exercício
>
> Qual o comprimento mínimo de filete com perna de 5 mm para transmitir 40 kN, com tensão admissível de 140 MPa na garganta?
>
> > [!success]- Resolução
> >
> > $a = 0{,}707 \times 5 \approx 3{,}54$ mm.
> > $L = \dfrac{F}{a\,\tau_{\text{adm}}} = \dfrac{40\,000}{3{,}54 \times 140} \approx 81$ mm (comprimento efetivo total). Na prática, acrescentam-se alguns milímetros por causa das extremidades do cordão.

## Erros comuns

- **Filete superdimensionado** "por segurança", gerando distorção.
- **Chanfro em V em chapas muito grossas** (excesso de solda e distorção).
- **Penetração parcial em juntas sob fadiga.**
- **Calcular o filete pela perna** em vez da garganta.

## Ver também

- [[Processos de soldagem]]
- [[Simbologia de soldagem]]
- [[08-unioes-vedacoes/index|Uniões soldadas]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
