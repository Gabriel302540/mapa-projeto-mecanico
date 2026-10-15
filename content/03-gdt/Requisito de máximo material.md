---
title: Modificadores de material (MMR e LMR)
tags: [gdt, modificadores]
fontes: [ISO 2692:2021, ISO 1101:2017, ASME Y14.5-2018, Henzold Geometrical Dimensioning and Tolerancing for Design, Manufacturing and Inspection (cap. de requisitos de material)]
status: rascunho
---

**Resumo:** o requisito de máximo material (Ⓜ) permite aumentar a tolerância geométrica quando o elemento se afasta do máximo material — um furo maior ou um pino menor —, porque a montagem fica mais fácil. Esse ganho é chamado de "bônus". O mínimo material (Ⓛ) faz o raciocínio inverso, para garantir espessura mínima de parede.

## O que é

### Condições de material

| Condição | Furo (elemento interno) | Eixo/pino (elemento externo) |
|---|---|---|
| **Máximo material (MMC/MMS)** | Diâmetro **mínimo** | Diâmetro **máximo** |
| **Mínimo material (LMC/LMS)** | Diâmetro **máximo** | Diâmetro **mínimo** |

Pense no peso: a peça tem mais material quando o furo é menor ou o pino é maior.

### Requisito de máximo material (Ⓜ)

Quando a tolerância de posição (ou orientação, retitude) tem **Ⓜ**:

- A tolerância indicada vale quando o elemento está no **máximo material**.
- Conforme o elemento se afasta do máximo material, a tolerância **aumenta** na mesma medida:

$$
t_{\text{total}} = t_{\text{indicada}} + \text{bônus}
$$

$$
\text{bônus}_{\text{furo}} = D_{\text{real}} - D_{\text{MMC}} \qquad \text{bônus}_{\text{pino}} = d_{\text{MMC}} - d_{\text{real}}
$$

**Por quê:** o que garante a montagem é o **limite virtual** (tamanho virtual), a "sombra" do pior caso: para um furo, $D_{\text{MMC}} - t$. Se o furo sai maior, ele pode se deslocar mais e ainda deixar livre o mesmo espaço para o parafuso.

### Calibrador funcional

O Ⓜ permite inspecionar com um **calibrador funcional**: uma placa com pinos no tamanho virtual, nas posições teóricas. Se a peça entra no calibrador, os furos estão aprovados quanto à posição. Rápido e barato em produção.

### Requisito de mínimo material (Ⓛ)

Garante uma **espessura mínima de material**, por exemplo a parede entre um furo e a borda, ou entre um furo e um rebaixo. O bônus cresce quando o elemento se afasta do mínimo material.

### Requisito de reciprocidade (Ⓡ)

Usado junto com Ⓜ ou Ⓛ: permite que, se a tolerância geométrica não for toda usada, a tolerância de tamanho seja ampliada. Menos comum. ⚠️ verificar na ISO 2692.

## Por que importa no projeto

- **Mais peças aprovadas sem prejuízo funcional**, reduzindo refugo em furos de passagem.
- **Inspeção rápida** com calibradores funcionais.
- **Não use em elementos de função precisa**, como furos de pinos de localização de precisão ou assentos de rolamentos: neles a posição importa independentemente do tamanho, e o bônus pode prejudicar a função.

## Como aplicar (passo a passo / regras práticas)

1. **Use Ⓜ em furos de passagem de parafusos** e em elementos cuja função é só **montar** com folga.
2. **Não use Ⓜ** em elementos de centralização precisa, ajustes com interferência ou elementos que giram.
3. **Use Ⓛ** quando a preocupação for parede mínima (resistência, vazamento, sobremetal para usinagem).
4. **Calcule o limite virtual** para projetar o calibrador ou verificar a montagem.

## Norma relacionada

- **ISO 2692:2021**: requisitos de máximo material (MMR), mínimo material (LMR) e reciprocidade (RPR).
- **ISO 1101:2017**: indicação dos modificadores no quadro.

## Exemplo prático

**Situação:** furos de uma tampa: **4× Ø14 +0,3/0** (14,0 a 14,3), com posição **Ø0,5 Ⓜ** em relação a A e B.

| Furo medido | Bônus | Tolerância de posição disponível |
|---|---|---|
| Ø14,00 (máximo material) | 0 | Ø0,50 |
| Ø14,10 | 0,10 | Ø0,60 |
| Ø14,30 (mínimo material) | 0,30 | Ø0,80 |

**Limite virtual do furo:** $14{,}0 - 0{,}5 = 13{,}5$ mm. O calibrador funcional teria 4 pinos de Ø13,5 nas posições teóricas. Qualquer furo que deixe passar esse pino, no lugar certo, garante a montagem de um parafuso M12 (Ø12) com folga.

> [!question] Exercício
>
> Um pino Ø10 −0,1/−0,2 (9,8 a 9,9 mm) tem posição Ø0,05 Ⓜ. Um pino medido com Ø9,82 está deslocado de modo a ocupar uma zona de Ø0,12. Está aprovado?
>
> > [!success]- Resolução
> >
> > Máximo material do pino: 9,9 mm.
> > Bônus: $9{,}90 - 9{,}82 = 0{,}08$ mm.
> > Tolerância disponível: $0{,}05 + 0{,}08 = 0{,}13$ mm.
> > Como $0{,}12 \le 0{,}13$, o pino está **aprovado**.

## Erros comuns

- **Confundir máximo material de furo e de eixo** (furo: menor; eixo: maior).
- **Usar Ⓜ em pinos de localização de precisão**, permitindo deslocamentos que prejudicam a função.
- **Esquecer o bônus** na inspeção por coordenadas, reprovando peças boas.
- **Projetar o calibrador** com o tamanho nominal em vez do limite virtual.

## Ver também

- [[Tolerâncias de localização]]
- [[Independência e envoltória]]
- [[Quadro de tolerância]]
- [[03-gdt/index|Índice do módulo 03]]
