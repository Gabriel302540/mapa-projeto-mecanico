---
title: Princípio da independência e requisito de envoltória
tags: [gdt, fundamentos]
fontes: [ISO 8015:2011, ISO 14405-1:2016, ASME Y14.5-2018 (Regra nº 1), Henzold Geometrical Dimensioning and Tolerancing for Design, Manufacturing and Inspection]
status: rascunho
---

**Resumo:** pela ISO, cada requisito do desenho vale de forma independente: a tolerância de diâmetro controla só o tamanho local, e a forma precisa de tolerância geométrica própria. Quando a peça precisa montar com garantia num par, usa-se o requisito de envoltória (símbolo Ⓔ), que obriga a peça inteira a caber dentro de um cilindro perfeito de diâmetro máximo. Nos EUA (ASME), a envoltória já é o padrão.

## O que é

### Princípio da independência (ISO 8015)

**Cada especificação dimensional ou geométrica é atendida de forma independente**, a menos que o desenho diga o contrário. Na prática:

- Uma tolerância de tamanho "Ø50 h6" controla o **tamanho local** (medido entre dois pontos opostos) em cada seção.
- Ela **não** controla retitude do eixo, circularidade "em lóbulos" (três lóbulos podem dar o mesmo diâmetro em qualquer direção), nem a forma geral.
- Se a forma importa, ela deve ser especificada por tolerância geométrica (ver [[Tolerâncias de forma]]).

Desde a revisão de 2011, a ISO 8015 vale **por padrão** em todo desenho ISO, sem precisar ser citada. Muitas empresas ainda escrevem "ISO 8015" na legenda para deixar claro.

### Requisito de envoltória (Ⓔ)

Quando aplicado (símbolo **Ⓔ** depois da tolerância de tamanho, conforme ISO 14405-1), exige duas coisas ao mesmo tempo:

1. O tamanho local em qualquer seção não pode passar do **mínimo material** (eixo: diâmetro mínimo).
2. A peça inteira deve caber dentro de uma **envoltória de forma perfeita** no **máximo material** (eixo: um cilindro perfeito de diâmetro máximo).

Consequência: se o eixo estiver todo no diâmetro máximo, ele precisa estar **perfeitamente reto e redondo**. Se estiver menor, sobra margem para erros de forma. É exatamente o que garante a montagem com um furo.

### A diferença para a ASME

Na **ASME Y14.5**, vale a **Regra nº 1**: a envoltória de forma perfeita no máximo material é **automática** para todos os elementos de tamanho, salvo indicação contrária. Um desenho ASME e um desenho ISO com a mesma cota "Ø50 h6" **não significam a mesma coisa**. Por isso a norma de referência deve estar declarada na legenda.

| Situação | ISO (padrão) | ASME (padrão) |
|---|---|---|
| Ø50 h6, sem mais nada | Só tamanho local; forma livre | Tamanho + envoltória de forma perfeita no máximo material |
| Para ter envoltória | Acrescentar Ⓔ | Já tem |
| Para ter independência | Já tem | Acrescentar o símbolo de independência (Ⓘ) ou nota |

## Por que importa no projeto

- **Ajustes:** num ajuste com folga (H7/g6), a folga mínima só é garantida se furo e eixo tiverem forma perfeita no máximo material. Sem Ⓔ (ou sem tolerância de forma), um eixo levemente curvado pode não entrar num furo que, pelos diâmetros, deveria aceitar.
- **Desenhos de origem americana:** ao fabricar peças a partir de desenhos ASME, é preciso entender que a forma está implicitamente controlada.
- **Custo:** usar Ⓔ em tudo encarece; usar só onde há ajuste é a prática recomendada.

## Como aplicar (passo a passo / regras práticas)

1. **Confirme a norma de referência** na legenda (ISO 8015 ou ASME Y14.5).
2. **Em desenhos ISO**, coloque **Ⓔ** nos elementos de tamanho que formam **ajustes** (furo e eixo que montam com folga ou incerto): "Ø50 H7 Ⓔ".
3. **Elementos sem ajuste** (diâmetros livres) ficam com independência e tolerâncias gerais.
4. **Se a forma precisar ser mais apertada** que a envoltória permite, acrescente uma tolerância de forma (por exemplo, cilindricidade).

## Norma relacionada

- **ISO 8015:2011**: princípio da independência e regras fundamentais do GPS.
- **ISO 14405-1:2016**: especificação de tamanho linear, incluindo o modificador Ⓔ e outros (tamanho de dois pontos, mínimos quadrados etc.).
- **ASME Y14.5-2018**: Regra nº 1.

## Exemplo prático

**Situação:** um pino guia Ø20 g6 (19,980 a 19,993 mm) deve entrar numa bucha Ø20 H7 (20,000 a 20,021 mm). A folga mínima calculada é de 7 µm.

- **Sem Ⓔ (independência):** o pino pode ter todos os diâmetros locais em 19,993 mm e estar **curvado** 0,03 mm. Ele se comporta como um cilindro "virtual" de cerca de 20,023 mm e **não entra** na bucha, embora esteja aprovado pelas cotas.
- **Com Ⓔ:** o pino tem de caber num cilindro perfeito de 19,993 mm. Se todos os diâmetros estiverem em 19,993, a curvatura permitida é zero; se estiverem em 19,985, sobra 0,008 mm para erro de forma. A montagem é garantida.

> [!question] Exercício
>
> Um eixo ISO "Ø30 h7 Ⓔ" (29,979 a 30,000) tem todos os diâmetros locais medidos em 29,990 mm. Qual a máxima retitude do eixo permitida pela envoltória?
>
> > [!success]- Resolução
> >
> > A envoltória é um cilindro perfeito de Ø30,000 mm (máximo material). Com o eixo em Ø29,990, sobram $30{,}000 - 29{,}990 = 0{,}010$ mm para a curvatura. A retitude do eixo pode chegar a **0,010 mm**. Se o eixo estivesse com 30,000 mm em toda parte, a retitude permitida seria zero.

## Erros comuns

- **Supor que "Ø50 h6" controla a forma** num desenho ISO.
- **Ler um desenho ASME com regras ISO** (ou o contrário).
- **Usar Ⓔ em elementos sem função de ajuste.**
- **Não declarar a norma de referência** na legenda.

## Ver também

- [[Por que GD&T]]
- [[Tolerâncias de forma]]
- [[Requisito de máximo material]]
- [[Indicação de tolerâncias]]
- [[03-gdt/index|Índice do módulo 03]]
