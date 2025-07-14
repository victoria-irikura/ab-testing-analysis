# ab-testing-analysis

# 🛍️ Projeto de otimização de receita para e-commerce com Teste A/B

Este projeto foi realizado como parte do **bootcamp de Análise de Dados da Tripleten** e simula uma análise real desenvolvida em parceria com o departamento de marketing de uma grande loja online.

## 🎯 Propósito e Planejamento da Análise

O objetivo do projeto foi **aumentar a receita do e-commerce** por meio da **priorização de hipóteses de otimização**, seguida pela **avaliação estatística de um teste A/B**. A partir de uma lista de hipóteses formuladas com a equipe de marketing, foram aplicados os frameworks **ICE** e **RICE** para definir prioridades estratégicas. Em seguida, os dados do experimento A/B foram analisados para embasar decisões sobre a continuidade ou interrupção da intervenção testada.

---

## 📁 Plano de Análise

O projeto foi dividido em **três etapas principais**:

### ✅ Parte 1: Pré-processamento e preparação dos dados

- Carregamento de bibliotecas (`pandas`, `matplotlib`, `scipy`, `numpy`);
- Leitura dos arquivos `.csv`;
- Verificação e tratamento de tipos de dados, valores ausentes e duplicados;
- Ajustes nos DataFrames para facilitar a análise (renomeações, filtros e criação de colunas auxiliares).

### ✅ Parte 2: Priorização de Hipóteses

- Aplicação do framework **ICE** (Impact, Confidence, Effort);
- Aplicação do framework **RICE** (Reach, Impact, Confidence, Effort);
- Comparação entre os rankings gerados, destacando as diferenças e o efeito do alcance (`Reach`) na priorização.

### ✅ Parte 3: Análise do Teste A/B

A análise utilizou os dados de visitas e pedidos registrados ao longo do experimento para responder:

- **O grupo B teve melhor desempenho que o grupo A?**
- **A diferença entre os grupos é estatisticamente significativa?**
- **O experimento deve ser encerrado ou continuar?**

#### 🔍 Métricas e técnicas utilizadas:

- Receita acumulada por grupo (visualização);
- Tamanho médio acumulado dos pedidos;
- Diferença relativa do ticket médio entre os grupos ao longo do tempo;
- Taxa de conversão diária e cumulativa;
- Cálculo dos percentis 95 e 99 para:
  - Número de pedidos por usuário
  - Preços dos pedidos
- Definição de limites para exclusão de anomalias;
- Aplicação do teste estatístico **Mann-Whitney** (com e sem outliers);
- Interpretação dos resultados com base em cenários possíveis:
  - Liderança clara de um grupo;
  - Ausência de diferença significativa;
  - Necessidade de mais dados antes da decisão final.

---

## 🧪 Dados Utilizados

Os dados foram fornecidos em três arquivos `.csv`:

### `/datasets/hypotheses_us.csv`
Contém as hipóteses de otimização:
- `Hypotheses`: descrição da hipótese;
- `Reach`: alcance (1 a 10);
- `Impact`: impacto esperado (1 a 10);
- `Confidence`: confiança na hipótese (1 a 10);
- `Effort`: esforço necessário (1 a 10).

### `/datasets/orders_us.csv`
Contém os pedidos registrados durante o teste A/B:
- `transactionId`: ID do pedido;
- `visitorId`: ID do usuário;
- `date`: data da transação;
- `revenue`: valor do pedido;
- `group`: grupo de teste (A ou B).

### `/datasets/visits_us.csv`
Contém as visitas ao site:
- `date`: data da visita;
- `group`: grupo de teste (A ou B);
- `visits`: número de visitas na data para o grupo.

---

## 📊 Exemplos de Visualizações

Alguns gráficos construídos durante a análise:

- Receita acumulada por grupo ao longo do tempo;
- Evolução do ticket médio por grupo;
- Taxas de conversão diárias;
- Diferença percentual acumulada entre os grupos;
- Gráfico de dispersão para preços dos pedidos com outliers.

---

## 📌 Conclusão

Após análise detalhada dos dados e aplicação de testes estatísticos, o grupo B demonstrou **melhor desempenho em receita e conversão**, com **diferenças estatisticamente significativas** em relação ao grupo A. A intervenção testada deve ser mantida e expandida, com base nos resultados do experimento.

---
## 🧠 Aprendizados

Este projeto envolveu a aplicação de técnicas práticas de análise de dados para tomada de decisão orientada por testes. A integração entre marketing, dados e estatística foi essencial para transformar hipóteses em ações com impacto comprovado.

