---
title: Redutores
tags: [elementos, transmissao]
fontes: [AGMA 6013 / AGMA 6113 (redutores industriais — fatores de serviço) ⚠️ verificar, ISO 6336, catálogos técnicos de redutores industriais (seções de seleção), Niemann Elementos de Máquinas (vol. de engrenagens), Budynas e Nisbett Elementos de Máquinas de Shigley]
status: rascunho
---

**Resumo:** redutores reduzem a rotação e multiplicam o torque entre o motor e a máquina. Podem ter engrenagens cilíndricas, cônicas, coroa e sem-fim ou planetárias. A seleção de um redutor de catálogo parte da potência e do torque necessários, multiplicados por um fator de serviço que depende do tipo de motor, da máquina acionada e das horas de operação, e verifica também a capacidade térmica.

## O que é

### Tipos

| Tipo | Eixos | Relação por estágio | Rendimento por estágio | Características |
|---|---|---|---|---|
| **Engrenagens cilíndricas (helicoidais)** | Paralelos | até ~6 | ~98 % | Robusto, eficiente; o mais comum na indústria |
| **Cônico-helicoidal** | Ortogonais (90°) | 1º estágio cônico + cilíndricos | ~97–98 % por estágio | Muda a direção; eficiente |
| **Coroa e sem-fim** | Ortogonais, não concorrentes | 5 a 100 | 50 % a 90 % (cai com a relação) | Compacto, silencioso; rendimento baixo em relações altas; pode ser irreversível |
| **Planetário** | Coaxiais | 3 a 10 por estágio | ~97–98 % | Muito compacto para torques altos; a carga se divide entre planetas |

### Grandezas de seleção

- **Relação:** $i = n_{\text{motor}}/n_{\text{saída}}$.
- **Torque de saída:** $T_2 = \dfrac{9550\,P\,\eta}{n_2}$.
- **Fator de serviço ($f_s$ ou SF):** multiplica a potência ou o torque necessário para escolher o redutor do catálogo. Depende:
  - do **tipo de carga** da máquina acionada: uniforme (bombas centrífugas, ventiladores), choques moderados (transportadores com carga irregular, misturadores), choques pesados (britadores, moinhos, prensas);
  - das **horas de operação por dia**;
  - do **motor** (elétrico, combustão);
  - do **número de partidas** por hora.

Valores usuais vão de cerca de 1,0 (carga uniforme, poucas horas) a 2,0 ou mais (choques pesados, 24 h). ⚠️ verificar na tabela do fabricante ou na AGMA.

- **Capacidade térmica:** potência que o redutor transmite continuamente sem superaquecer o óleo. Pode limitar antes da capacidade mecânica, principalmente em redutores de sem-fim e em ambientes quentes. Soluções: ventilador no eixo, serpentina de água, trocador de calor.
- **Cargas radiais nas pontas de eixo** (pinhões, polias, rodas dentadas montadas na ponta): têm limites no catálogo.

## Por que importa no projeto

- **Acionamentos de alto torque e baixa rotação** (rolos, tambores, transportadores, misturadores) normalmente combinam motor, acoplamento, redutor e, às vezes, transmissão final aberta (engrenagens abertas ou correntes).
- **Padronização:** poucos tamanhos de redutor no parque reduzem sobressalentes.
- **Eficiência:** um redutor de sem-fim com 70 % de rendimento desperdiça 30 % da energia em calor durante toda a vida do equipamento.

## Como aplicar (passo a passo / regras práticas)

1. **Potência da máquina** ($P_{\text{máq}}$) e rotação de saída ($n_2$).
2. **Relação** com o motor escolhido.
3. **Fator de serviço** pelo tipo de carga, horas e partidas.
4. **Potência (ou torque) de seleção:** $P_{\text{sel}} = P_{\text{máq}} \times f_s$; escolha no catálogo um redutor com capacidade ≥ $P_{\text{sel}}$.
5. **Verifique a capacidade térmica** e, se necessário, a refrigeração.
6. **Verifique as cargas nas pontas de eixo** e a forma de montagem (posição, flange, base).
7. **Defina acoplamentos** de entrada e saída. Ver [[Acoplamentos]].

## Norma relacionada

- **AGMA 6013 / 6113**: redutores industriais de engrenagens (inclui fatores de serviço). ⚠️ verificar edições.
- **ISO 6336**: cálculo das engrenagens internas.
- **Catálogos de fabricantes**: tabelas de seleção, fatores de serviço e capacidade térmica.

## Exemplo prático

**Situação:** acionar um transportador pesado que precisa de **45 kW a 25 rpm**, com motor de 4 polos (**1750 rpm** a 60 Hz), operação **24 h/dia** com choques moderados.

1. Relação: $i = 1750/25 = 70$ → redutor de 3 estágios helicoidais (ou cônico-helicoidal se os eixos forem a 90°).
2. Torque de saída: $T_2 = 9550 \times 45/25 \approx 17\,190$ N·m (com rendimento ~0,95 do redutor, o motor precisa de cerca de 47 kW → motor de 55 kW comercial).
3. Fator de serviço adotado: **1,5** (choques moderados, 24 h — confirmar na tabela).
4. Torque de seleção: $17\,190 \times 1{,}5 \approx 25\,800$ N·m → escolher redutor com torque nominal de saída ≥ 26 kN·m na relação 70.
5. Verificar a capacidade térmica para 45 kW contínuos no ambiente de instalação.

> [!question] Exercício
>
> Um redutor de coroa e sem-fim de relação 40:1 tem rendimento de 75 % e recebe 11 kW a 1750 rpm. Qual o torque de saída e quanta potência vira calor?
>
> > [!success]- Resolução
> >
> > - $n_2 = 1750/40 = 43{,}75$ rpm
> > - Potência de saída: $11 \times 0{,}75 = 8{,}25$ kW
> > - $T_2 = 9550 \times 8{,}25/43{,}75 \approx 1800$ N·m
> > - Calor: $11 - 8{,}25 = 2{,}75$ kW, que precisam ser dissipados pela carcaça. É por isso que a capacidade térmica limita redutores de sem-fim.

## Erros comuns

- **Selecionar pelo motor** (potência nominal) sem fator de serviço, ou com fator de serviço errado para a máquina.
- **Esquecer a capacidade térmica.**
- **Montar polias ou pinhões grandes na ponta do eixo** sem verificar a carga radial admissível.
- **Óleo e nível errados** para a posição de montagem.

## Ver também

- [[Geometria de engrenagens]]
- [[Dimensionamento de engrenagens]]
- [[Acoplamentos]]
- [[Correias e correntes]]
- [[05-elementos-de-maquinas/index|Índice do módulo 05]]
