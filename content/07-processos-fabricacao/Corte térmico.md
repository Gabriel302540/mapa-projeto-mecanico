---
title: Corte térmico (oxicorte, plasma, laser)
tags: [fabricacao, caldeiraria, corte]
fontes: [ISO 9013:2017 (corte térmico — classificação e tolerâncias), AWS Welding Handbook vol. 2 (processos de corte), Kalpakjian e Schmid Manufacturing Engineering and Technology (cap. de processos de corte), catálogos técnicos de fabricantes de equipamentos de corte]
status: rascunho
---

**Resumo:** chapas são cortadas principalmente por processos térmicos: oxicorte (aço carbono, grandes espessuras), plasma (metais condutores, espessuras finas e médias, rápido) e laser (alta precisão em chapas finas e médias). O jato d'água corta qualquer material sem calor. Cada processo tem faixa de espessura, precisão, acabamento e zona afetada pelo calor diferentes.

## O que é

| Processo | Princípio | Materiais | Espessura típica | Precisão / acabamento | Zona afetada pelo calor |
|---|---|---|---|---|---|
| **Oxicorte** | Pré-aquecimento + jato de oxigênio que **oxida** (queima) o ferro | Só aços carbono e baixa liga (não corta inox nem alumínio) | ≈ 3 mm a mais de 300 mm | Baixa; Ra 12,5–50 | Larga |
| **Plasma** | Arco elétrico constringido funde o metal; o gás o expulsa | Qualquer metal condutor (aço, inox, alumínio) | ≈ 1 a 50 mm (mais com equipamentos grandes) | Média; leve inclinação na borda (alguns graus) | Média |
| **Laser** | Feixe concentrado funde ou vaporiza o metal | Aço, inox, alumínio (conforme o laser) | ≈ 0,5 a 25 mm (aço) | **Alta**; kerf estreito; Ra 1,6–6,3 | Estreita |
| **Jato d'água abrasivo** | Água em alta pressão com abrasivo | **Qualquer** material (metais, borracha, compósitos, pedra) | Até ≈ 200 mm | Alta; borda sem alteração | **Nenhuma** |

⚠️ verificar faixas com o equipamento disponível e os fornecedores.

### Qualidade do corte (ISO 9013)

A norma classifica o corte térmico por:
- **Tolerância de perpendicularidade ou inclinação** da face cortada ($u$);
- **Altura média do perfil** (rugosidade da face, $Rz5$);
- **Tolerâncias dimensionais** por classe e espessura.

No desenho, pode-se especificar "corte térmico ISO 9013 – classe X" para definir a qualidade exigida. ⚠️ verificar as classes e valores na norma.

### Efeitos do calor

- **Zona afetada pelo calor (ZTA):** a borda cortada de aços temperáveis pode ficar **dura e frágil** (martensita), atrapalhando a usinagem e a dobra e podendo trincar. Em chapas antidesgaste e aços de alta resistência, isso exige atenção (pré-aquecimento no oxicorte, remoção da camada por usinagem, ou corte a frio).
- **Distorção** em peças finas e longas.

## Por que importa no projeto

- **A escolha do processo define tolerâncias e acabamento** das bordas: um furo cortado a plasma não serve como furo de ajuste; um furo a laser pode servir como furo de passagem de parafuso com boa precisão.
- **Chanfros para solda** podem ser feitos diretamente no corte (oxicorte e plasma com tocha inclinada).
- **Furos pequenos** (diâmetro menor que a espessura) não saem bem no plasma e no oxicorte.

## Como aplicar (passo a passo / regras práticas)

1. **Espessura grande de aço carbono:** oxicorte.
2. **Espessuras finas e médias, vários metais, produção:** plasma.
3. **Precisão, furos pequenos, contornos complexos em chapas finas e médias:** laser.
4. **Materiais sensíveis ao calor ou não metálicos:** jato d'água.
5. **Especifique a qualidade** (ISO 9013) ou deixe sobremetal para usinar bordas funcionais.
6. **Furos de ajuste** sempre usinados depois do corte.

## Norma relacionada

- **ISO 9013:2017**: classificação geométrica e de qualidade de cortes térmicos, com tolerâncias.

## Exemplo prático

**Situação:** fabricar **flanges** de chapa de 25 mm de aço A36 com 8 furos para parafusos M20 e um furo central de Ø300 onde encaixa um tubo.

- **Contorno e furo central:** plasma ou oxicorte (tolerâncias de caldeiraria bastam; o tubo é soldado).
- **Furos dos parafusos (Ø22):** com 25 mm de espessura, o diâmetro é menor que a espessura — o **plasma** pode deixar furos cônicos e irregulares. Melhor **furar na furadeira/fresadora** depois do corte, ou usar **laser** de alta potência se disponível.
- **Face de vedação:** usinada (faceamento) depois da soldagem do tubo.

> [!question] Exercício
>
> Por que não se pode cortar aço inoxidável por oxicorte?
>
> > [!success]- Resolução
> >
> > O oxicorte depende da **reação de oxidação do ferro** com o oxigênio, que gera calor e um óxido líquido que escorre. No inox, o **cromo** forma óxidos com ponto de fusão muito alto, que não escorrem e impedem a reação de continuar. Por isso, inox (e alumínio) são cortados por **plasma, laser ou jato d'água**.

## Erros comuns

- **Furos menores que a espessura feitos a plasma.**
- **Usar a borda cortada a fogo como superfície funcional** sem usinagem.
- **Ignorar a borda endurecida** em aços de alta resistência antes de dobrar ou usinar.
- **Oxicorte em inox ou alumínio.**

## Ver também

- [[Caldeiraria]]
- [[Dobra de chapas]]
- [[Tolerâncias por processo]]
- [[07-processos-fabricacao/index|Índice do módulo 07]]
