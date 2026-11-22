# EFATÁ – Algoritmo de Organização e Tratamento de Dados de Caixa

Projeto da disciplina **ACE: Análise Inteligente de Dados** (Engenharia de Software – UNIFSA, Teresina-PI), sob orientação da professora **Heloísa Guimarães**.

## Sobre o projeto

A **EFATÁ – Empresa de Temperos Caseiros** controla suas vendas em um caderno de papel, o que gera registros incompletos, confusos e difíceis de consultar. Este projeto entrega um algoritmo em Python (notebook do Google Colab) que lê a planilha de caixa, corrige os erros da base e gera uma planilha limpa e padronizada, com indicadores de vendas.

Questionário aplicado com a proprietária: <https://canva.link/kt0bqxdo07occjn>

## O que o algoritmo faz

- Padroniza datas em 7 formatos diferentes (barra, ponto, traço, ano curto, ISO, entre outros).
- Normaliza nomes e produtos, corrige erros de digitação e unifica variações (ex.: "fono med" e "fonomed").
- Converte números por extenso, moeda e vírgula decimal.
- Remove vazios, zeros, negativos, outliers (preço e quantidade, pelo método IQR) e duplicatas.
- Calcula faturamento, ticket médio, dias de pico e evolução mensal, com gráficos.
- Audita o resultado contra a aba de gabarito de erros (228 de 228 conferidos) e roda um checklist final de qualidade.
- Exporta a base tratada em Excel formatado (e CSV) e baixa o arquivo ao final.

## Estrutura do repositório

```
├── notebooks/   notebook de tratamento (Colab)
├── data/    planilha bruta (Empresa_efata.xlsx: dados_caixa e gabarito_erros)
├── docs/        documentação final
└── README.md
```

## Como executar

1. Abra `notebooks/Empresa_Efata.ipynb` no [Google Colab](https://colab.research.google.com/).
2. Envie `data/Empresa_efata.xlsx` para a **raiz do seu Google Drive** (Meu Drive). O notebook lê o arquivo em `/content/drive/MyDrive/Empresa_efata.xlsx`.
3. Execute tudo (**Ctrl+F9**) e autorize o acesso ao Drive quando solicitado.
4. Na última célula, o arquivo `dados_caixa_tratados.xlsx` é baixado automaticamente.

## Sobre a planilha tratada

A planilha tratada **não está versionada neste repositório** de propósito: o próprio algoritmo a gera limpa a cada execução (célula de exportação e comando de download no fim do notebook). Assim, o repositório guarda apenas a base **bruta**, o código e a documentação, e qualquer pessoa reproduz o resultado rodando o notebook.

## Resultados (base de teste)

| Indicador | Valor |
|---|---|
| Registros brutos → tratados | 547 → 472 |
| Anomalias do gabarito tratadas corretamente | 228 de 228 |
| Faturamento total | R$ 57.348,00 |
| Ticket médio | R$ 121,50 |

## Limitações

- Os dados são, em sua maioria, sintéticos (gerados no Mockaroo);

## Equipe

* Giovane Ferreira Paes Ribeiro 
* João Vitor Rodrigues Santos 
* Julia Beatriz Borges 
* Lia Rachel Ferreira de Sousa 
* Pamella Roberta dos Santos Silva
