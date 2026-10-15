---
title: Legenda (carimbo)
tags: [desenho-tecnico, folha]
fontes: [ABNT NBR 16752:2020, ISO 7200:2004, Silva et al. Desenho Técnico Moderno (cap. de normalização), Telecurso 2000 Leitura e Interpretação de Desenho Técnico Mecânico]
status: rascunho
---

**Resumo:** a legenda, também chamada de carimbo ou selo, é o quadro no canto inferior direito da folha que identifica o desenho: o que é, de quem é, quem fez, em que escala, de que material, e em qual revisão está. É a primeira coisa que se lê num desenho e a que garante que a oficina está fabricando a versão certa.

## O que é

A legenda é a **"carteira de identidade" do desenho**. Ela fica sempre no **canto inferior direito**, dentro do quadro, e continua visível quando a folha é dobrada para o arquivo (ver [[Formatos de folha]]).

Os campos variam de empresa para empresa, mas costumam se dividir em três grupos:

| Grupo | Campos típicos | Para que serve |
|---|---|---|
| **Identificação** | Proprietário (empresa, logotipo), número do desenho, título, revisão, folha (1 de N) | Saber exatamente que documento é este e se é a versão mais nova |
| **Técnico** | Escala, unidade, método de projeção (símbolo do 1º ou 3º diedro), material, tratamento térmico, tolerâncias gerais, acabamento geral, massa | Informações que valem para o desenho inteiro e não precisam ser repetidas em cada cota |
| **Responsabilidade** | Desenhista, verificador, aprovador, datas | Rastreabilidade: quem fez e quem liberou |

A norma internacional **ISO 7200** define os nomes dos campos, o conteúdo esperado e o número de caracteres de cada um, separando campos obrigatórios de opcionais. Fontes secundárias citam como obrigatórios, entre outros, o **proprietário legal**, o **número de identificação** e a **data de emissão**. ⚠️ verificar a lista completa na ISO 7200.

Muitas empresas acrescentam, junto à legenda:

- **Quadro de revisões:** tabela com cada revisão (A, B, C... ou 0, 1, 2...), a data, uma descrição curta do que mudou e quem aprovou.
- **Lista de peças:** em desenhos de conjunto, a tabela com item, quantidade, denominação, material e código. Ela fica logo acima da legenda e é numerada de baixo para cima, para poder crescer sem apagar nada. Ver [[09-metodologia-de-projeto/index|Metodologia de projeto]].

## Por que importa no projeto

- **Evita fabricar a versão errada.** Na oficina circulam cópias antigas. O campo de revisão, junto com o quadro de revisões, é o que diz se aquela cópia ainda vale.
- **Concentra as informações gerais.** Em vez de escrever a tolerância em cada cota, a legenda diz, por exemplo, "tolerâncias gerais conforme ISO 2768-m"; só as cotas críticas recebem tolerância própria. Ver [[02-tolerancias-ajustes/index|Tolerâncias e ajustes]].
- **Define como ler o desenho.** O símbolo do método de projeção diz se as vistas estão no 1º ou no 3º diedro. Ler um desenho americano (3º diedro) como se fosse brasileiro (1º diedro) inverte as vistas. Ver [[Projeções ortográficas]].
- **Rastreabilidade e responsabilidade técnica.** Em caso de falha de um componente, a legenda mostra quem projetou, quem verificou e quando o desenho foi liberado.
- **Padronização de componentes.** Um número de desenho único e bem estruturado é a base para cadastrar a peça no sistema de manutenção e no almoxarifado.

## Como aplicar (passo a passo / regras práticas)

1. **Use sempre o modelo oficial da empresa.** Não crie legenda própria. Em CAD, ela é um bloco com atributos que já vem no *template* da folha. Ver [[10-cad/index|CAD]].
2. **Preencha o título do geral para o específico**, do jeito que se procura no arquivo: "EIXO — ROLO SUPERIOR — TERNO 1", e não "Eixo do rolo de cima".
3. **Número do desenho:** siga a regra de codificação da empresa. Ele deve ser único; nunca reaproveite o número de um desenho cancelado.
4. **Escala:** escreva a escala principal (por exemplo, `1:10`). Se houver detalhes em outra escala, indique a escala embaixo de cada detalhe e, na legenda, algo como "1:10 (indicadas)". Ver [[Escalas]].
5. **Unidade:** em mecânica, as cotas ficam em milímetros. Basta "mm" na legenda, e as cotas são escritas sem unidade.
6. **Método de projeção:** insira o símbolo do diedro usado. No Brasil, o padrão é o 1º diedro.
7. **Material e tratamento:** use a designação normalizada (por exemplo, "SAE 4140 — temperado e revenido, 28–32 HRC"), e não nomes comerciais vagos. Ver [[06-materiais/index|Materiais]].
8. **Tolerâncias e acabamento gerais:** declare-os na legenda ou numa nota geral, para não repetir em cada cota.
9. **Revisão:** a cada alteração, incremente a revisão, registre no quadro de revisões o que mudou e marque a região alterada no desenho (com um triângulo ou nuvem de revisão, conforme o padrão da empresa).

## Norma relacionada

- **ABNT NBR 16752:2020**: posição da legenda na folha e sua relação com o dobramento. ⚠️ verificar as dimensões da legenda (materiais didáticos citam 180 mm de largura) e os campos mínimos exigidos.
- **ISO 7200:2004**: campos de dados em legendas e cabeçalhos de documentos. Define nomes, conteúdo e tamanho dos campos, e quais são obrigatórios. Confirmada em revisão sistemática em 2025, portanto vigente. ⚠️ verificar a lista de campos obrigatórios.
- A legenda antiga da NBR 10068 tinha valores de largura diferentes (178 mm, ou 175 mm nos formatos A0 e A1), que ainda aparecem em apostilas.

## Exemplo prático

**Situação:** um eixo de rolo de moenda foi redimensionado após uma falha por fadiga. O raio de concordância no ressalto do mancal passou de R5 para R15, e o material mudou de SAE 1045 para SAE 4140 temperado e revenido.

Como fica a legenda depois da alteração:

| Campo | Antes | Depois |
|---|---|---|
| Título | EIXO — ROLO SUPERIOR — TERNO 1 | (igual) |
| Número | DES-MOE-0123 | (igual: é a mesma peça, só revisada) |
| Revisão | B | **C** |
| Material | SAE 1045 normalizado | **SAE 4140 temperado e revenido, 28–32 HRC** ⚠️ verificar faixa de dureza com o projeto |
| Escala | 1:10 (indicadas) | (igual) |
| Data | 03/2025 | **10/2026** |

No **quadro de revisões**, entra uma linha: "Rev. C — 10/2026 — Raio de concordância R5→R15 no ressalto do mancal; material alterado para SAE 4140 T&R — elaborado por / verificado por (iniciais)". No desenho, o raio alterado recebe o símbolo de revisão "C".

O resultado é que qualquer cópia **Rev. B** que ainda esteja na oficina é imediatamente reconhecida como obsoleta.

## Erros comuns

- **Revisar o desenho sem mudar a revisão na legenda.** É o erro mais perigoso: a oficina não percebe que algo mudou.
- **Título vago** ("Peça 1", "Suporte"), que torna o desenho impossível de encontrar depois.
- **Escala da legenda diferente da escala real**, por exemplo depois de mudar a escala da vista no CAD sem atualizar o atributo.
- **Esquecer o símbolo do diedro** em desenhos que vão para fornecedores estrangeiros.
- **Material sem tratamento ou dureza**, deixando a decisão para o fornecedor.
- **Lista de peças numerada de cima para baixo**, o que obriga a redesenhar a tabela quando um item é acrescentado.

## Ver também

- [[Formatos de folha]]
- [[Escalas]]
- [[Projeções ortográficas]]
- [[01-desenho-tecnico/index|Índice do módulo 01]]
