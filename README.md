# Blood Donation Prediction

Este repositório contém um projeto de Machine Learning para prever se um doador fará uma nova doação de sangue. O modelo foi construído utilizando Random Forest com dados do *Blood Transfusion Service Center Dataset*.

## Estrutura do Repositório

- `data/`: Base de dados utilizada no projeto.
- `models/` : Modelo gerados na construção do projeto
- `notebooks/`:  Notebook com a análise e implementação do modelo.
- `results/`: Resultados gerados pelo modelo (métricas e visualizações).
- `requirements.txt`: Lista de dependências do projeto.

## Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/SadPineapple/blood-donation-prediction.git

# Previsão de Doações de Sangue com Machine Learning
## Dificuldade: Iniciante

## Introdução
A doação de sangue é essencial para salvar vidas, mas os bancos de sangue enfrentam dificuldades em prever o comportamento de doadores. Este projeto utiliza machine learning para criar um modelo preditivo, ajudando a identificar padrões que indicam a probabilidade de um indivíduo doar sangue novamente.

## Metodologia
O modelo desenvolvido foi baseado no algoritmo Random Forest, que utiliza um conjunto de árvores de decisão para melhorar a precisão e evitar overfitting. O conjunto de dados utilizado foi o Blood Transfusion Service Center Dataset, que contém as seguintes variáveis:

Recency: Tempo desde a última doação (meses).
Frequency: Número total de doações realizadas.
Monetary: Volume total de sangue doado (em centilitros).
Time: Tempo desde a primeira doação (meses).
Target: Variável-alvo (1 para doadores, 0 para não doadores).

# Etapas de Desenvolvimento:

## Pré-processamento dos Dados:

Normalização das variáveis explicativas para uniformizar as escalas.
Divisão dos dados em 70% para treino e 30% para teste.
Treinamento do Modelo:

Algoritmo: Random Forest Classifier com parâmetros padrão.
Métrica principal: Acurácia.

## Avaliação:

Métricas utilizadas: Acurácia, precisão, recall e matriz de confusão.

## Resultados

### Desempenho do Modelo:
Acurácia Geral: 74,2%.

### Métricas detalhadas:
### Classe "0" (Não doou):
Precisão: 78%.
Recall: 91%.
F1-Score: 84%.

### Classe "1" (Doou):
Precisão: 53%.
Recall: 28%.
F1-Score: 37%.

### Matriz de Confusão:
Classe Real	Previsto: Não	Previsto: Sim
Não	150	15
Sim	43	17

## Análise:
O modelo tem um bom desempenho em identificar não doadores (classe majoritária).
Contudo, apresenta dificuldade em prever corretamente os doadores (classe minoritária), devido ao desbalanceamento dos dados.

## Dificuldades encontradas
Durante o desenvolvimento do projeto de previsão de doações de sangue, enfrentamos desafios relacionados ao desbalanceamento da variável-alvo, o que afetou a capacidade do modelo de identificar corretamente os doadores. Apesar de utilizar técnicas como SMOTE para balanceamento e o ajuste de hiperparâmetros, o modelo ainda apresentou baixa precisão e recall na classe minoritária. Além disso, o modelo de Random Forest demonstrou tendência ao overfitting, o que exigiu o uso de validação cruzada para melhorar sua generalização. A interpretação dos resultados também foi um desafio, mas foi superada com o uso de visualizações claras, como a matriz de confusão, para facilitar a comunicação dos resultados.

## Conclusão
O modelo Random Forest apresentou desempenho satisfatório na identificação de não doadores, mas a baixa precisão e recall para doadores indica a necessidade de balanceamento de classes ou ajuste de hiperparâmetros. Esse projeto demonstra como o aprendizado de máquina pode ser aplicado para resolver desafios em bancos de sangue, mas melhorias futuras são essenciais para obter resultados mais equilibrados.
