# Spaceship_Titanic_Kaggle

## **Introdução**

Bem-vindo ao ano de 2912, onde suas habilidades em ciência de dados são necessárias para resolver um mistério cósmico. Recebemos uma transmissão de quatro anos-luz de distância e as coisas não estão parecendo boas.

A nave espacial Titanic era um transatlântico interestelar de passageiros lançado há um mês. Com quase 13.000 passageiros a bordo, a nave partiu em sua viagem inaugural transportando emigrantes do nosso sistema solar para três exoplanetas recém-habitáveis em órbita de estrelas próximas.

Ao contornar Alpha Centauri a caminho de seu primeiro destino - o tórrido 55 Cancri E - a incauta nave espacial Titanic colidiu com uma anomalia do espaço-tempo escondida em uma nuvem de poeira. Infelizmente, ela teve um destino semelhante ao de sua homônima de 1000 anos antes. Embora a nave tenha permanecido intacta, quase metade dos passageiros foi transportada para uma dimensão alternativa!

Para ajudar as equipes de resgate e recuperar os passageiros perdidos, você é desafiado a prever quais passageiros foram transportados pela anomalia usando registros recuperados do sistema de computador danificado da nave espacial.

Ajude a salvá-los e mude a história!

## **Entendimento dos dados**

**Descrições de arquivos e campos de dados**

train.csv - Registros pessoais de cerca de dois terços (~8700) dos passageiros, a serem usados como dados de treinamento.
PassengerId - Um ID exclusivo para cada passageiro. Cada Id tem o formato gggg_pp, em que gggg indica o grupo com o qual o passageiro está viajando e pp é o seu número dentro do grupo. As pessoas em um grupo geralmente são membros da família, mas nem sempre.
HomePlanet - O planeta de onde o passageiro partiu, normalmente seu planeta de residência permanente.
CryoSleep - Indica se o passageiro escolheu ser colocado em animação suspensa durante a viagem. Os passageiros em sono criogênico ficam confinados em suas cabines.
Cabin (Cabine) - O número da cabine onde o passageiro está hospedado. Tem o formato deck/num/lado, onde o lado pode ser P para bombordo ou S para estibordo.
Destino - O planeta em que o passageiro desembarcará.
Idade - A idade do passageiro.
VIP - Se o passageiro pagou por um serviço VIP especial durante a viagem.
RoomService, FoodCourt, ShoppingMall, Spa, VRDeck - Valor que o passageiro cobrou em cada uma das muitas comodidades de luxo da Spaceship Titanic.
Name (Nome) - O primeiro e o último nome do passageiro.
Transported - Se o passageiro foi transportado para outra dimensão. Esse é o alvo, a coluna que você está tentando prever.

test.csv - Registros pessoais para o terço restante (~4300) dos passageiros, a serem usados como dados de teste. 
Sua tarefa é prever o valor de Transported para os passageiros desse conjunto.

sample_submission.csv - Um arquivo de envio no formato correto.
PassengerId - Id de cada passageiro no conjunto de teste.
Transported - O alvo. Para cada passageiro, preveja True (verdadeiro) ou False (falso).


## **Preparação dos Dados**

- Gerar Metadados dos dados
- Corrigir os tipos e valores das colunas
- Tratamento de missing (nulos)
- Aplicar padronização nas variáveis numéricas.
- Aplicar OneHotEncoder e LabelEncoder nas variáveis categóricas
- Gerar artefatos para implantação do data prep realizado <br><br>

## **Feature Selection**

- Realizar a seleção das variáveis mais importantes utilizando o RandomForestClassifier
- Gerar artefatos para implantação do feature selection realizado
- Salvar as tabelas abts para utilizar na modelagem <br><br>

## **Modelagem**

- Treinar diferentes tipos de modelo
- Alterar os hiperparâmetros dos modelos
- Retreinar os modelos com hiperparâmetros diferentes
- Realizar stacking de modelos para tentar obter um melhor resultado
- Escolher o que obteve a maior acurácia para a escoragem

## **Escoragem**

- Aplicar todo o tratamento de Preparação dos Dados e Feature Selection nas tabelas de treino e teste
- Carregar o modelo que apresentou o melhor desempenho na modelagem
- Escorar as bases de treino e teste
- Entender em qual modelo os dados devem ser submetidos no Kaggle
- Submeter os dados no Kaggle


## **Resultado Kaggle**

- Acurácia (Leaderboard): 0.79401
<br><br>

**Aprendizados e reflexões para as próximas versões:**

- Modelos simples, bem ajustados e com bons dados, superaram abordagens mais complexas com menos tratamento.

- A engenharia de features vai ser o diferencial para melhorar a performance e alcançar melhores resultados.

- Um stacking utilizando redes neurais + LightGBM provavelmente conseguirá obter um resultando melhor do que os modelos utilizados nesse projeto.
