---
title: Parâmetros Ra, Rz e outros
tags: [acabamento, parametros]
fontes: [ISO 21920-2:2021, ISO 4287:1997 (histórica), ISO 13565-2 (parâmetros de razão de material, histórica), Whitehouse Surfaces and their Measurement, Mitutoyo Quick Guide to Surface Roughness Measurement]
status: rascunho
---

**Resumo:** os parâmetros de rugosidade resumem o perfil medido em números. O Ra (média aritmética dos desvios) é o mais usado e o mais estável, mas não distingue picos de vales. O Rz (altura máxima do perfil) é mais sensível a riscos e defeitos isolados. Para superfícies de contato e deslizamento, parâmetros de razão de material complementam a informação.

## O que é

### Linha média

Todos os parâmetros partem da **linha média**: a linha que divide o perfil de rugosidade de modo que a soma das áreas acima seja igual à das áreas abaixo (pelo método dos mínimos quadrados). As alturas $z(x)$ são medidas a partir dela.

### Parâmetros de amplitude

| Parâmetro | Definição | Comentário |
|---|---|---|
| **Ra** | Média aritmética dos valores absolutos das alturas: $Ra = \dfrac{1}{l}\displaystyle\int_0^l \lvert z(x)\rvert\,dx$ | O mais usado. Estável e pouco sensível a defeitos isolados |
| **Rq** | Média quadrática: $Rq = \sqrt{\dfrac{1}{l}\displaystyle\int_0^l z^2(x)\,dx}$ | Usado em óptica e estatística; para perfis senoidais, $Rq \approx 1{,}11\,Ra$ |
| **Rp / Rv** | Altura do maior pico / profundidade do maior vale | Indicam assimetria do perfil |
| **Rz** | Altura máxima do perfil (pico mais alto + vale mais profundo). Na prática de instrumentos e da antiga ISO 4287, média de Rz dos 5 comprimentos de amostragem | Mais sensível a riscos. Muito usado na Europa |
| **Rt** | Altura total do perfil no comprimento de avaliação inteiro | O mais severo: um único risco determina o valor |

**Relação aproximada entre Rz e Ra:** para superfícies usinadas comuns, $Rz \approx 4$ a $7 \times Ra$. É só uma ordem de grandeza: os dois medem coisas diferentes e **não devem ser convertidos** para fins de aceitação.

### Parâmetros de forma do perfil

- **Rsk (assimetria):** negativo quando o perfil tem platôs com vales profundos (bom para reter óleo e suportar carga); positivo quando tem picos agudos.
- **Rku (curtose):** indica se o perfil tem picos e vales "pontiagudos" ou "achatados".

### Parâmetros de razão de material

- **Rmr(c):** porcentagem do comprimento em que o material é "cortado" a uma dada profundidade c. Representa a área de apoio real depois do amaciamento.
- **Rk, Rpk, Rvk:** dividem o perfil em picos (que se desgastam no amaciamento), núcleo (que suporta carga) e vales (que retêm óleo). Muito usados em cilindros de motores e superfícies brunidas.

### Série de valores de Ra

Os valores de Ra são escolhidos numa série preferencial (em µm), em que cada valor é cerca do dobro do anterior:

$$
0{,}025 - 0{,}05 - 0{,}1 - 0{,}2 - 0{,}4 - 0{,}8 - 1{,}6 - 3{,}2 - 6{,}3 - 12{,}5 - 25 - 50
$$

Desenhos antigos podem usar as **classes N** (N1 = 0,025 µm, ..., N6 = 0,8, N7 = 1,6, N8 = 3,2, N9 = 6,3, N10 = 12,5, ..., N12 = 50) ou os **triângulos** da antiga norma brasileira (▽, ▽▽, ▽▽▽). ⚠️ verificar a correspondência dos triângulos no desenho de origem.

## Por que importa no projeto

- **Ra é o padrão "universal"**, entendido por qualquer oficina e instrumento.
- **Rz é melhor quando defeitos isolados importam** (vedações, superfícies com risco de riscos de ferramenta).
- **Duas superfícies com o mesmo Ra podem funcionar de forma oposta**: uma com picos agudos (desgaste rápido) e outra com platôs (boa sustentação). Rsk e Rmr ajudam a distinguir.

## Como aplicar (passo a passo / regras práticas)

1. **Use Ra** para a grande maioria das superfícies.
2. **Use Rz (ou Ra + Rz máximo)** em superfícies de vedação e onde riscos isolados são críticos.
3. **Use parâmetros de razão de material** em superfícies de deslizamento de alto desempenho (cilindros hidráulicos, camisas), se o fornecedor e o laboratório tiverem capacidade de medir.
4. **Escolha valores da série preferencial.**
5. **Especifique o limite máximo**, que é o critério usual (por padrão, na ISO 21920, todos os valores medidos devem respeitar o limite, salvo se for indicada a regra dos 16 %). ⚠️ verificar a regra de aceitação.

## Norma relacionada

- **ISO 21920-2:2021**: definições de todos os parâmetros de perfil. Substitui a ISO 4287 e as ISO 13565-2/-3. Uma mudança relevante: os parâmetros passam a ser calculados sobre o comprimento de avaliação inteiro, e não pela média de vários comprimentos de amostragem. Para a maioria das medições, os resultados mudam pouco.

## Exemplo prático

**Situação:** a haste de um cilindro hidráulico especificada como "Ra 0,4" apresentava vazamento precoce pela vedação.

- A medição mostrou **Ra 0,35 µm** (aprovado) mas **Rz 4,5 µm**, com alguns riscos profundos de retificação.
- Ra, por ser média, "esconde" os riscos; a vedação, que trabalha deslizando, é sensível a eles.
- **Especificação revista:** "Ra 0,1–0,4; Rz máx. 2,5; Rmr ≥ 50 % a uma profundidade c definida" (conforme recomendação do fabricante da vedação). ⚠️ verificar.

> [!question] Exercício
>
> Um perfil de rugosidade simplificado é uma onda triangular simétrica com amplitude de ±4 µm em torno da linha média. Qual é o Ra?
>
> > [!success]- Resolução
> >
> > Numa onda triangular simétrica de amplitude $A$, o valor absoluto $\lvert z \rvert$ varia linearmente de 0 a $A$, então sua média é $A/2$.
> > $Ra = 4/2 = 2$ µm. O Rz (pico + vale) seria $4 + 4 = 8$ µm, ou seja, $Rz = 4\,Ra$ nesse perfil.

## Erros comuns

- **Converter Rz em Ra** por uma relação fixa para aceitar ou rejeitar peças.
- **Especificar só Ra em superfícies de vedação.**
- **Usar valores fora da série** (Ra 1,0; Ra 2,0), que dificultam a comparação e não são usuais nos padrões de referência.
- **Comparar medições com filtros (λc) diferentes.**

## Ver também

- [[Textura superficial]]
- [[Medição de rugosidade]]
- [[Rugosidade pela função]]
- [[04-acabamento-superficial/index|Índice do módulo 04]]
