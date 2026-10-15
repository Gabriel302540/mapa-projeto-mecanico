---
title: Padronização de componentes
tags: [metodologia, padronizacao]
fontes: [ISO 3 (números preferenciais — séries de Renard), ISO 17 e ISO 497 (guias de uso de números preferenciais), Pahl, Beitz, Feldhusen e Grote Projeto na Engenharia (cap. de séries e sistemas modulares), Back, Ogliari, Dias e Silva Projeto Integrado de Produtos]
status: rascunho
---

**Resumo:** padronizar é reduzir a variedade de componentes, materiais e soluções usados no parque de equipamentos, sem perder a função. Menos variedade significa menos itens em estoque, compras maiores e mais baratas, manutenção mais rápida e menos erros. As ferramentas são catálogos internos de componentes, codificação, números preferenciais e projetos modulares.

## O que é

### Níveis de padronização

| Nível | Exemplos |
|---|---|
| **Normas externas** | Usar parafusos ISO, rolamentos de séries normalizadas, chavetas DIN |
| **Seleção preferencial** | Dentro das normas, usar só alguns tamanhos (ex.: parafusos M12, M16, M20, M24; rolamentos de 3 séries) |
| **Catálogo interno** | Lista aprovada de componentes, com código, fornecedores e aplicação |
| **Soluções padronizadas** | Mancais, acoplamentos, tampas e bases com o mesmo projeto em vários equipamentos |
| **Projeto modular** | Equipamentos montados a partir de módulos comuns, variando o tamanho por séries |

### Números preferenciais (séries de Renard)

Para escolher tamanhos de uma família (potências, diâmetros, capacidades), usam-se séries geométricas normalizadas:

| Série | Razão | Valores (1 a 10) |
|---|---|---|
| R5 | $\sqrt[5]{10} \approx 1{,}6$ | 1 – 1,6 – 2,5 – 4 – 6,3 – 10 |
| R10 | $\sqrt[10]{10} \approx 1{,}25$ | 1 – 1,25 – 1,6 – 2 – 2,5 – 3,15 – 4 – 5 – 6,3 – 8 – 10 |
| R20 | $\sqrt[20]{10} \approx 1{,}12$ | 1 – 1,12 – 1,25 – 1,4 – 1,6 – ... |

A mesma ideia está nos [[Graus IT]], nas [[Escalas]] e nos módulos de engrenagens. A vantagem é que a diferença **relativa** entre tamanhos vizinhos é constante.

### Análise de Pareto da variedade

Em parques industriais, é comum que **poucos itens** (por exemplo, 20 % dos tipos de rolamento) respondam pela **maior parte** do consumo. A padronização começa por esses itens e pelos casos "únicos" que podem migrar para um padrão.

## Por que importa no projeto

- **Estoque de sobressalentes:** cada componente diferente é mais um item parado no almoxarifado.
- **Tempo de parada:** se o sobressalente é o mesmo para vários equipamentos, a chance de tê-lo em estoque é maior.
- **Treinamento e procedimentos:** montagens iguais são feitas mais rápido e com menos erros.
- **Compras:** volumes maiores de menos itens têm preços e prazos melhores.

## Como aplicar (passo a passo / regras práticas)

1. **Levante** o que existe: lista de componentes por equipamento (rolamentos, acoplamentos, redutores, motores, retentores, parafusos).
2. **Agrupe** por função e tamanho; identifique duplicidades e casos únicos.
3. **Defina os preferidos** (por exemplo, 2 ou 3 tipos de acoplamento em poucos tamanhos).
4. **Crie o catálogo interno** com código, especificação completa, equivalências e fornecedores.
5. **Aplique em projetos novos** e, na manutenção, migre gradualmente os equipamentos antigos quando houver troca.
6. **Use a lista de requisitos** para registrar "usar componente do catálogo" como desejo ou exigência. Ver [[Levantamento de requisitos]].

## Norma relacionada

- **ISO 3**: números preferenciais (séries de Renard).
- **ISO 17 / ISO 497**: guias de uso das séries.
- Normas de componentes (ISO 4017, ISO 281, DIN 6885...) são a base da padronização externa.

## Exemplo prático

**Situação:** um levantamento em 40 transportadores encontrou **23 modelos diferentes de redutores** de 8 fabricantes, com potências de 7,5 a 75 kW.

**Proposta de padronização:**

1. Adotar **um fabricante preferencial** (e um alternativo com intercambiabilidade dimensional).
2. Escolher **6 tamanhos** cobrindo a faixa de torques, em progressão aproximadamente geométrica (como uma série R5).
3. Usar **eixo de saída oco com braço de torção** onde possível, com bucha de fixação, para trocas rápidas.
4. Migrar os equipamentos aos poucos, aproveitando as trocas por falha ou reforma.
5. Resultado esperado: estoque de reserva de 23 para 6 redutores (com 1 ou 2 de cada), trocas mais rápidas e procedimentos únicos.

> [!question] Exercício
>
> Uma linha de equipamentos precisa de capacidades entre 10 e 100 t/h. Usando a série R5, quais tamanhos você ofereceria?
>
> > [!success]- Resolução
> >
> > Série R5 de 10 a 100: **10 – 16 – 25 – 40 – 63 – 100 t/h**. Seis tamanhos, cada um cerca de 1,6 vez o anterior, cobrindo a faixa com diferença relativa constante.

## Erros comuns

- **Padronizar "por baixo"**, forçando componentes inadequados em aplicações especiais.
- **Catálogo interno desatualizado** ou sem especificação completa.
- **Projetos novos ignorando o catálogo.**
- **Trocar tudo de uma vez**, em vez de migrar gradualmente.

## Ver também

- [[Lista de materiais]]
- [[Levantamento de requisitos]]
- [[Graus IT]]
- [[09-metodologia-de-projeto/index|Índice do módulo 09]]
