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

#### João Victor de Freitas Lucas
- Problema escolhido: Titanic - Machine Learning from Disaster
- O que precisa ser resolvido: Predizer se uma determinada pessoa sobrevive ou não ao acidente do Titanic
- Melhor resultado obtido na submissão: 77,75% de acurácia
- Técnicas utilizadas para resolver o problema: 
    1. Comparação de diversos métodos e modelos
    2. Aplicação da estratégia ordinal encoder nas features catégoricas
    3. Imputação de dados nas colunas numéricas utilizando a estratégia most_frequent
- Créditos: @joaovictorfl18

#### Leonardo Celeste
- Problema escolhido: Titanic - Machine Learning from Disaster (Capítulo 9 - Feature Engineering)
- O que precisa ser resolvido: Transformar e enriquecer as variáveis brutas do dataset para que capturem melhor os padrões relacionados à sobrevivência dos passageiros, antes da etapa de modelagem
- Melhor resultado obtido na submissão: *
- Técnicas utilizadas para resolver o problema:
    1. Feature Selection com Mutual Information Score (`mutual_info_classif`) para medir a relevância de cada variável em relação a 'Survived'
    2. Feature Construction: extração do título social ('Title') a partir do campo 'Name', criação de 'FamilySize' (soma de 'SibSp' + 'Parch') e 'IsAlone'
    3. Feature Extraction com K-means (6 clusters em 'Age'/'Fare', com remoção de outliers) para gerar uma nova variável de agrupamento
    4. Feature Extraction com PCA (após normalização com MinMaxScaler) reduzindo 'Age' e 'Fare' a um componente principal
    5. Target Encoding da feature 'Title' com MEstimateEncoder, suavizando a média por categoria para evitar vazamento de dados
- Créditos: @rodolpho-neves