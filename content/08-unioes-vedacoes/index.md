---
title: 08 · Uniões e vedações
tags: [indice, unioes]
---

**Resumo:** Como juntar peças (solda, parafuso, interferência) e como impedir vazamentos (retentores, gaxetas, o-rings).

## Por que este módulo importa
Parafuso afrouxando e mancal vazando óleo ou recebendo caldo são falhas clássicas em moenda. Pré-carga correta e vedação bem especificada resolvem boa parte delas.

## Tópicos
Ordem sugerida de estudo: de cima para baixo.

- [x] [[Uniões parafusadas|Uniões parafusadas: pré-carga e torque]]
- [x] [[Uniões soldadas|Uniões soldadas: dimensionamento de cordões]]
- [x] [[Uniões por interferência]]
- [x] [[Pinos e cavilhas]]
- [x] [[Retentores]]
- [x] [[Gaxetas]]
- [x] [[O-rings|O-rings: alojamento]]
- [x] [[Juntas planas]]
- [x] [[Selos mecânicos]]

## Normas principais
Lista de partida, para conferir no documento original. Nenhum trecho de norma é reproduzido aqui.

- VDI 2230 — cálculo de uniões parafusadas
- ISO 3601 (série) — o-rings
- ISO 6194 (série) — retentores radiais

## Módulos relacionados
- [[05-elementos-de-maquinas/index|05 · Elementos de máquinas]]
- [[07-processos-fabricacao/index|07 · Processos de fabricação]]

## Revisão rápida

Tente responder antes de abrir a resposta.

> [!question] 1. Numa união parafusada com C = 0,25, por que o parafuso 'sente' só 25 % da carga externa enquanto as peças não se separam?
>
> > [!success]- Resposta
> >
> > Porque o parafuso e as peças comprimidas funcionam como **molas em paralelo**: as peças são muito mais rígidas e absorvem a maior parte da carga externa (reduzindo sua compressão). O parafuso recebe só a fração $C = k_b/(k_b + k_m)$. Ver [[Uniões parafusadas]].

> [!question] 2. Por que a pré-carga alta protege o parafuso contra a fadiga?
>
> > [!success]- Resposta
> >
> > Porque, mantendo as peças unidas, a **variação de força no parafuso** fica limitada a $C\,\Delta P$. Se as peças se separam (pré-carga baixa), o parafuso passa a carregar toda a variação da carga. Ver [[Uniões parafusadas]].

> [!question] 3. Como se calcula a tensão num cordão de filete sob carga excêntrica, pelo método da solda como linha?
>
> > [!success]- Resposta
> >
> > Calculam-se as propriedades **unitárias** ($A_u$, $I_u$ ou $J_u$) dos cordões, multiplica-se pela **garganta** ($0{,}707\,h$), e somam-se vetorialmente o cisalhamento direto ($F/(a A_u)$) e a tensão de flexão ($Mc/I$) ou torção ($Tr/J$). Ver [[Uniões soldadas]].

> [!question] 4. Numa união por interferência, qual interferência (mínima ou máxima) define o torque garantido, e qual define a tensão máxima no cubo?
>
> > [!success]- Resposta
> >
> > A **mínima** define o **torque garantido** (pior caso de aperto). A **máxima** define a **tensão máxima** no cubo e a força de montagem. Ver [[Uniões por interferência]].

> [!question] 5. Por que se usa um pino cilíndrico e um pino losango para localizar uma tampa, e não dois cilíndricos?
>
> > [!success]- Resposta
> >
> > Para evitar **hiperestaticidade**: dois pinos cilíndricos em furos precisos podem não montar por causa das tolerâncias de posição. O cilíndrico fixa a posição; o losango fixa só a rotação. Ver [[Pinos e cavilhas]].

> [!question] 6. Quais requisitos do eixo são decisivos para a vida de um retentor?
>
> > [!success]- Resposta
> >
> > **Rugosidade** Ra 0,2–0,8, **retificação de mergulho** (sem marcas helicoidais), **dureza** adequada (≥ 45–55 HRC), **tolerância** h11, **chanfro** de entrada e **batimento** limitado. Ver [[Retentores]].

> [!question] 7. Por que uma gaxeta precisa de um pequeno vazamento em operação?
>
> > [!success]- Resposta
> >
> > Porque o **gotejamento lubrifica e refrigera** o contato entre a gaxeta e o eixo. Sem ele, a gaxeta queima e a luva se desgasta. Ver [[Gaxetas]].

> [!question] 8. Um o-ring de seção 2,62 mm é montado num canal de altura 2,0 mm. Qual a compressão?
>
> > [!success]- Resposta
> >
> > $(2{,}62 - 2{,}0)/2{,}62 \approx 24\ \%$ — adequada para vedação estática. Ver [[O-rings]].

> [!question] 9. Na verificação de uma junta plana pelo método ASME, quais duas condições definem a força mínima dos parafusos?
>
> > [!success]- Resposta
> >
> > O **assentamento** da junta ($W_{m2} = \pi b G y$) e a **operação** sob pressão ($W_{m1} = H + H_p$, com o fator de manutenção $m$). Usa-se o maior dos dois. Ver [[Juntas planas]].

> [!question] 10. Qual a falha mais rápida de um selo mecânico e como evitá-la?
>
> > [!success]- Resposta
> >
> > O **funcionamento a seco**: sem fluido entre as faces, elas aquecem e trincam em segundos. Evita-se com **escorva** antes da partida, instrumentação de nível ou pressão, e planos de lavagem adequados. Ver [[Selos mecânicos]].

