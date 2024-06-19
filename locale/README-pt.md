# Padrão README multilíngue
[![en](https://img.shields.io/badge/lang-en-red.svg)](https://github.com/jonatasemidio/multilanguage-readme-pattern/blob/master/README.md)
[![pt-br](https://img.shields.io/badge/lang-pt--br-green.svg)](https://github.com/jonatasemidio/multilanguage-readme-pattern/blob/master/README.pt-br.md)
[![en](https://img.shields.io/badge/lang-es-yellow.svg)](https://github.com/jonatasemidio/multilanguage-readme-pattern/blob/master/README.es.md)

## Proposta de um sistema baseado em computação flexível para análise de acidentes automobilísticos
## 1. Introdução
O sistema proposto visa analisar acidentes de carro em Madri, Espanha, de 2019 a 2023. Usando técnicas de soft computing, o sistema permitirá a identificação de padrões e fatores que contribuem para os acidentes, facilitando a tomada de decisões e a implementação de medidas de segurança.
## 2. Seleção de variáveis
O modelo é baseado em um período específico; para usar outros anos, pesquise os conjuntos de dados em: https://datos.madrid.es/portal/site/egob/menuitem.c05c1f754a33a9fbe4b2e4b284f1a5a0/?vgnextoid=7c2843010d9c3610VgnVCM2000001f4a900aRCRD&vgnextchannel=374512b9ace9f310VgnVCM100000171f5a0aRCRD&vgnextfmt=default
Variáveis de entrada :

- data : Data do acidente
- hora : Hora do acidente
- location : Local do acidente
- district_code : Código do distrito
- district : Distrito
- type_accident : Tipo de acidente \
- weather_status : Condições meteorológicas \
- type_vehicle : Tipo de veículo \
- type_person : Tipo de pessoa \
- age_range : Faixa etária
- coordenada_x_utm : Coordenada X em UTM \
- coordenada_y_utm : Coordenada Y em UTM \
- positive_alcohol : Resultado positivo para álcool : Resultado positivo para álcool \
- positive_drug : Resultado positivo para drogas \
Variáveis de saída : \
- Probabilidade de acidente : Estimativa da probabilidade de ocorrência de um acidente em um local específico, considerando as variáveis de entrada. \
- Hotspots de acidentes: identificação de áreas com maior probabilidade de acidentes, com base na probabilidade de acidentes calculada. \
## 3. Construção do modelo de análise
O sistema usa um modelo de árvore de decisão para analisar os dados de acidentes. Esse algoritmo é adequado para identificar padrões e fatores contribuintes em acidentes de trânsito, pois é fácil de interpretar e pode lidar com variáveis categóricas e contínuas.
### Implementação do modelo
O modelo de árvore de decisão é implementado usando bibliotecas Python, como Scikit-learn, que facilita a criação e a avaliação de modelos de árvore de decisão.
### 3.2. Esboço do processo de análise
O processo de análise é dividido nas seguintes etapas:
1. coleta e preparação de dados: os dados de acidentes são obtidos de fontes como a Dirección General de Tráfico (DGT) ou o Instituto Nacional de Estadística (INE).
2.	Limpeza e pré-processamento: os dados são limpos e pré-processados para eliminar valores ausentes, converter variáveis categóricas em numéricas e normalizar os dados.
3.	Treinamento do modelo: o modelo de árvore de decisão é treinado com os dados pré-processados.
4.	Avaliação do modelo: o desempenho do modelo é avaliado usando métricas como precisão, integridade e pontuação F1.
5.	Previsão: o modelo treinado é usado para prever a probabilidade de acidentes e os pontos críticos de acidentes.
### 3.3 Resultados e análise
O sistema gera dois tipos de resultados: \
- Mapa de probabilidade de acidentes: Esse mapa mostra a probabilidade de acidentes em diferentes áreas de Madri, visualizando as áreas de maior risco. \
- Mapa de pontos críticos: esse mapa identifica as áreas com a maior concentração de acidentes, permitindo que as autoridades tomem medidas para melhorar a segurança viária.
## Exemplos de aplicação
### 4.1. Exemplo prático
O sistema é aplicado a dados de acidentes de carro em Madri, Espanha, de 2019 a 2023. É usado um conjunto de dados de acidentes reais, incluindo informações sobre data, hora, local, tipo de acidente, condições climáticas, tipo de veículo e tipo de pessoa envolvida.
### 4.2 Visualização dos resultados
![Esta imagem mostra os acidentes previstos por zona] (https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/2c7103bf227e00fe7e68e58e39f89864ec0901bc/Transporte%2C%20Localizaci%C3%B3n%20y%20Patrullaje/Figuras/Imagen3.png) 

1717399581495
Esta imagem mostra os acidentes previstos por zona. Como o algoritmo faz a previsão por coordenadas, optou-se por exibi-las em pontos que reúnem os possíveis acidentes ao redor delas.
 Esta imagem mostra os recursos previstos por zona](https://github.com/EdgarJP006/Accidentes-de-Trafico-de-Madrid/blob/2c7103bf227e00fe7e68e58e39f89864ec0901bc/Transporte%2C%20Localizaci%C3%B3n%20y%20Patrullaje/Figuras/Imagen5.png) 
 
1717399594301

O aplicativo também permite aumentar e diminuir o zoom para mostrar mais detalhes sobre os locais mais prováveis onde podem ocorrer acidentes de carro. Isso poderia ajudar a mapear rotas mais seguras para as pessoas, especialmente para turistas que podem estar menos familiarizados com os movimentos das ruas de Madri.
## 5. Conclusão
Desenvolvemos um sistema completo para a análise de acidentes de carro em Madri, na Espanha, usando soft computing. O sistema inclui a implementação de um modelo de árvore de decisão, limpeza e preparação de dados e o desenvolvimento de uma interface da Web para a apresentação dos resultados.
## Limitações do estudo
O estudo tem algumas limitações: \
- Disponibilidade de dados: a qualidade e a quantidade de dados disponíveis podem afetar a precisão do modelo. \
- Generalização: o modelo pode não ser generalizável para outras cidades ou regiões com características diferentes. \
- Fatores não considerados: o modelo não considera todos os fatores que podem contribuir para os acidentes, como a fadiga do motorista ou as condições do veículo.
## 7. propostas para trabalhos futuros
- Expandir o conjunto de dados: incluir mais dados de acidentes de diferentes cidades ou regiões para melhorar a generalização do modelo.
- Incorporar novos fatores: considerar fatores adicionais que possam influenciar a probabilidade de acidentes, como a condição do veículo ou a fadiga do motorista.
- Desenvolver um sistema de alerta: implemente um sistema de alerta que notifique os usuários sobre áreas de maior risco de acidentes.
