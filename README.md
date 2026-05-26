# Estudo de Predição e Análise de Insuficiência Cardíaca

## 1. Introdução
A insuficiência cardíaca (IC) é uma condição clínica complexa e de caráter progressivo, caracterizada pela incapacidade do coração de bombear sangue em quantidade suficiente para suprir as demandas metabólicas teciduais, ou de fazê-lo apenas sob pressões de enchimento elevadas. Esta síndrome representa um dos maiores desafios de saúde pública global, estando associada a altas taxas de hospitalização, morbidade expressiva e mortalidade elevada.

Com o advento da medicina baseada em dados e das técnicas de Aprendizado de Machine (*Machine Learning*), tornou-se possível explorar bases de dados clínicas para identificar biomarcadores e fatores de risco críticos. A predição precoce da sobrevivência e a estratificação de risco de pacientes diagnosticados com insuficiência cardíaca desempenham um papel vital na otimização dos protocolos terapêuticos e na alocação eficiente de recursos hospitalares.

## 2. Metodologia

1. **Analise dos dataset Heart Failure Clinical Records (UCI):** Foi baixado o dataset, preparado o ambiente de trabalho e analise de dados o dataset.
2. **Pré-processamento de Dados:**
   * Identificação da variável alvo e tranformação da mesma em fator, deixando de ser binário (0 e 1) e passando a ser Vivo ou Óbito.
   * Divisão dos valores da variável platelets (plaquetas) por mil, reduzindo processamento e sem interferir na triagem médica.
   * Divisão do conjunto de dados em partições de treino e teste (80% para treino e 20% para teste).
3. **Treinamento de Modelos:**
   * Árvore de Decisão: O modelo escolhido foi a árvore de decisão, por sua fácil implementação e transparência, tendo seu treinamento sido efetuado com 80% do dataset.
4. **Avaliação de Desempenho:** A modelo da árvore de decisão foi avaliado através da matriz de confusão, do CI 95% e Kappa.

## 3. Ambiente de Desenvolvimento (Google Colab)
Todo o desenvolvimento prático e visualização gráfica deste projeto foram centralizados no ambiente em nuvem do **Google Colab**. 

O notebook estruturado contém o código documentado passo a passo, desde o carregamento do dataset até a plotagem das matrizes de confusão.

* **Google Colab:** [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1dOJ2pdN80SzitlOXuLWPS6ELn7cdF86B?usp=sharing)

## 4. Dataset utilizado
O modelo e as análises foram construídos utilizando o conjunto de dados **Heart Failure Clinical Records** (UCI Machine Learning Repository).

### Atributos do Dataset:
O dataset mapeia dados de pacientes acompanhados durante um período de acompanhamento médico, contendo as seguintes características:

| Variável | Tipo | Descrição |
| :--- | :--- | :--- |
| **Idade** | Contínua | Idade do paciente (anos) |
| **Anemia** | Booleana | Diminuição de glóbulos vermelhos ou hemoglobina (0: Não, 1: Sim) |
| **Creatinina Fosfoquinase** | Contínua | Nível da enzima CPK no sangue (mcg/L) |
| **Diabetes** | Booleana | Se o paciente possui histórico de diabetes (0: Não, 1: Sim) |
| **Fração de Ejeção** | Contínua | Porcentagem de sangue que deixa o coração a cada contração (%) |
| **Pressão Arterial Alta** | Booleana | Se o paciente possui hipertensão (0: Não, 1: Sim) |
| **Plaquetas** | Contínua | Quantidade de plaquetas no sangue (kiloplatelets/mL) |
| **Creatinina Sérica** | Contínua | Nível de creatinina sérica no sangue (mg/dL) |
| **Sódio Sérico** | Contínua | Nível de sódio sérico no sangue (mEq/L) |
| **Sexo** | Booleana | Gênero do paciente (0: Mulher, 1: Homem) |
| **Tabagismo** | Booleana | Se o paciente fuma (0: Não, 1: Sim) |
| **Tempo (Time)** | Contínua | Período de acompanhamento/seguimento médico (dias) |
| **DEATH_EVENT** | Booleana | **Variável Alvo:** Se o paciente faleceu durante o período (0: Não, 1: Sim) |

### Citação:
* **Heart Failure Clinical Records [Dataset]. (2020). UCI Machine Learning Repository. https://doi.org/10.24432/C5Z89R.*
