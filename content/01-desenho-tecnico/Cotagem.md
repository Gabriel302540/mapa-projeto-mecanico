---
title: "Cotagem: princípios"
tags: [desenho-tecnico, cotagem]
fontes: [ABNT NBR 10126:1987, ISO 129-1, French e Vierck Desenho Técnico e Tecnologia Gráfica (cap. de cotagem), Silva et al. Desenho Técnico Moderno (cap. de cotagem), Telecurso 2000 Leitura e Interpretação de Desenho Técnico Mecânico]
status: rascunho
---

**Resumo:** cotar é escrever no desenho todas as medidas necessárias para fabricar e inspecionar a peça, uma única vez cada, de forma clara e a partir das referências certas. A forma de organizar as cotas (em cadeia, em paralelo, por coordenadas) muda o acúmulo de tolerâncias e, portanto, a precisão final da peça.

## O que é

### Elementos de uma cota

| Elemento | Linha | Regra |
|---|---|---|
| **Linha auxiliar (de chamada)** | Contínua estreita | Prolonga a aresta até a cota. Começa com um pequeno afastamento do contorno e ultrapassa a linha de cota em cerca de 2 mm |
| **Linha de cota** | Contínua estreita | Paralela à medida; não é interrompida, mesmo se o elemento for |
| **Limites da linha de cota** | Setas (cheias, em geral) ou traços oblíquos | Use o mesmo tipo no desenho todo |
| **Valor (cota)** | Escrita técnica, altura ≥ 3,5 mm | Acima da linha de cota, sem tocá-la, de preferência no meio |

Linhas de centro e de contorno **não** podem ser usadas como linha de cota, mas podem servir como linha auxiliar (no caso das linhas de centro, prolongando-as). ⚠️ verificar na NBR 10126.

### Tipos de cota quanto à função

- **Cota funcional:** essencial para a peça funcionar (um diâmetro de assento de rolamento, a distância entre furos que recebem pinos). Deve ser cotada **diretamente**, nunca obtida por soma ou subtração de outras.
- **Cota não funcional:** necessária para fabricar, mas sem efeito na função (comprimento de uma ponta livre).
- **Cota auxiliar:** pode ser calculada a partir de outras e é dada só para informação, **entre parênteses** e sem tolerância. Por exemplo, o comprimento total quando os trechos já estão cotados.

### Sistemas de cotagem

| Sistema | Como é | Efeito nas tolerâncias |
|---|---|---|
| **Em cadeia (em série)** | Cada cota começa onde termina a anterior | As tolerâncias **se somam**: o erro da posição final é a soma dos erros de cada trecho |
| **Em paralelo** | Todas as cotas partem de uma mesma **referência** | Cada posição tem só o seu próprio erro, sem acúmulo |
| **Aditiva (sobreposta)** | Igual à paralela, mas numa linha de cota só, com origem marcada por um círculo e valores escritos ao longo da linha | Mesmo efeito da paralela, ocupando menos espaço |
| **Por coordenadas** | Posições dadas em X e Y a partir de uma origem, muitas vezes numa tabela | Ideal para peças com muitos furos e para usinagem CNC |
| **Combinada** | Mistura das anteriores | A mais usada na prática |

### Por que o sistema muda a precisão

Considere quatro trechos com tolerância de ±0,1 mm cada.

- **Em cadeia:** a posição do último elemento em relação à origem acumula os quatro erros. No pior caso:
  $$\Delta_{\text{final}} = \pm(0{,}1 + 0{,}1 + 0{,}1 + 0{,}1) = \pm 0{,}4\ \text{mm}$$
- **Em paralelo:** cada posição é medida direto da referência, então o último elemento tem só **±0,1 mm**.

Esse fenômeno é o **acúmulo (empilhamento) de tolerâncias**, tratado no [[02-tolerancias-ajustes/index|módulo de tolerâncias]].

## Por que importa no projeto

- **Uma cota faltando** para a fabricação; uma cota sobrando cria contradição (se a soma dos trechos não bater com o total, qual vale?).
- **O sistema de cotagem define o que é controlado.** Se dois furos precisam estar a 250 ± 0,05 mm um do outro, essa distância tem de ser cotada diretamente; se ela resultar de duas cotas a partir da borda, o erro dobra.
- **A referência de cotagem deve ser a referência funcional e de fabricação**: a face que encosta no apoio, o eixo de simetria, o furo principal. Assim, quem usina mede do mesmo lugar que o projetista pensou.

## Como aplicar (passo a passo / regras práticas)

1. **Escolha as referências:** normalmente uma face usinada de apoio e um eixo de simetria ou de rotação.
2. **Cote primeiro as medidas funcionais**, diretamente a partir das referências.
3. **Complete com as cotas de fabricação**, evitando cadeias fechadas (todos os trechos e o total ao mesmo tempo). Se o total for útil, dê-o como **cota auxiliar**, entre parênteses.
4. **Cada elemento é cotado uma vez só**, na vista em que aparece mais claramente e em verdadeira grandeza.
5. **Não cote arestas ocultas:** faça um corte. Ver [[Cortes e seções]].
6. **Posicione as cotas fora da peça**, com a menor à mais próxima do contorno e as maiores por fora, para que as linhas auxiliares não cruzem as linhas de cota. Distância típica: cerca de 10 mm do contorno até a primeira linha de cota e 7 a 8 mm entre linhas sucessivas.
7. **Orientação do texto:** cotas legíveis de baixo ou da direita da folha (as horizontais lidas normalmente, as verticais lidas girando a folha no sentido horário). ⚠️ verificar o método admitido na NBR 10126.
8. **Cota fora de escala:** se o desenho não foi alterado mas a cota foi, sublinhe o valor.
9. **Agrupe as cotas de um mesmo elemento** (diâmetro e profundidade de um furo) na mesma vista.

## Norma relacionada

- **ABNT NBR 10126:1987**, *Cotagem em desenho técnico*: elementos de cotagem, regras de apresentação e métodos de cotagem. Em 1998 recebeu uma errata. ⚠️ verificar se a norma continua vigente ou se foi revisada.
- **ISO 129-1**: representação de dimensões e tolerâncias (princípios gerais).

## Exemplo prático

**Situação:** uma **placa de base** de um motorredutor tem quatro furos para os chumbadores do motor e quatro para os do redutor. O alinhamento entre o eixo do motor e o do redutor depende da posição relativa desses dois grupos de furos.

- **Referências:** a borda esquerda usinada (X) e a borda inferior usinada (Y).
- **Cotagem errada:** furos do motor cotados da borda esquerda; furos do redutor cotados em cadeia a partir dos furos do motor, trecho por trecho. Cada trecho soma erro, e o desalinhamento entre os eixos fica maior que o admitido pelo acoplamento.
- **Cotagem certa:** todos os furos cotados **em paralelo ou por coordenadas** a partir das duas bordas de referência, e a **distância funcional** entre os grupos (a que garante o alinhamento) cotada diretamente com a tolerância necessária. O comprimento total da placa entra como cota auxiliar, se for útil.

> [!question] Exercício 1
>
> Uma peça tem cinco furos alinhados. As distâncias entre furos consecutivos são cotadas em cadeia, cada uma com ±0,05 mm. Qual é a variação máxima possível da distância entre o primeiro e o último furo? E se as posições fossem cotadas em paralelo a partir do primeiro furo?
>
> > [!success]- Resolução
> >
> > Cinco furos formam **quatro** intervalos.
> > - **Em cadeia:** pior caso $= 4 \times 0{,}05 = \pm 0{,}20$ mm.
> > - **Em paralelo** a partir do primeiro furo: a posição do último é uma cota direta, com **±0,05 mm**.
> >
> > Se a distância entre o primeiro e o último furo for funcional, ela deve ser cotada diretamente.

> [!question] Exercício 2
>
> Um eixo tem três trechos cotados: 120, 80 e 200 mm, e também o comprimento total 400 mm, todos com tolerância geral. O que está errado e como corrigir?
>
> > [!success]- Resolução
> >
> > É uma **cadeia fechada**: o total é a soma dos trechos, então há uma cota sobrando. Se cada trecho variar dentro da tolerância, a soma pode não respeitar a tolerância do total, e o desenho fica contraditório. **Correção:** retire a cota do trecho menos importante funcionalmente (ou escreva o total como cota auxiliar, "(400)", sem tolerância).

## Erros comuns

- **Cadeias fechadas** (todos os trechos mais o total).
- **Cotar a partir de arestas ocultas** ou de faces brutas (não usinadas) quando há uma face usinada disponível.
- **Linhas de cota cruzando linhas auxiliares** por posicionar as cotas grandes por dentro.
- **Cotar a mesma medida em duas vistas.**
- **Deixar a cota funcional resultar de uma soma**, em vez de cotá-la diretamente.

## Ver também

- [[Cotagem de elementos]]
- [[Caligrafia técnica]]
- [[Tipos de linha]]
- [[02-tolerancias-ajustes/index|Tolerâncias e ajustes]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
