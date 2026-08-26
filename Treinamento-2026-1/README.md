# NIAS-IA
## Treinamento 2026-1

### Formas de iteração com o repositório:
1. Clone o repositório em sua máquina. 
2. Edite e salve o notebook que você vai apresentar na entrevista do Processo Seletivo.
3. Faça uma seção neste README.md como o exemplo abaixo.
4. Não retire as instruções do README.md

#### Rodolpho Neves
- Problema escolhido: Titanic - Machine Learning from Disaster
- O que precisa ser resolvido: Predizer se uma determinada pessoa sobrevive ou não ao acidente do Titanic
- Melhor resultado obtido na submissão: 75% de acurácia
- Técnicas utilizadas para resolver o problema: 
    1. Descarte das colunas 'sibsp', 'parch', 'ticket' e 'cabin'
    2. Imputação de dados de média na coluna 'Age'
    3. Padronização da coluna 'fare'
    4. Transformação dos dados da coluna 'embarked' em valores numéricos ordinais
- Créditos: @rodolpho-neves

#### Victor Ferreira
- Problema escolhido: Titanic - Machine Learing from disaster
- O que precisa ser resolvido: Predizer se um determinado passageiro sobrevive ou não ao acidente do Titanic
- Melhor resultado obtido na submissão: 76,5% de acurácia
- Técnicas utilizadas para resolver o problema:
    1. Feature Selection com Mutual Information Score (`mutual_info_classif`) para medir a relevância de cada variável em relação a 'Survived'
    2. Feature Construction: extração do título social ('Title') a partir do campo 'Name', criação de 'FamilySize' (soma de 'SibSp' + 'Parch') e 'IsAlone'
    3. Feature Extraction com K-means (6 clusters em 'Age'/'Fare', com remoção de outliers) para gerar uma nova variável de agrupamento
    4. Feature Extraction com PCA (após normalização com MinMaxScaler) reduzindo 'Age' e 'Fare' a um componente principal
    5. Target Encoding da feature 'Title' com MEstimateEncoder, suavizando a média por categoria para evitar vazamento de dados
- Créditos: @leoscelestee-coder

#### Gustavo Silva Pereira
- Problema escolhido: Análise Exploratória Global de Dados da COVID-19
- O que precisa ser resolvido: Analisar a evolução temporal de mortes por regiões da OMS, calcular taxas proporcionais de mortalidade e verificar a correlação entre o tamanho da população e o impacto da doença.
- Principais resultados obtidos: Constatação de que as Américas lideraram o acumulado de mortes no período e comprovação estatística (via matriz de correlação) de que a população total de um país não afeta a sua taxa de mortes por milhão.
- Técnicas utilizadas para resolver o problema:
	1. Conversão da coluna de datas de string para o formato datetime
	2. Agrupamento de dados (groupby) para sumarizar as informações por região da OMS
	3. Cruzamento de tabelas (merge) para unificar o dataset da doença com os dados de população mundial
	4. Construção de gráficos de linhas, dispersão e mapa de calor para correlação de Pearson
Créditos: @elgusta

    1. Descarte das colunas 'Cabin', 'Ticket' e 'Name' (excesso de nulos ou sem uso direto)
    2. Imputação de valores ausentes em 'Age', 'Fare' e 'Embarked' via pipelines, testando estratégias de média, mediana, zero e moda
    3. Encoding das variáveis categóricas 'Sex' e 'Embarked' com OneHotEncoder e LabelEncoder, comparando one-hot vs ordinal
    4. Criação de variáveis derivadas com pd.cut (AgeGroup) e pd.qcut (FareGroup)
    5. Validação cruzada para comparar Random Forest e Gradient Boosting e escolher o modelo final
- Créditos: @victortdsferreira
