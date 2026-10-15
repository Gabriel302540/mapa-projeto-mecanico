---
title: Estilos de cota e de texto
tags: [cad, autocad, cotagem]
fontes: [Autodesk AutoCAD — documentação oficial (estilos de cota, estilos de texto, objetos anotativos), ABNT NBR 10126 (cotagem), ABNT NBR 16861 (escrita), ISO 129-1, ISO 3098-1]
status: rascunho
---

**Resumo:** estilos de texto e de cota definem, uma única vez, como textos e cotas aparecem: fonte, altura, setas, distâncias, casas decimais, tolerâncias. Com estilos anotativos, o texto e as cotas mantêm a mesma altura no papel em qualquer escala de vista. Um bom estilo reproduz automaticamente as regras de cotagem e caligrafia das normas.

## O que é

### Estilo de texto (comando STYLE)

- **Fonte:** técnica, de traço simples (por exemplo, isocp.shx ou similar), coerente com a [[Caligrafia técnica]].
- **Altura:** fixa (3,5; 5; 7 mm no papel) ou zero (definida na criação de cada texto).
- **Anotativo:** sim, para que a altura seja definida **no papel**.

### Estilo de cota (comando DIMSTYLE)

| Configuração | Valor típico (no papel) | Observação |
|---|---|---|
| Altura do texto | 3,5 mm | Ver [[Caligrafia técnica]] |
| Tamanho da seta | ≈ 3 mm | Seta cheia (ou traço oblíquo, conforme padrão) |
| Afastamento da linha de chamada ao objeto | ≈ 1 mm | |
| Extensão da linha de chamada além da linha de cota | ≈ 2 mm | |
| Espaçamento entre linhas de cota (cotagem paralela) | ≈ 7–8 mm | |
| Texto sobre a linha de cota, alinhado | Sim | Leitura conforme NBR 10126 |
| Separador decimal | Vírgula | |
| Casas decimais | 0 (cotas inteiras); tolerâncias com 2 ou 3 | |
| Supressão de zeros | Zeros à direita suprimidos nas cotas | |
| Tolerâncias | Desvios, simétrica ou limites, com altura menor | Ver [[Indicação de tolerâncias]] |

⚠️ adaptar ao padrão da equipe e conferir com a NBR 10126.

**Estilos filhos:** o AutoCAD permite variações de um estilo para tipos específicos (raios, diâmetros, ângulos), por exemplo para colocar o símbolo Ø automaticamente nas cotas de diâmetro.

### Escala anotativa

Com objetos **anotativos**, define-se a altura no papel (3,5 mm) e a escala da vista; o programa calcula o tamanho no espaço do modelo. Sem anotatividade, a altura no modelo precisa ser multiplicada pelo fator de escala:

$$
h_{\text{modelo}} = h_{\text{papel}} \times \text{fator de escala}
$$

Para uma vista em 1:10, um texto de 3,5 mm no papel tem 35 mm no modelo.

## Por que importa no projeto

- **Cotas e textos uniformes** em todos os desenhos, sem ajuste manual.
- **Mudança de escala sem retrabalho** (com anotatividade).
- **Regras da norma aplicadas automaticamente** (posição do texto, setas, decimais).
- **Cotas associativas:** a cota acompanha a geometria quando ela muda. Por isso **não se deve sobrescrever o valor** com texto digitado.

## Como aplicar (passo a passo / regras práticas)

1. **Crie os estilos no template** da equipe.
2. **Um estilo de cota principal** com variações (filhos) para diâmetro, raio e ângulo.
3. **Use anotatividade** para cotas e textos que aparecem em vistas de escalas diferentes.
4. **Nunca sobrescreva** o valor da cota com texto; corrija a geometria.
5. **Tolerâncias pelo estilo** (ou propriedades da cota), não por texto solto.

## Norma relacionada

- **ABNT NBR 10126 / ISO 129-1**: regras de cotagem.
- **ABNT NBR 16861 / ISO 3098**: escrita.

## Exemplo prático

**Situação:** num layout A2, há uma vista geral em 1:10 e um detalhe em 2:1. Sem anotatividade, as cotas do detalhe saem 20 vezes menores que as da vista geral.

- **Solução:** cotas e textos anotativos; viewport da vista geral com escala anotativa 1:10 e o do detalhe com 2:1. As cotas de ambos saem com **3,5 mm** no papel.

> [!question] Exercício
>
> Sem usar anotatividade, que altura de texto (no espaço do modelo) você deve usar para obter 3,5 mm no papel em vistas de 1:5 e de 2:1?
>
> > [!success]- Resolução
> >
> > - **1:5:** $3{,}5 \times 5 = 17{,}5$ mm no modelo.
> > - **2:1:** $3{,}5 \times 0{,}5 = 1{,}75$ mm no modelo (a vista é ampliada 2 vezes no papel).

## Erros comuns

- **Valor de cota digitado** por cima do valor medido.
- **Alturas de texto diferentes** para a mesma função em vistas de escalas diferentes.
- **Ponto decimal** em desenhos com padrão de vírgula.
- **Estilos criados em cada desenho**, em vez de vir do template.

## Ver também

- [[Cotagem]]
- [[Caligrafia técnica]]
- [[Model e layout]]
- [[10-cad/index|Índice do módulo 10]]
