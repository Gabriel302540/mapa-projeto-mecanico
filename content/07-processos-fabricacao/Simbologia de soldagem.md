---
title: Simbologia de soldagem
tags: [fabricacao, soldagem, desenho]
fontes: [AWS A2.4 (símbolos de soldagem, brasagem e ensaios não destrutivos), ISO 2553:2019 (representação simbólica de soldas), Marques, Modenesi e Bracarense Soldagem: Fundamentos e Tecnologia (cap. de simbologia), ABNT NBR 5874 (terminologia de soldagem) ⚠️ verificar]
status: rascunho
---

**Resumo:** soldas são indicadas no desenho por um símbolo composto: uma linha de referência, uma seta que aponta para a junta e um símbolo básico do tipo de solda (filete, chanfro em V, bisel...), com dimensões e informações complementares. Há dois sistemas em uso: o americano (AWS A2.4) e o internacional (ISO 2553). Eles diferem principalmente na forma de indicar o lado da seta.

## O que é

### Elementos do símbolo

| Elemento | Função |
|---|---|
| **Seta** | Aponta para a junta. Define o "lado da seta" |
| **Linha de referência** | Linha horizontal onde ficam os símbolos |
| **Símbolo básico** | Tipo de solda (filete, V, bisel, J, U, I, tampão, ponto, revestimento) |
| **Dimensões** | Perna ou garganta do filete, profundidade do chanfro, comprimento, passo |
| **Símbolos suplementares** | Solda em todo o contorno (círculo), solda de campo (bandeira), contorno (plano, convexo, côncavo), acabamento, cobre-junta |
| **Cauda** | Processo, procedimento (EPS), outras referências |

### Símbolos básicos mais comuns

| Solda | Símbolo |
|---|---|
| Filete | Triângulo retângulo (◺) |
| Chanfro em V | V |
| Chanfro em meio V (bisel) | Meio V (\|/) |
| Chanfro em J / U | J / U |
| Sem chanfro (I, juntas de topo retas) | Duas barras verticais (‖) |
| Tampão / em furo | Retângulo |
| Revestimento | Dois semicírculos (︵︵) |

### Lado da seta e outro lado

**AWS A2.4:**
- Símbolo **abaixo** da linha de referência → solda **do lado da seta**.
- Símbolo **acima** → solda **do outro lado**.
- Símbolo dos dois lados → solda dos dois lados.

**ISO 2553 (sistema A, o mais usado na Europa):**
- Usa **duas linhas de referência**: uma contínua e uma tracejada (acima ou abaixo da contínua).
- Símbolo na **linha contínua** → solda **do lado da seta**.
- Símbolo na **linha tracejada** → solda **do outro lado**.
- Soldas simétricas dos dois lados dispensam a linha tracejada.

⚠️ verificar os detalhes nas normas. Antes de ler um desenho, **confira qual sistema ele usa**: o mesmo desenho, lido pelo sistema errado, coloca a solda do lado oposto.

### Dimensão do filete

- **AWS:** a dimensão à esquerda do símbolo é a **perna** ($z$).
- **ISO:** escreve-se **"a"** (garganta) ou **"z"** (perna) antes do número: "a5" ou "z7".

Relação, para filete de pernas iguais a 45°:

$$
a = z\cos 45° \approx 0{,}707\,z
$$

### Soldas intermitentes

Indicadas por **comprimento-passo** à direita do símbolo, por exemplo "50-150" (cordões de 50 mm a cada 150 mm de centro a centro, na AWS). Na ISO: número de cordões × comprimento (passo). ⚠️ verificar.

## Por que importa no projeto

- **A garganta define a resistência** do filete (ver [[Juntas e chanfros]]). Confundir perna com garganta muda a resistência em cerca de 40 %.
- **Lado errado** = solda no lugar errado, interferindo com outras peças.
- **Solda de campo** (bandeira) indica que a solda é feita na montagem, não na oficina: muda o planejamento e o processo.

## Como aplicar (passo a passo / regras práticas)

1. **Declare o sistema** usado (AWS A2.4 ou ISO 2553) numa nota do desenho.
2. **Aponte a seta para a junta**; em chanfros de um lado só (bisel, J), a seta aponta para a peça que será chanfrada.
3. **Indique a dimensão** (perna ou garganta, com a letra na ISO), o comprimento se não for contínuo, e os símbolos suplementares.
4. **Use a cauda** para referenciar a EPS quando houver.
5. **Não repita** símbolos para soldas iguais: use notas ("todos os filetes não indicados: a4").

## Norma relacionada

- **AWS A2.4**: símbolos de soldagem (padrão americano).
- **ISO 2553:2019**: representação simbólica de soldas.
- **ISO 4063**: números dos processos de soldagem, usados na cauda.

## Exemplo prático

**Situação:** um suporte em T (chapa vertical soldada numa chapa de base) com **filete de 6 mm de perna nos dois lados, em todo o comprimento**, feito na oficina por MAG.

- **AWS:** linha de referência com triângulo **acima e abaixo**, "6" à esquerda de cada triângulo, cauda com "GMAW".
- **ISO:** linha contínua com triângulos dos dois lados (sem tracejada, por ser simétrica), "z6" (ou "a4", já que $0{,}707 \times 6 \approx 4{,}2$), cauda com "135".

> [!question] Exercício
>
> Num desenho AWS, um símbolo de filete aparece **só acima** da linha de referência, com "8" à esquerda. Onde fica a solda e qual a garganta?
>
> > [!success]- Resolução
> >
> > Acima da linha, no sistema AWS, significa **do outro lado** da junta (oposto ao lado para onde a seta aponta). O "8" é a **perna** de 8 mm; a garganta é $0{,}707 \times 8 \approx 5{,}7$ mm.

## Erros comuns

- **Ler desenho ISO pelo sistema AWS** (ou o contrário).
- **Confundir perna e garganta.**
- **Seta apontando para a peça errada** em chanfros de um lado só.
- **Esquecer a bandeira** de solda de campo.

## Ver também

- [[Processos de soldagem]]
- [[Juntas e chanfros]]
- [[Desenho de conjunto e de detalhe]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
