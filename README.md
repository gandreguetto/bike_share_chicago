# Compartilhamento de bicicletas na cidade de Chicago - Estados Unidos

## Introdução

#### Sobre os dados

Nesse projeto, dados do sistema de compartilhamento de bicicletas da cidade de Chicago são analisados. Os dados foram obtidos do Kaggle (https://www.kaggle.com/datasets/evangower/cyclistic-bike-share) e também são utilizados como um caso de estudo do curso Google Data Analytics do Coursera.

#### O período de coleta

Os dados contém informações sobre o uso do sistema no período de um ano, entre os meses de Abril de 2021 à março de 2022. 

#### Os tipos de bicicleta

Três diferentes tipos de bicleta são descriminados nos dados, em inglês: "Classic", "Docked" e "Electric". Aqui eles serão designados em português como: Clássica, Ancorada e Elétrica.

Não há informações detalhadas sobre o funcionamento do sistema mas supõe-se que as bicicletas "clássicas" sejam bicicletas que não ficam ancoradas a uma estação, diferentemente das "ancoradas".   

#### Localizações 

Há informações sobre as coordenadas de início e fim do uso das bicicletas e também o nome das estações correspondentes. Porém, existem dados com as coordenadas dos locais mas sem o nome das estações. Não está claro se os dados com os nomes das estações faltantes referem-se a ínicio ou fim de compartilhamento que ocorrem fora das estações ou se é algum outro fator.     

De qualquer forma, a maior parte dos dados (mais de 86%) apresenta informação completa sobre a localização. Isso também indica que mesmo para as bicicletas "clássicas" e "elétricas" as estações são amplamente utilizadas. Talvez exista uma exigência, que não está clara olhando apenas para os dados, de que as bicicletas sempre fiquem nas estações após o uso ou ainda as pessoas podem preferir utilizar as estações por outros motivos, como por exemplo realizar o pagamento em máquinas de cobrança.

As análises que envolvem localização serão focadas nos compartilhamentos que contém os nomes das estações.

#### Usuários casuais e membros

Por fim, os dados discriminam se um usuário é casual ou membro. Novamente, não há detalhamento sobre a diferença entre essas classes.

#### Análises e Insights

A seguir, uma análise detalhada desses dados é realizada.  Em especial, será explorado como a utilização das bicicletas varia ao longo do ano, como se comporta a distribuição dos tempos de utilização nos dados e quais são as estações mais utilizadas.

Os resultados obtidos nas análises realizadas fornecem uma riquíssima fonte de informações úteis para serem aplicadas na administração do sistema. Por exemplo, a variação no uso ao longo do ano indica a melhor época do ano para realizar manutenções nas bicicletas. A distribuição do tempo de uso, por outro lado, pode ser utilizada na precificação dos serviços. Também, as informações sobre a utilização das diferentes estações pode auxiliar na distribuição e relocação das bicicletas.

## Os arquivos do repositório

Têm-se dois python notebooks no repositório. O arquivo "mapa.ipynb" contém as análises que permitem visualizar sobre o mapa da cidade as estações e o volume de uso de cada. O arquivo "shared_bikes.ipynb" contém todas as demais análises. 

## Principais resultados das análises

Têm-se dois python notebooks no repositório. O arquivo "mapa.ipynb" contém as análises que permitem visualizar sobre o mapa da cidade as estações e o volume de uso de cada. O arquivo "shared_bikes.ipynb" contém todas as demais análises. 

## Utilização dos diferentes tipos de bicicletas ao longo dos meses

