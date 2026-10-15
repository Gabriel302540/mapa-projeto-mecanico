---
title: Pinos e cavilhas
tags: [unioes, fixadores]
fontes: [ISO 2338 (pinos cilíndricos), ISO 8734 (pinos cilíndricos temperados), ISO 2339 (pinos cônicos), ISO 8752 (pinos elásticos), Budynas e Nisbett Elementos de Máquinas de Shigley, Niemann Elementos de Máquinas (cap. de pinos)]
status: rascunho
---

**Resumo:** pinos são elementos cilíndricos ou cônicos usados para posicionar peças com precisão (pinos de localização ou guia), transmitir pequenas cargas, travar e articular. Um caso especial é o pino de ruptura (fusível mecânico), que se rompe numa sobrecarga para proteger o restante do acionamento.

## O que é

### Tipos

| Tipo | Norma | Características | Uso |
|---|---|---|---|
| **Pino cilíndrico** | ISO 2338 (m6 ou h8) / ISO 8734 (temperado) | Precisão, ajuste com interferência num furo e deslizante no outro | Localização precisa entre peças (tampa × carcaça) |
| **Pino cônico** (1:50) | ISO 2339 | Autotravante, remontagem precisa | Localização com desmontagem frequente |
| **Pino elástico** (tubular fendido) | ISO 8752 | Montagem por pressão em furo comum (sem alargar) | Fixação simples, eixos de alavancas |
| **Pino com cabeça / articulação** | — | Com furo para contrapino ou anel | Articulações, garfos |
| **Pino de ruptura (cisalhamento)** | — | Dimensionado para romper num torque definido | Proteção de acionamentos |

### Localização com dois pinos

Para posicionar uma peça sobre outra sem **hiperestaticidade** (excesso de restrições):

- **Um pino cilíndrico** (fixa a posição em X e Y);
- **Um pino "losango"** (com faces rebaixadas) ou um **furo oblongo** na peça (fixa só a rotação).

Dois pinos cilíndricos em furos de precisão podem não montar por causa das tolerâncias de posição.

Os pinos **posicionam**; os **parafusos** é que apertam. Os pinos não devem ser contados para transmitir a carga principal se a união for projetada por atrito (ver [[Uniões parafusadas]]).

### Dimensionamento

**Cisalhamento simples** (uma seção) e **duplo** (duas seções, como num garfo):

$$
\tau = \frac{F}{n_s\,\pi d^2/4}
$$

($n_s$ = número de seções de cisalhamento.)

**Pressão de contato** nas peças:

$$
p = \frac{F}{d\,t}
$$

com $t$ a espessura da peça em contato.

**Pino de ruptura:** dimensiona-se para romper com o torque limite. A tensão de ruptura ao cisalhamento é aproximadamente $\tau_u \approx 0{,}6$ a $0{,}8\,S_{ut}$ (depende do material e do entalhe). Como há dispersão, o pino costuma ter um **entalhe** (canal) na seção de corte, que torna a ruptura mais previsível. ⚠️ verificar com ensaio ou fornecedor.

## Por que importa no projeto

- **Remontagem sem realinhar:** tampas de redutores, bases de motores e acoplamentos com pinos de localização voltam à mesma posição após a manutenção.
- **Proteção contra sobrecarga:** pinos de ruptura em transportadores e alimentadores evitam que um travamento quebre o redutor.
- **Articulações** de alavancas, cilindros hidráulicos e garfos.

## Como aplicar (passo a passo / regras práticas)

1. **Localização:** use dois pinos (cilíndrico + losango) o mais **afastados** possível; furos alargados (H7) feitos com as peças montadas juntas, quando possível.
2. **Articulação:** dimensione por cisalhamento e pressão; especifique dureza e lubrificação (ou buchas).
3. **Pino de ruptura:** defina o torque limite, o raio, o material e o entalhe; preveja estoque de reposição e acesso fácil.
4. **Facilite a extração:** pinos em furos cegos precisam de rosca interna para extrator, ou furo passante.

## Norma relacionada

- **ISO 2338 / ISO 8734**: pinos cilíndricos (não temperados / temperados).
- **ISO 2339**: pinos cônicos.
- **ISO 8752**: pinos elásticos.

## Exemplo prático

**Situação:** a roda dentada de um acionamento por corrente deve se soltar do eixo se o torque passar de **2000 N·m**, protegendo o redutor. O pino de ruptura fica a **100 mm** do centro, em cisalhamento simples. Material do pino: aço com $S_{ut}$ ≈ 400 MPa; adota-se $\tau_u \approx 0{,}6 \times 400 = 240$ MPa.

- Força no pino: $F = 2\,000\,000/100 = 20$ kN
- Área: $A = 20\,000/240 \approx 83$ mm² → $d \approx 10{,}3$ mm

Adota-se um pino de Ø10 (rompe com ≈ 1900 N·m), confirmado por ensaio de algumas peças do mesmo lote, porque a dispersão real é grande.

> [!question] Exercício
>
> Um pino de articulação de Ø20 trabalha em cisalhamento duplo num garfo, com força de 40 kN. Qual a tensão de cisalhamento? E a pressão de contato na peça central de 30 mm de espessura?
>
> > [!success]- Resolução
> >
> > - $\tau = \dfrac{40\,000}{2 \times \pi \times 20^2/4} = \dfrac{40\,000}{628} \approx 64$ MPa
> > - $p = \dfrac{40\,000}{20 \times 30} \approx 67$ MPa

## Erros comuns

- **Dois pinos cilíndricos de precisão** para localizar, causando problemas de montagem.
- **Pinos colocados próximos demais** um do outro (localização angular fraca).
- **Pino de ruptura substituído por parafuso** "porque quebrava muito" — elimina a proteção.
- **Pinos em furos cegos sem forma de extração.**

## Ver também

- [[Uniões parafusadas]]
- [[Fixação axial]]
- [[Correias e correntes]]
- [[08-unioes-vedacoes/index|Índice do módulo 08]]
