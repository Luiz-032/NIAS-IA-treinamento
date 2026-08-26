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
    1. Descarte das colunas 'Cabin', 'Ticket' e 'Name' (excesso de nulos ou sem uso direto)
    2. Imputação de valores ausentes em 'Age', 'Fare' e 'Embarked' via pipelines, testando estratégias de média, mediana, zero e moda
    3. Encoding das variáveis categóricas 'Sex' e 'Embarked' com OneHotEncoder e LabelEncoder, comparando one-hot vs ordinal
    4. Criação de variáveis derivadas com pd.cut (AgeGroup) e pd.qcut (FareGroup)
    5. Validação cruzada para comparar Random Forest e Gradient Boosting e escolher o modelo final
- Créditos: @victortdsferreira
