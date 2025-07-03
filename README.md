# ✈️ Análise de Acidentes na Aviação Brasileira

Este projeto tem como objetivo explorar e analisar as ocorrências aeronáuticas no Brasil, utilizando dados públicos disponibilizados pela **CENIPA**. A ideia é aplicar técnicas de **Ciência de Dados** para gerar insights relevantes sobre os acidentes registrados, com foco em **qualidade dos dados, limpeza, integração e visualização**.

---

## 🧠 Objetivo do Projeto

Explorar e analisar as ocorrências aeronáuticas brasileiras com:

- 🎨 Criatividade  
- 📊 Profundidade analítica  
- 🧾 Storytelling eficaz

O foco é demonstrar:

- ✅ Entendimento dos dados  
- 🏗️ Estruturação de projeto  
- 🧠 Pensamento analítico (hipóteses, testes e conclusões)  
- 🗣️ Clareza na comunicação dos resultados

---

## 🔄 Etapas Realizadas

### 01. Tratamento dos Dados

- ✅ Leitura e visualização inicial  
- 🔍 Identificação de chaves primárias e estrangeiras  
- 🧹 Tratamento e limpeza dos dados  
  - Preenchimento de valores ausentes com justificativas
  - Substituição de valores inconsistentes (ex.: `'****'` → `'N/A'`)
- 🔗 Integração das tabelas
  - Merge entre tabelas `ocorrencia`, `aeronave` e `fator_contribuinte`
  - Aplicação de One-Hot Encoding na variável `fator_area` para evitar explosão de granularidade

---

## 📊 Dados Utilizados

- **Fonte:** [CENIPA - Dados Abertos do Governo Federal](https://dados.gov.br/dados/conjuntos-dados/ocorrencias-aeronauticas-da-aviacao-civil-brasileira)
- **Tabelas utilizadas:**
  - `ocorrencia.csv`
  - `aeronave.csv`
  - `fator_contribuinte.csv`

---

## 📁 Organização do Projeto



