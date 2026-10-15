---
title: Segurança de máquinas
tags: [metodologia, seguranca, nr-12]
fontes: [NR-12 — Segurança no Trabalho em Máquinas e Equipamentos (texto consolidado no portal do Ministério do Trabalho e Emprego) ⚠️ verificar versão vigente, ABNT NBR ISO 12100 (apreciação e redução de riscos), ABNT NBR ISO 13857 (distâncias de segurança), ABNT NBR ISO 13850 (parada de emergência), ABNT NBR ISO 13849-1 (partes de sistemas de comando relacionadas à segurança), ABNT NBR ISO 14120 (proteções)]
status: rascunho
---

**Resumo:** no Brasil, a NR-12 estabelece requisitos mínimos de segurança para máquinas e equipamentos, desde o projeto até a operação e a manutenção. A base técnica é a apreciação de riscos (ABNT NBR ISO 12100): identificar perigos, estimar e avaliar riscos e reduzi-los numa ordem de prioridade — primeiro eliminando o perigo no projeto, depois com proteções e dispositivos, e por último com informações e procedimentos.

## O que é

### Apreciação de riscos (ISO 12100)

1. **Determinar os limites da máquina:** uso pretendido, mau uso previsível, fases da vida (transporte, montagem, operação, limpeza, manutenção, desmontagem).
2. **Identificar os perigos:** mecânicos (esmagamento, cisalhamento, arraste, enrolamento, impacto, projeção), elétricos, térmicos, ruído, vibração, materiais e substâncias, ergonomia.
3. **Estimar o risco:** combinação da **gravidade** do dano com a **probabilidade** de ocorrência (exposição, ocorrência do evento, possibilidade de evitar).
4. **Avaliar** se o risco é aceitável.
5. **Reduzir o risco** e repetir.

### Ordem de prioridade na redução de riscos

1. **Medidas de projeto inerentemente seguras:** eliminar o perigo ou reduzir a energia (afastar pontos de esmagamento, reduzir velocidades e forças, eliminar cantos vivos, projetar a manutenção sem acesso a partes móveis).
2. **Proteções e dispositivos de segurança:** proteções fixas, móveis intertravadas, cortinas de luz, comandos bimanuais, parada de emergência.
3. **Informações para uso:** sinalização, manuais, treinamento, procedimentos (inclusive bloqueio e etiquetagem de energias na manutenção).

### Elementos frequentes na NR-12 e normas associadas

| Tema | Ideia principal | Norma técnica de apoio |
|---|---|---|
| **Proteções fixas** | Só removíveis com ferramenta; impedem acesso às zonas de perigo | ABNT NBR ISO 14120 |
| **Distâncias de segurança** | Distância entre a proteção (ou abertura) e o perigo, em função do tamanho da abertura e da parte do corpo | ABNT NBR ISO 13857 |
| **Proteções móveis intertravadas** | Abrir a proteção para a máquina | ABNT NBR ISO 14119 ⚠️ verificar |
| **Parada de emergência** | Dispositivos acessíveis que levam a máquina a uma parada segura | ABNT NBR ISO 13850 |
| **Sistemas de comando de segurança** | Confiabilidade dos circuitos de segurança (categorias, nível de desempenho PL) | ABNT NBR ISO 13849-1 |
| **Transmissões de força** | Correias, correntes, engrenagens, acoplamentos e eixos girantes acessíveis devem ser protegidos | NR-12 |
| **Manuais e capacitação** | Informações para operação e manutenção segura | NR-12 |

⚠️ verificar todos os requisitos no **texto consolidado vigente da NR-12** (portal do Ministério do Trabalho e Emprego) e nas normas ABNT citadas. A NR-12 passou por várias alterações desde a grande revisão de 2010.

## Por que importa no projeto

- **Obrigação legal:** máquinas novas e modificadas devem atender à NR-12; o projeto é o momento mais barato de fazer isso.
- **Transmissões de potência** (acoplamentos, correias, correntes, eixos expostos) e **pontos de esmagamento** entre rolos são perigos clássicos de equipamentos pesados.
- **Manutenção:** a maioria dos acidentes graves acontece em intervenções (limpeza, desentupimento, ajustes) com a máquina energizada ou com energia acumulada (gravidade, molas, hidráulica).

## Como aplicar (passo a passo / regras práticas)

1. **Faça a apreciação de riscos** ainda no projeto conceitual e atualize no detalhamento.
2. **Elimine perigos pelo projeto** sempre que possível (pontos de lubrificação fora das proteções, regulagens sem abrir proteções).
3. **Projete proteções** com as distâncias de segurança corretas e que não atrapalhem a operação (proteções que atrapalham são removidas).
4. **Preveja pontos de bloqueio** de energia (elétrica, hidráulica, pneumática, gravidade).
5. **Inclua os requisitos de segurança** na lista de requisitos e na matriz de decisão. Ver [[Levantamento de requisitos]].
6. **Documente** a apreciação de riscos e as medidas adotadas.

## Norma relacionada

- **NR-12** (Ministério do Trabalho e Emprego): segurança no trabalho em máquinas e equipamentos.
- **ABNT NBR ISO 12100**: princípios gerais de projeto — apreciação e redução de riscos.
- **ABNT NBR ISO 13857, 13850, 13849-1, 14120, 14119**: normas técnicas de apoio.

## Exemplo prático

**Situação:** um acionamento com motor, acoplamento elástico, redutor e acoplamento de engrenagens até o eixo de um rolo, ao nível do piso.

| Perigo | Medida |
|---|---|
| Enrolamento em acoplamentos e eixos girantes | Proteção fixa (chapa perfurada ou tela) envolvendo os acoplamentos, com aberturas e distâncias conforme a NBR ISO 13857 |
| Inspeção do acoplamento | Janela de inspeção com tela, sem precisar remover a proteção |
| Lubrificação do acoplamento | Graxeira remota trazida para fora da proteção |
| Manutenção | Ponto de bloqueio da chave do motor; procedimento de bloqueio e etiquetagem |
| Ponto de esmagamento entre rolos | Proteções e distâncias; acesso para limpeza somente com o equipamento parado e bloqueado |

> [!question] Exercício
>
> Coloque em ordem de prioridade, segundo a ISO 12100, as medidas: (a) placa de advertência; (b) proteção fixa; (c) reposicionar a graxeira para fora da área de risco.
>
> > [!success]- Resolução
> >
> > 1. **(c)** medida de projeto inerentemente segura (elimina a necessidade de acesso);
> > 2. **(b)** proteção (salvaguarda);
> > 3. **(a)** informação para uso.

## Erros comuns

- **Pensar em segurança só no fim do projeto** ("depois a gente coloca uma proteção").
- **Proteções que atrapalham a operação ou a manutenção** e acabam sendo retiradas.
- **Distâncias de segurança erradas** (tela com malha grande demais perto do perigo).
- **Esquecer energias acumuladas** (gravidade, molas, acumuladores hidráulicos).

## Ver também

- [[Levantamento de requisitos]]
- [[Acoplamentos]]
- [[Correias e correntes]]
- [[09-metodologia-de-projeto/index|Índice do módulo 09]]
