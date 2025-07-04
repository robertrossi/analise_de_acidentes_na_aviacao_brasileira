
# ✈️ Análise de Ocorrências Aeronáuticas na Aviação Brasileira

Este projeto tem como objetivo explorar e analisar as ocorrências aeronáuticas da Aviação Civil, utilizando dados públicos do CENIPA. A ideia é aplicar técnicas de Ciência de Dados para gerar insights relevantes sobre os acidentes registrados, com foco em **qualidade dos dados, limpeza, integração, análise exploratória, clusterização e hipóteses estatísticas.**

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
  - `ocorrencia.csv`             Tabela com dados gerais das ocorrências aeronáuticas
  - `aeronave.csv`               Tabela com dados sobre as aeronaves envolvidas nas ocorrências aeronáuticas
  - `fator_contribuinte.csv`     Tabela com dados de Fatores contribuintes para as ocorrências aeronáuticas

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
- Pré-processamento específico para EDA
- Análise Temporal das Ocorrências
- Ocorrências por Ano
- Ocorrências por Mês
- Ocorrências por Hora e Tipo de Operação
- Análise dos Fatores Contribuintes
- Frequência dos Fatores Causadores
- Fatalidades por Localidade ao Longo dos Anos
- Armazenamento do arquivo final para etapa de hipóteses e estatística


### 3. Hipóteses Estatísticas (`03-hipoteses_estatisticas.ipynb`)
- Hipótese testada: Existem perfis distintos de ocorrências aeronáuticas que se agrupam segundo características da aeronave (como número de motores, peso e assentos), e esses perfis estão associados a diferentes fatores contribuintes (humano, material, operacional, etc.) e fases de operação.
- Clusterização com KMeans baseada em características técnicas das aeronaves, 
- Avaliação com métricas:
- Formulação de hipóteses com base nos clusters
- Testes estatísticos 
- Interpretação de p-valores e conclusões

---

## 💡 Principais Insights

- Com base na clusterização realizada sobre as ocorrências aeronáuticas, foi possível identificar três perfis bem distintos de acidentes, fortemente associados a características técnicas das aeronaves (peso, número de assentos e motores) fatores contribuintes e fases do voo.

- A análise revelou que diferentes perfis de aeronaves enfrentam riscos distintos ao longo do ciclo de voo. Estratégias genéricas de mitigação podem falhar se não forem adaptadas à realidade de cada grupo. As evidências obtidas por meio da clusterização podem servir como base para políticas de segurança mais inteligentes e personalizadas.

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
