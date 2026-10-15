---
title: Eixos estriados
tags: [elementos, eixo-cubo]
fontes: [ISO 14 (estrias de flancos retos), ISO 4156 (estrias evolventes), DIN 5480 (estrias evolventes), Niemann Elementos de Máquinas (cap. de uniões eixo-cubo), Budynas e Nisbett Elementos de Máquinas de Shigley]
status: rascunho
---

**Resumo:** um eixo estriado tem vários "dentes" longitudinais que encaixam em ranhuras do cubo, funcionando como muitas chavetas integradas ao eixo. Transmite torques maiores que uma chaveta, distribui melhor a carga, centraliza o cubo e permite deslizamento axial quando necessário.

## O que é

### Tipos

| Tipo | Norma | Características |
|---|---|---|
| **Flancos retos** | ISO 14 | Dentes de faces paralelas; séries leve e média; centralização pelo diâmetro interno (mais comum) ou pelos flancos |
| **Evolvente** | ISO 4156, DIN 5480 | Perfil de dente de engrenagem (ângulo de pressão de 30°, ou 37,5° e 45°); autocentralizante pelos flancos; mais resistente e fácil de fabricar por geração |
| **Serrilhado** | DIN 5481 | Dentes pequenos e numerosos; torques menores, fixação de alavancas e manivelas |

### Centralização

- **Pelo diâmetro** (interno ou externo): precisão de centralização alta; exige retificação do diâmetro de centralização.
- **Pelos flancos:** o próprio contato dos dentes centraliza; típico das estrias evolventes; simplifica a fabricação.

### Capacidade de carga (estimativa)

Por pressão nos flancos:

$$
p = \frac{2T}{d_m\,h'\,L\,z\,\varphi} \le p_{\text{adm}}
$$

onde $d_m$ é o diâmetro médio, $h'$ a altura útil de contato, $L$ o comprimento de contato, $z$ o número de estrias e $\varphi \approx 0{,}75$ um fator que considera que nem todas as estrias carregam igualmente. ⚠️ verificar os fatores e pressões admissíveis na DIN 5466 / referência adotada.

## Por que importa no projeto

- **Torques altos e alternados**, onde uma chaveta ficaria comprida demais.
- **Deslizamento axial sob carga:** engrenagens deslizantes de caixas de câmbio, cardans (cruzetas) com compensação de comprimento.
- **Acoplamentos e cubos de grandes acionamentos.**
- **Montagem e desmontagem** sem prensa, com centralização precisa.

## Como aplicar (passo a passo / regras práticas)

1. **Escolha o tipo:** evolvente (DIN 5480) para casos novos com torque alto; flancos retos (ISO 14) quando a peça de reposição exigir.
2. **Selecione o perfil** pelo diâmetro do eixo nas tabelas da norma (módulo, número de dentes, diâmetros).
3. **Calcule o comprimento** pela pressão admissível.
4. **Defina o ajuste** (fixo, deslizante) pela classe de tolerância das estrias.
5. **Designe completamente** no desenho (por exemplo, "DIN 5480 — W 50 × 2 × 24 × 8f" para eixo). ⚠️ verificar o formato de designação.

## Norma relacionada

- **ISO 14**: estrias de flancos retos com centralização interna.
- **ISO 4156** (partes 1 a 3): estrias evolventes, dimensões e inspeção.
- **DIN 5480**: estrias evolventes, muito usada em equipamentos industriais.

## Exemplo prático

**Situação:** o eixo de saída de um redutor que aciona um transportador pesado transmite **12 000 N·m** com picos de partida de 2×. Com chaveta, o eixo de Ø110 precisaria de comprimento acima de 2 d.

- Solução com estria evolvente DIN 5480 de diâmetro de referência próximo de 110 mm, comprimento de engrenamento de cerca de 1 d.
- Vantagens adicionais: o cubo do acoplamento é centralizado pelos flancos e pode ser removido sem prensa na manutenção.

> [!question] Exercício
>
> Cite duas vantagens de um eixo estriado em relação a uma chaveta paralela e uma desvantagem.
>
> > [!success]- Resolução
> >
> > **Vantagens:** maior capacidade de torque para o mesmo comprimento; carga distribuída em vários dentes (menor concentração no eixo); permite deslizamento axial; boa centralização.
> > **Desvantagens:** fabricação mais cara (exige fresa geradora, brocha ou ferramentas especiais); reparo mais difícil; cubo também precisa de ferramenta especial (brochamento ou mortajadora).

## Erros comuns

- **Misturar normas** (eixo DIN 5480 com cubo ISO 4156): os perfis não são intercambiáveis.
- **Esquecer a lubrificação** de estrias deslizantes, que sofrem desgaste por *fretting*.
- **Designação incompleta** no desenho.

## Ver também

- [[Chavetas]]
- [[Geometria de engrenagens]]
- [[Acoplamentos]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
