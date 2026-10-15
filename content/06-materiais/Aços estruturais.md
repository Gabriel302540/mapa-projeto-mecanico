---
title: Aços estruturais
tags: [materiais, acos, caldeiraria]
fontes: [ASTM A36/A36M, ASTM A572/A572M, ASTM A516/A516M, ABNT NBR 7007 (aços-carbono e microligados para uso estrutural) ⚠️ verificar, AWS D1.1 (soldagem de estruturas — pré-aquecimento), Chiaverini Aços e Ferros Fundidos, Pfeil Estruturas de Aço]
status: rascunho
---

**Resumo:** aços estruturais são aços de baixo carbono, fornecidos em chapas, perfis e barras, especificados por propriedades mínimas de escoamento e ruptura. São a matéria-prima de estruturas, bases, carcaças soldadas e peças de caldeiraria. Sua principal qualidade, além da resistência, é a soldabilidade, avaliada pelo carbono equivalente.

## O que é

### Principais especificações

| Material | Escoamento mín. (MPa) | Ruptura (MPa) | Uso típico |
|---|---|---|---|
| **ASTM A36** | 250 | 400 – 550 | Estruturas, bases, chapas de caldeiraria em geral |
| **ASTM A572 Gr 50** | 345 | ≥ 450 | Estruturas mais leves e solicitadas |
| **ASTM A283 Gr C** | 205 | 380 – 515 | Chapas de uso geral, tanques |
| **ASTM A516 Gr 70** | 260 | 485 – 620 | **Vasos de pressão** e caldeiras (requisitos de tenacidade) |
| **ASTM A588 / A242** (patináveis) | 345 | ≥ 485 | Estruturas expostas à atmosfera (formam pátina protetora) |
| **NBR 7007 MR250 / AR350** | 250 / 350 | — | Equivalentes nacionais para perfis estruturais ⚠️ verificar |

⚠️ verificar todos os valores nas normas (variam com a espessura).

### Soldabilidade e carbono equivalente

A tendência de formar martensita (e trincar) na zona afetada pelo calor da solda cresce com o carbono e os elementos de liga. Mede-se pelo **carbono equivalente** (fórmula do IIW):

$$
CE = C + \frac{Mn}{6} + \frac{Cr + Mo + V}{5} + \frac{Ni + Cu}{15}
$$

| CE | Soldabilidade | Cuidados |
|---|---|---|
| < 0,40 | Boa | Normalmente sem pré-aquecimento (exceto chapas muito espessas ou baixa temperatura) |
| 0,40 – 0,60 | Regular | **Pré-aquecimento** e controle de hidrogênio (eletrodos básicos secos) |
| > 0,60 | Difícil | Pré e pós-aquecimento, procedimento qualificado |

⚠️ verificar os limites e as temperaturas de pré-aquecimento na AWS D1.1 ou norma aplicável. Ver [[07-processos-fabricacao/index|Soldagem]].

### Laminação e anisotropia

Chapas laminadas têm propriedades diferentes na direção da laminação e na espessura. Em juntas em T muito restritas, com tração perpendicular à superfície da chapa, pode ocorrer **arrancamento lamelar**; nesse caso se especificam chapas com propriedades garantidas na espessura (qualidade "Z"). ⚠️ verificar.

## Por que importa no projeto

- **Bases de máquinas, estruturas de suporte, chutes, tremonhas, tanques e carcaças soldadas** são feitos desses aços.
- **Vasos de pressão** exigem material com rastreabilidade e tenacidade comprovadas (A516 e similares), conforme código de projeto e NR-13.
- **Soldar peças de aço de construção mecânica (4140, 1045) em estruturas** de A36 exige procedimento especial por causa do CE alto.

## Como aplicar (passo a passo / regras práticas)

1. **Use A36** como padrão para estruturas e caldeiraria comuns.
2. **Use A572 Gr 50** quando o peso ou o espaço exigirem maior resistência.
3. **Use A516 Gr 60/70** em equipamentos sujeitos a pressão (conforme código).
4. **Calcule o CE** quando houver dúvida sobre a soldagem, principalmente em ligações com aços de construção mecânica.
5. **Especifique** no desenho e na lista de materiais: norma, grau, espessura ("Chapa ASTM A36 # 12,5 mm").

## Norma relacionada

- **ASTM A36, A572, A283, A516, A588**: especificações de chapas e perfis.
- **ABNT NBR 7007**: aços estruturais para perfis. ⚠️ verificar.
- **AWS D1.1**: soldagem de estruturas de aço (inclui pré-aquecimento por grupo de material e espessura).

## Exemplo prático

**Situação:** soldar um cubo de **SAE 1045** (C ≈ 0,45; Mn ≈ 0,75) numa chapa de **A36** para formar uma polia.

$$
CE_{1045} \approx 0{,}45 + \frac{0{,}75}{6} \approx 0{,}58
$$

- CE no limite superior da faixa "regular": exige **pré-aquecimento** (da ordem de 150 a 250 °C, conforme espessura ⚠️ verificar), eletrodo de baixo hidrogênio seco (E7018), resfriamento lento e, de preferência, alívio de tensões.
- Alternativa de projeto: fazer o cubo de **SAE 1020** (CE ≈ 0,35) se a resistência permitir, ou eliminar a solda (cubo aparafusado).

> [!question] Exercício
>
> Calcule o CE de um aço com C = 0,18 %, Mn = 1,40 %, Cr = 0,05 %, Ni = 0,10 %, Cu = 0,20 %, Mo = 0, V = 0,05 %. Precisa de pré-aquecimento pela regra geral?
>
> > [!success]- Resolução
> >
> > $CE = 0{,}18 + \dfrac{1{,}40}{6} + \dfrac{0{,}05 + 0 + 0{,}05}{5} + \dfrac{0{,}10 + 0{,}20}{15}$
> > $= 0{,}18 + 0{,}233 + 0{,}020 + 0{,}020 \approx 0{,}45$
> >
> > Está na faixa **0,40 – 0,60**: recomenda-se **pré-aquecimento** e controle de hidrogênio, principalmente em chapas grossas.

## Erros comuns

- **Soldar aço de construção mecânica como se fosse A36.**
- **Usar A36 em vaso de pressão** sem atender ao código.
- **Não especificar a norma da chapa** ("chapa de aço" apenas).
- **Ignorar o arrancamento lamelar** em nós muito restritos.

## Ver também

- [[Aços para construção mecânica]]
- [[Classificação dos aços]]
- [[07-processos-fabricacao/index|Processos de fabricação]]
- [[06-materiais/index|Índice do módulo 06]]
