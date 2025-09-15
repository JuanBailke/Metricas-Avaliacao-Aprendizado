# Calculadora de Métricas para Modelos de Classificação

Este projeto em Python implementa o cálculo das principais métricas de avaliação para modelos de classificação de dados. A partir de vetores de dados reais e previstos, o script gera uma matriz de confusão e calcula as seguintes métricas de desempenho:

- Sensibilidade (Recall / Revocação)

- Especificidade (Specificity)

- Acurácia (Accuracy)

- Precisão (Precision)

- F-Score (F1-Score)

## Sobre o Projeto
Este repositório foi desenvolvido como parte do desafio de projeto do bootcamp BairesDev - Machine Learning Training da plataforma DIO (Digital Innovation One). O objetivo é demonstrar a compreensão e a aplicação prática das métricas fundamentais usadas para avaliar a performance de algoritmos de classificação.

Você pode encontrar o bootcamp no link:
[BairesDev - Machine Learning Training](https://web.dio.me/track/bairesdev-machine-learning-training)

## A Matriz de Confusão Utilizada
A base para todos os cálculos é a matriz de confusão, que compara os valores reais com os valores previstos pelo modelo. Para este projeto, foram utilizados os seguintes vetores de 50 posições, resultando na matriz abaixo:

|                    |Previsto: Negativo (0)|Previsto: Positivo (1)|
|--------------------|----------------------|----------------------|
| Real: Negativo (0) | VN = 12|FP = 6|
| Real: Positivo (1) | FN = 6|VP = 16|

Onde:

- **VP (Verdadeiros Positivos): 16**
- **VN (Verdadeiros Negativos): 12**
- **FP (Falsos Positivos): 6**
- **FN (Falsos Negativos): 6**

## Métricas Calculadas
Abaixo estão as fórmulas e definições de cada métrica implementada no código.

1. Acurácia (Accuracy)

Mede a proporção geral de previsões corretas em relação ao total de amostras.
```
(VP+VN) / VP+VN+FP+FN
```
2. Sensibilidade ou Recall (Revocação)

Mede a proporção de positivos reais que foram corretamente identificados pelo modelo. É crucial quando o custo de um Falso Negativo é alto.
```
VP / (VP+FN)
```
 
3. Especificidade (Specificity)

Mede a proporção de negativos reais que foram corretamente identificados pelo modelo.
```
VN / (VN+FP)
```
4. Precisão (Precision)

Mede a proporção de previsões positivas que estavam, de fato, corretas. É importante quando o custo de um Falso Positivo é alto.
```
VP / (VP + FP)
```
 
5. F-Score (F1-Score)

A média harmônica entre a Precisão e o Recall, oferecendo um balanço entre as duas métricas. É especialmente útil em cenários com classes desbalanceadas.

```
2 x (Precisão x Sensibilidade) / (Precisão + Sensibilidade)
```
 
### Como Executar
1. Clone este repositório:

```Bash
git clone https://github.com/JuanBailke/Metricas-Avaliacao-Aprendizado
cd Metricas-Avaliacao-Aprendizado
```
2. Crie um ambiente virtual (opcional, mas recomendado) e instale as dependências do projeto usando o arquivo requirements.txt:

```Bash
# Comando para instalar as bibliotecas
pip install -r requirements.txt
```

3. Inicie o Servidor Jupyter

```Bash
jupyter notebook
```

4. Abra e Execute o Notebook

- Após executar o comando acima, uma nova aba será aberta automaticamente no seu navegador padrão, mostrando os arquivos da pasta.
- Clique no arquivo do projeto com a extensão .ipynb (por exemplo, projeto_metricas.ipynb).
- Com o notebook aberto, você pode executar o código. Para rodar todas as células de uma vez e ver o resultado final, vá ao menu superior e clique em Cell > Run All.

### Alternativas de Execução
- Visual Studio Code: Se você utiliza o VS Code com a extensão oficial de Python da Microsoft, pode abrir o arquivo .ipynb diretamente no editor e executar as células sem precisar iniciar o servidor manualmente pelo terminal.
- Google Colab: Você também pode fazer o upload do arquivo .ipynb para o Google Colab e executá-lo na nuvem, sem a necessidade de instalar nada em sua máquina local.