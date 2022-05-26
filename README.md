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

### Utilização dos diferentes tipos de bicicletas ao longo dos meses

![types_months](https://user-images.githubusercontent.com/88217999/170534010-a0c9c612-63b7-4021-8be2-754697fd22b8.png)

Há uma forte variação sazonal no uso das bicicletas. Como esperado, o uso das bicicletas tem forte queda nos meses de inverno no emisfério norte. 

Um outro ponto interessante é que a queda relativa é menor para as bicicletas elétricas. Nos meses de janeiro e fevereiro o número de auéis dessas bicicletas parece bastante próximo das bicicletas clássicas, enquanto que nos meses de verão as clássicas representam uma fração consideravelmente maior. 

### Utilização das bicicletas de acordo com o dia da semana

![week_days](https://user-images.githubusercontent.com/88217999/170535355-f0fcaa3b-812b-4ad5-96e5-a7fb811e9f44.png)

Para todos os tipos o dia da semana com o maior número de compartilhamentos é sábado. Porém, essa variação é bem suave para as bicicletas elétricas e um pouco mais acentuada para as clássicas e ancoradas. 

### Utilização por usuários casuais e membros

![membros_casual](https://user-images.githubusercontent.com/88217999/170536202-a26ceafe-2c48-4300-8945-5a8a72dbe07e.png)

As bicicletas ancoradas são utilizadas somente por usuários casuais. A quantidade de compartilhamentos por membros das bicicletas clássicas e elétricas é maior do que a de usuários casuais, porém, os dados indicam que o sistema é amplamente utilizado por não membros.

### Durações dos compartilhamentos

#### Distribuição com todos os tipos de bicicletas agregados 

![duracao_agregado](https://user-images.githubusercontent.com/88217999/170541733-90320d32-6e34-45d1-984c-9f3e33f0131a.png)

A distribuição é assimétrica à direita. A maioria dos compartilhamentos tem breve duração mas há vários registros de compartilhamentos mais longos.

O tempo médio de compartilhamento é 21.54 minutos e a mediana é 11.72 minutos.

#### Distribuições para cada tipo de bicicleta

![duracao_nao_agregado](https://user-images.githubusercontent.com/88217999/170542548-85ea13c7-868e-4278-a2cf-bc9e2611d276.png)

Há uma marcante diferença nos tempos de uso das bicicletas ancoradas. As bicicletas clássicas e elétricas apresentam distribuições semelhantes com médias e medianas relativamente próximas entre si mas muito menores do que a média e mediana das bicicletas ancoradas.

#### Variação da média e mediana com os tipos de bicicletas agregados

![media_mediana_agregado](https://user-images.githubusercontent.com/88217999/170544335-493ca201-5e54-41b6-9826-7d5e44a78508.png)

Assim como o número de compartilhamentos varia com os meses do ano, também observa-se variação na duração dos compartilhamentos. A duração média dos compartilhamentos é mais de 10 minutos mais curta no inverno do que no verão. A mediana também tem valor reduzido no inverno.

#### Variação da média e mediana para cada tipo de bicicleta

![media_mediana_nao_agregado](https://user-images.githubusercontent.com/88217999/170545060-a12925fa-dc28-4489-922a-a9ec8fd953ea.png)

O comportamento da média das bicicletas ancoradas não segue o comportamento geral visto. Existe um pico bastante acentuado em janeiro, provavelmente ocasionado por poucos compartilhamentos com longa duração. A mediana das bicicletas ancoradas tem um comportamento mais regular com maiores valores no verão e valores menores no inverno, assim como os outros tipos.

### Uso das estações

![estacoes_inicio](https://user-images.githubusercontent.com/88217999/170546043-04a8b2df-318e-4e70-b087-b54bdc5a73c7.png)

A estação "Streeter Dr & Grand Ave" é de longe a estação com o maior número de partidas. 

![estacoes_fim](https://user-images.githubusercontent.com/88217999/170546394-69b85968-2a7f-4069-b170-9b059b88d1b5.png)

![trajetos](https://user-images.githubusercontent.com/88217999/170546985-e752d75a-8924-4f85-8e8e-a67d5d0d26e4.png)
