
# ✈️ Análise de Ocorrências Aeronáuticas na Aviação Brasileira

Este projeto tem como objetivo explorar e analisar as ocorrências aeronáuticas no Brasil, utilizando dados públicos do CENIPA. A ideia é aplicar técnicas de Ciência de Dados para gerar insights relevantes sobre os acidentes registrados, com foco em **qualidade dos dados, limpeza, integração, análise exploratória, clusterização e hipóteses estatísticas.**

---

## 📌 Índice

1. [Objetivo do Projeto](#objetivo-do-projeto)
2. [Dados Utilizados](#dados-utilizados)
3. [Etapas da Análise](#etapas-da-análise)
4. [Principais Insights](#principais-insights)
5. [Como Reproduzir](#como-reproduzir)
6. [Tecnologias e Bibliotecas](#tecnologias-e-bibliotecas)
7. [Autor](#autor)

---

## 🧠 Objetivo do Projeto

Explorar e analisar as ocorrências aeronáuticas brasileiras com foco em:

- 🎨 Criatividade
- 📊 Profundidade analítica
- 🧾 Storytelling eficaz

Demonstrando:

- ✅ Entendimento dos dados
- 🏗️ Estruturação de projeto
- 🧠 Pensamento analítico (hipóteses, testes e conclusões)
- 🗣️ Clareza na comunicação dos resultados

---

## 📊 Dados Utilizados

- Fonte: [CENIPA - Dados Abertos do Governo Federal](https://dados.gov.br/dataset/ocorrencias-aeronauticas-da-aviacao-civil-brasileira)
- Tabelas utilizadas:
  - `ocorrencia.csv`
  - `aeronave.csv`
  - `fator_contribuinte.csv`

---

## 🔄 Etapas da Análise

### 1. Tratamento dos Dados (`01-Tratamento_dos_dados.ipynb`)
- ✅ Leitura e inspeção inicial dos dados
- 🔍 Identificação de chaves primárias e estrangeiras
- 🧹 Limpeza e padronização (ex.: '****' → 'N/A')
- 📉 Preenchimento de valores ausentes com justificativas
- 🔗 Merge entre tabelas: ocorrência, aeronave, fator_contribuinte
- 🧠 Criação de variáveis numéricas e codificação (`One-Hot` para `fator_area`)

### 2. Análise Exploratória (`02-Analise_exploratoria.ipynb`)
- Distribuição temporal das ocorrências
- Análise dos tipos de danos, fases do voo e localizações
- Clusterização com KMeans baseada em características técnicas das aeronaves
- Avaliação com métricas:
  - Silhouette Score: `0.352`
  - Calinski-Harabasz: `405.5`
  - Davies-Bouldin: `1.13`

### 3. Hipóteses Estatísticas (`03-hipoteses_estatisticas.ipynb`)
- Formulação de hipóteses com base nos clusters
- Testes estatísticos (Qui-quadrado, ANOVA)
- Interpretação de p-valores e conclusões

---

## 💡 Principais Insights

- **Erro humano** é mais comum em aviões grandes, apontando desafios operacionais mesmo com protocolos robustos.
- **Aeronaves leves** concentram acidentes com maior gravidade (nível de dano), especialmente em fases de pouso.
- Três **perfis distintos** foram revelados com base em peso, assentos e número de motores, com associação a diferentes fatores contribuintes.
- A fase de voo crítica varia conforme o cluster, revelando onde esforços de prevenção devem ser direcionados.

---

## ⚙️ Como Reproduzir

1. Clone o repositório:
```bash
git clone https://github.com/seu-usuario/ocorrencias-aeronauticas.git
cd ocorrencias-aeronauticas
```

2. Instale os pacotes necessários:
```bash
pip install -r requirements.txt
```

3. Execute os notebooks na ordem:
   - `01-Tratamento_dos_dados.ipynb`
   - `02-Analise_exploratoria.ipynb`
   - `03-hipoteses_estatisticas.ipynb`

---

## 💻 Tecnologias e Bibliotecas

- Python 3.10+
- Jupyter / Google Colab
- pandas, numpy, seaborn, matplotlib
- scikit-learn, scipy
- chardet

---

## 👨‍💻 Autor

**Robert Rossi Silva de Mesquita**  
Cientista de Dados  
[🔗 LinkedIn](https://www.linkedin.com/in/seu-perfil-aqui)
