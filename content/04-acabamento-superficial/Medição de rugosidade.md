---
title: Medição com rugosímetro
tags: [acabamento, metrologia]
fontes: [ISO 21920-3:2021, ISO 4288:1996 (histórica), ISO 3274 (instrumentos de contato), Mitutoyo Quick Guide to Surface Roughness Measurement, Whitehouse Surfaces and their Measurement]
status: rascunho
---

**Resumo:** a rugosidade é medida com rugosímetro de contato: uma agulha de diamante percorre a superfície e o perfil é filtrado e convertido em parâmetros. Para que a medição seja válida e comparável, é preciso escolher corretamente o comprimento de corte (cut-off λc), o comprimento de avaliação e a direção de medição.

## O que é

### O instrumento

- **Apalpador:** agulha de diamante com raio de ponta pequeno (tipicamente 2 µm ou 5 µm) e ângulo de 60° ou 90°.
- **Unidade de avanço:** desloca o apalpador em linha reta sobre a superfície.
- **Patim (opcional):** apoio que acompanha a superfície e serve de referência; simplifica o instrumento, mas filtra parte da ondulação.
- **Processamento:** aplica os filtros e calcula Ra, Rz etc.

Existem também instrumentos ópticos (sem contato), usados em laboratório e em superfícies delicadas.

### Comprimentos

- **Comprimento de corte (cut-off, λc):** separa rugosidade de ondulação.
- **Comprimento de amostragem ($l_r$):** igual a λc.
- **Comprimento de avaliação ($l_n$):** normalmente **5 × λc**.
- **Comprimento de percurso:** um pouco maior, incluindo o início e o fim (descartados).

### Escolha do cut-off (superfícies não periódicas)

| Ra esperado (µm) | λc (mm) | Comprimento de avaliação (mm) |
|---|---|---|
| até 0,02 | 0,08 | 0,4 |
| > 0,02 a 0,1 | 0,25 | 1,25 |
| > 0,1 a 2 | **0,8** | **4** |
| > 2 a 10 | 2,5 | 12,5 |
| > 10 a 80 | 8 | 40 |

⚠️ verificar na ISO 21920-3 (que substituiu as regras da ISO 4288). Para superfícies periódicas (torneadas), a escolha é feita pelo espaçamento das marcas.

## Por que importa no projeto

- **Medições com cut-offs diferentes não são comparáveis.** A mesma peça medida com λc = 0,8 e com λc = 2,5 dá valores diferentes de Ra.
- **Direção:** mede-se **perpendicularmente às marcas** de usinagem, onde a rugosidade é máxima. Medir ao longo das marcas dá valores muito menores e enganosos.
- **Peças grandes:** rugosímetros portáteis permitem medir eixos e rolos montados na máquina.
- **Alternativas rápidas:** **padrões de comparação visuo-táteis** (plaquetas com rugosidades conhecidas por processo) permitem uma avaliação aproximada na oficina, comparando com a unha e o olho. Não substituem a medição em peças críticas.

## Como aplicar (passo a passo / regras práticas)

1. **Limpe a superfície** (óleo e cavacos distorcem a leitura).
2. **Posicione o apalpador perpendicular às marcas**.
3. **Escolha λc** pela tabela (0,8 mm na maioria das superfícies usinadas).
4. **Meça em vários pontos** (no mínimo três, distribuídos), principalmente em superfícies grandes.
5. **Compare com o limite do desenho** pela regra de aceitação indicada (por padrão, nenhum valor acima do máximo, na ISO 21920; ou a regra dos 16 % se o desenho indicar).
6. **Registre** as condições: λc, comprimento, apalpador, posição.

## Norma relacionada

- **ISO 21920-3:2021**: operadores de especificação (filtros e comprimentos padrão).
- **ISO 4288:1996**: regras e procedimentos antigos para avaliação; ainda presente em muitos instrumentos.
- **ISO 3274**: características nominais de instrumentos de contato. ⚠️ verificar se foi substituída.

## Exemplo prático

**Situação:** inspecionar a **pista do retentor** de um eixo de Ø60, especificada como Ra 0,2–0,8.

- Rugosímetro portátil, apalpador de 5 µm, **λc = 0,8 mm**, comprimento de avaliação de 4 mm.
- Medição **na direção axial** (perpendicular às marcas circunferenciais da retificação), em três posições a 120°.
- Leituras: Ra 0,52; 0,48; 0,55 µm → **aprovado**.
- Observação adicional: inspeção visual para confirmar ausência de marcas helicoidais (a pista deve ser retificada de mergulho).

> [!question] Exercício
>
> Um inspetor mede a rugosidade de um eixo torneado deslizando o apalpador **ao longo da circunferência** (na direção das marcas) e encontra Ra 0,4, quando o desenho pede Ra 1,6 máximo. O eixo está aprovado?
>
> > [!success]- Resolução
> >
> > **A medição não é válida.** No torneamento, as marcas são circunferenciais; medir ao longo delas mostra uma rugosidade muito menor que a real. A medição deve ser feita na **direção axial**, perpendicular às marcas. Só depois de medir corretamente é possível aprovar ou reprovar.

## Erros comuns

- **Medir na direção das marcas.**
- **Usar o cut-off errado**, ou diferente entre fornecedor e cliente.
- **Medir superfícies sujas** ou com óleo.
- **Confiar só no comparador visuo-tátil** em superfícies críticas.

## Ver também

- [[Parâmetros de rugosidade]]
- [[Textura superficial]]
- [[Símbolos de acabamento]]
- [[04-acabamento-superficial/index|Índice do módulo 04]]
