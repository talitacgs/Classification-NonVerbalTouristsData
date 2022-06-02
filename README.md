# Classification-NonVerbalTouristsData

## 1. Project Motivation 
 
Esse é o projeto final do Programa de Formação em Dados Lojas Renner S.A realizado com o apoio das Lojas Renner e a César School. O curso teve 84horas de duração com aulas sobre programação python, cultura DevOps, Design Thinking, Data Science e Machine Learning. Foram abordados algoritmos supervisionados e não supervisionados. O projeto final consiste no desenvolvimento de um algoritmo de classificação para análise de um dataset sobre o tipo de cliente.

## 2. Data 

O dataset possui informações de região, sexo, idade, se retornaria ou não ao estabelecimento/experiência, diversas colunas com classificação indiferente/gostou/não gostou e, por fim, a classificação do tipo ou classe do cliente.

## 3. Implementation

Na fase de tratamento dos dados foi necessário a substituição de caracter especial e transformação de valores categóricos em númericos. Através da função .describe observou-se que existia coluna com variância e média nula e, portanto, poderia ser excluída do modelo. Os dados foram separados em 75% treino e 25% teste. As variáveis foram padronizadas. Para para treinar o modelo k-NN, foi criado uma função que recebe o valor de k de fora iterativa, a função retorna o f1_score, pois é uma métrica que combina precisão e recall. Foi necessário definir o average, pois é um parâmetro obrigatório para targets multilabels, e, ao analisar o histograma, os dados estão desbalanceados, por isso foi utilizado average = weighted.

## 4. Result

Para k=3 o valor da acurácia é 0.789, porém o gráfico Error rate vs k value mostra que k=3 é uma região instável. Em k=5 obtem-se uma acurácia de 0.735. 

<div align="center">
<img src="https://user-images.githubusercontent.com/102559911/171673583-ff4739d1-8840-4354-ad3a-02ee61711034.PNG" width="500px" />
</div>

Entretanto o relatório de classificação apresenta um resultado importante para o modelo, os dados estão fortemente agrupados (support = 12) em uma única classe (2), retornando 0 para as outras métricas e classes. Um dos fatores para isso acontecer é baixa quantidade de dados no dataset.

<div align="center">
<img src="https://user-images.githubusercontent.com/102559911/171674389-512b23e0-579d-44f9-8d1a-53275c1b16c0.PNG" width="300px" />
</div>
