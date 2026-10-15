---
title: "Rolamentos: vida nominal"
tags: [elementos, rolamentos]
fontes: [ISO 281:2007, ISO 76 (capacidade estática), catálogos técnicos gerais de rolamentos (seções de cálculo de vida), Budynas e Nisbett Elementos de Máquinas de Shigley (cap. 11), Harris e Kotzalas Rolling Bearing Analysis]
status: rascunho
---

**Resumo:** a vida de um rolamento é o número de rotações (ou horas) até aparecer a primeira fadiga do material nas pistas ou corpos rolantes. A vida nominal L10, atingida por 90 % de um grande lote de rolamentos iguais, é calculada pela razão entre a capacidade de carga dinâmica C (do catálogo) e a carga equivalente P. Fatores de ajuste corrigem a confiabilidade, a lubrificação e a contaminação.

## O que é

### Vida nominal básica

$$
L_{10} = \left(\frac{C}{P}\right)^{p} \quad [\text{milhões de rotações}]
$$

- $C$: capacidade de carga dinâmica básica (catálogo): a carga com a qual 90 % dos rolamentos atingem 1 milhão de rotações.
- $P$: carga dinâmica equivalente.
- $p$ = **3** para rolamentos de esferas; **10/3** para rolamentos de rolos.

Em horas, com rotação $n$ em rpm:

$$
L_{10h} = \frac{10^6}{60\,n}\left(\frac{C}{P}\right)^{p}
$$

**Sensibilidade:** num rolamento de esferas, dobrar a carga divide a vida por 8; reduzir a carga em 20 % praticamente dobra a vida.

### Carga equivalente

Combina carga radial $F_r$ e axial $F_a$:

$$
P = X\,F_r + Y\,F_a
$$

Os fatores $X$ e $Y$ dependem do tipo de rolamento e da relação $F_a/F_r$ comparada com um valor-limite $e$ (tabelados no catálogo). Para rolamentos de rolos cilíndricos sem carga axial, $P = F_r$.

### Vida ajustada (ISO 281)

$$
L_{nm} = a_1\,a_{\text{ISO}}\,L_{10}
$$

**Confiabilidade ($a_1$):**

| Confiabilidade | 90 % | 95 % | 96 % | 97 % | 98 % | 99 % |
|---|---|---|---|---|---|---|
| $a_1$ | 1 | 0,64 | 0,55 | 0,47 | 0,37 | 0,25 |

⚠️ verificar na ISO 281:2007.

**Condições de operação ($a_{\text{ISO}}$):** depende da relação entre a viscosidade do lubrificante na temperatura de operação e a viscosidade mínima necessária (relação $\kappa$), do nível de **contaminação** e do limite de fadiga do material. Pode ser bem maior que 1 (lubrificação boa e limpa) ou bem menor (óleo fino, sujeira, água). Calculado com os diagramas do catálogo.

### Carga estática

Para rotações muito baixas, oscilações ou choques, verifica-se a **capacidade de carga estática** $C_0$:

$$
s_0 = \frac{C_0}{P_0}
$$

Valores mínimos típicos de $s_0$: cerca de 1 em operação suave, 1,5 a 2 com choques, maiores para exigências de silêncio e precisão. ⚠️ verificar no catálogo.

### Vida requerida — referências

| Tipo de máquina | Vida $L_{10h}$ típica (h) |
|---|---|
| Uso intermitente (equipamentos de manutenção, ferramentas) | 3 000 – 8 000 |
| 8 h/dia, não totalmente utilizadas | 10 000 – 25 000 |
| 8 h/dia, totalmente utilizadas | 20 000 – 30 000 |
| Operação contínua 24 h | 40 000 – 50 000 |
| Contínua, com alta confiabilidade exigida | 60 000 – 100 000 |

⚠️ verificar no catálogo do fabricante. Equipamentos que trabalham 24 h durante uma safra de vários meses e param na entressafra podem ser avaliados pelas horas anuais de operação.

## Por que importa no projeto

- **Dimensionar o rolamento** e o diâmetro do eixo naquele ponto.
- **Comparar alternativas** (rolamento maior × lubrificação melhor × vedação melhor).
- **Planejar a manutenção:** a vida calculada orienta a troca preventiva.
- **Diagnosticar falhas:** se o rolamento falhou muito antes da vida calculada, a causa raramente é a fadiga "normal" — procure contaminação, lubrificação, ajuste, desalinhamento ou montagem.

## Como aplicar (passo a passo / regras práticas)

1. **Calcule as reações** nos mancais (radial e axial). Ver [[Dimensionamento estático de eixos]].
2. **Escolha um rolamento candidato** (tipo pelo [[Seleção de rolamentos|critério de seleção]]; tamanho pelo diâmetro do eixo).
3. **Calcule $P$** com X e Y do catálogo.
4. **Calcule $L_{10h}$** e compare com a vida requerida.
5. **Ajuste pela confiabilidade e pelas condições** ($a_1$, $a_{\text{ISO}}$).
6. **Verifique a carga estática** se houver choques ou rotação baixa.
7. **Se a vida for insuficiente:** rolamento de série mais pesada, outro tipo, melhor lubrificação ou vedação.

## Norma relacionada

- **ISO 281:2007**: capacidade de carga dinâmica e vida nominal, com o método de vida ajustada ($a_{\text{ISO}}$).
- **ISO 76**: capacidade de carga estática.
- **ISO/TS 16281**: cálculo avançado da vida considerando folga e desalinhamento. ⚠️ verificar.

## Exemplo prático

**Situação 1 — rolamento de esferas:** motor elétrico a **1450 rpm**, carga equivalente **8 kN**, rolamento com **C = 95,6 kN** (valor ilustrativo).

$$
L_{10} = \left(\frac{95{,}6}{8}\right)^3 \approx 1706\ \text{milhões de rotações}
\qquad
L_{10h} = \frac{1706 \times 10^6}{60 \times 1450} \approx 19\,600\ \text{h}
$$

Para operação contínua (exigência de 40 000 h), **insuficiente**: seria preciso um rolamento maior.

**Situação 2 — rolamento de rolos em equipamento lento:** rolo de transportador a **60 rpm**, carga **150 kN**, rolamento autocompensador de rolos com **C = 500 kN** (ilustrativo).

$$
L_{10} = \left(\frac{500}{150}\right)^{10/3} \approx 55\ \text{milhões de rotações}
\qquad
L_{10h} = \frac{55 \times 10^6}{60 \times 60} \approx 15\,400\ \text{h}
$$

> [!question] Exercício 1
>
> Um rolamento de esferas tem vida de 20 000 h. Qual a nova vida se a carga aumentar 25 %? E se a rotação dobrar (mesma carga)?
>
> > [!success]- Resolução
> >
> > - Carga ×1,25: vida $\times (1/1{,}25)^3 = 0{,}512$ → **≈ 10 240 h**.
> > - Rotação ×2: a vida em rotações é a mesma; em horas, cai pela metade → **10 000 h**.

> [!question] Exercício 2
>
> Qual a vida com 99 % de confiabilidade de um rolamento com $L_{10h}$ = 30 000 h (considerando $a_{\text{ISO}}$ = 1)?
>
> > [!success]- Resolução
> >
> > $L_{1h} = 0{,}25 \times 30\,000 = 7\,500$ h.

## Erros comuns

- **Usar $C_0$ no cálculo de vida** (é $C$).
- **Esquecer a carga axial** na carga equivalente.
- **Expoente 3 para rolamentos de rolos** (é 10/3).
- **Ignorar lubrificação e contaminação**, que podem reduzir a vida real a uma fração da calculada.
- **Superdimensionar demais** rolamentos de rolos com carga muito baixa: podem deslizar (*skidding*) em vez de rolar. Há uma carga mínima indicada no catálogo.

## Ver também

- [[Seleção de rolamentos]]
- [[Montagem de rolamentos]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
