# Modelagem preditiva de mortalidade em aves

Projeto de extensão da PUC-SP (fev 2026). Modelo de Machine Learning com **dados reais de lotes de frango de corte** de uma empresa do setor avícola, para prever a mortalidade.

![Prevendo a mortalidade de aves](imagens/aves-esquema.png)

## Preparação dos dados

Antes do modelo veio a parte que ninguém vê:

- **11 variáveis removidas por vazamento de dados.** Elas só existem depois do fim do ciclo e inflariam o resultado.
- Tratamento de valores ausentes.
- Transformação das variáveis categóricas.

## Modelos comparados

Ordenados pelo erro médio absoluto (MAE), quanto menor, melhor:

| # | Modelo | Papel |
|---|---|---|
| 1º | **Elastic Net (L1 + L2)** | menor erro · modelo escolhido |
| 2º | Lasso (L1) | seleção de variáveis |
| 3º | Ridge (L2) | regularização |
| 4º | Regressão Linear | referência interpretável |

## Aprendizados

Num modelo, a preparação dos dados pesa tanto quanto o algoritmo. Ser honesto com as métricas também conta: o R² mostrou que ainda faltam variáveis, e adicioná-las é o próximo passo.

## Estrutura

```
notebooks/   preparação, modelagem e avaliação
docs/        documentação do projeto
imagens/     imagens do README
```

## Ferramentas

Python · Pandas · Scikit-Learn

## Equipe

João Pedro Coelho, Kaique Munhoz, Théo Seraphim e Yuri Ivanov · Ciência de Dados e IA · PUC-SP
