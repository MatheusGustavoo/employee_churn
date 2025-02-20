# Predição de Churn de Funcionários

## Introdução
A retenção de talentos é um dos maiores desafios para empresas de tecnologia, principalmente diante da crescente concorrência do mercado. Este projeto visa desenvolver um modelo preditivo para identificar a probabilidade de churn de funcionários e entender os principais fatores que influenciam essa decisão.

## Objetivo
Criar um modelo de aprendizado de máquina utilizando **Random Forest** para prever se um funcionário tem alta probabilidade de sair da empresa e identificar os principais fatores que contribuem para essa decisão.

## Tecnologias Utilizadas
- **Linguagem**: Python
- **Bibliotecas**: pandas, numpy, scikit-learn, plotly, SHAP, optuna
- **Técnicas**: Feature Engineering, Análise Exploratória de Dados (EDA), Random Forest, Validação Cruzada, Tuning de Hiperparâmetros, Interpretação de Modelos com SHAP

## Pipeline do Projeto
1. **Carga e Limpeza de Dados**
   - Carregamento do dataset `employee_churn.csv`
   - Conversão de colunas de datas
   - Remoção de colunas irrelevantes

2. **Análise Exploratória de Dados (EDA)**
   - Verificação de valores ausentes
   - Distribuição da variável target (Churn)
   - Análise de correlação entre variáveis
   - Testes estatísticos de dependência

3. **Feature Engineering**
   - Cálculo do tempo de empresa
   - Tempo desde o último feedback, aumento salarial e mudança de cargo
   - Codificação de variáveis categóricas e normalização de variáveis numéricas

4. **Treinamento do Modelo**
   - Separar os dados em conjunto de treino e teste (50/50)
   - Treinar um modelo baseline com Random Forest
   - Avaliação inicial: **Acurácia, F1-score, Matriz de Confusão, ROC AUC**

5. **Otimização do Modelo**
   - Validação cruzada com **Stratified KFold** (5 folds)
   - Busca de hiperparâmetros com **GridSearchCV**
   - Ajuste fino do threshold para maximizar recall

6. **Interpretação dos Resultados**
   - Importância das variáveis com Random Forest
   - Análise de SHAP Values para entender influência das features na decisão do modelo

## Principais Insights
- Tempo de empresa e tempo desde o último aumento salarial foram os fatores mais relevantes para previsão do churn.
- A probabilidade de churn é maior em funcionários que passaram longos períodos sem feedbacks.
- Ajustar o threshold do modelo permitiu priorizar a identificação de funcionários com maior risco de saída.

## Como Executar o Projeto
1. Clone o repositório:
   ```bash
   git clone https://github.com/MatheusGustavoo/employee_churn.git
   ```
2. Instale em seu ambiente virtual todas as depêndencias importadas no inicio do arqivo .ipynb.
   ```
3. Execute o nootebook.

## Conclusão
Este projeto demonstrou a eficácia do uso de aprendizado de máquina para prever churn de funcionários e identificar fatores-chave que podem ajudar a empresa a reter talentos. A análise de SHAP foi essencial para interpretar os resultados e criar possíveis estratégias para mitigar a saída de profissionais valiosos.

## Autor
[Matheus Pedra](https://www.linkedin.com/in/matheus-gustavo11)

