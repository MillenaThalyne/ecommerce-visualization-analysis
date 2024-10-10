# E-commerce Assessments Analysis Project
## Sobre o Projeto 
> Autoria: Millena Thalyne

> Linguagem: Python

> *Desafio disponibilizado pela EBAC na Profissão Cientista de Dados*

Esse projeto tem como objetivo realizar diversos tratamentos em uma base de dados de avaliações de produtos do setor de E-commerce para, ao final, criar visualizações pertinentes a fim de coletar informações relevantes. <br>
Para replicar esse projeto perfeitamente, basta utilizar o arquivo de requirements disponibilizado neste repositório! 🌟

## Base de Dados

Os dados utilizados nesse projeto são avaliações de clientes para produtos E-commerce e, dentre as variáveis presentes nessa base, é disponibilizado as seguintes:
- **'Título'**: Título da Avaliação,
- '**Nota**': Nota da Avaliação,
- '**N_Avaliações**': Número de Avaliações,
- '**Desconto**': Desconto aplicado ao produtos referente àquela avaliação,
- '**Marca**': Marca do produto daquela avaliação,
- '**Material**': Material do produto daquela avaliação,
- '**Gênero**': Gênero do produto daquela avaliação,
- '**Temporada**': Temporada do produto daquela avaliação,
- '**Review1**': Avaliação 1,
- '**Review2**': Avaliação 2,
- '**Review3**': Avaliação 3,
- '**Qtd_Vendidos**': Quantidade de produtos vendidos naquela avaliação,
- '**Preço**': Preço do produto daquela avaliação,
- '**Marca_Cod**': Código da marca do produto em avaliação,
- '**Material_Cod**': Código do Material do produto em avaliação,
- '**Temporada_Cod**': Código de temporada do produto em avaliação.

[![Gráfico](https://img.shields.io/badge/Dados-pink?style=flat&logo=bar-chart&logoColor=pink)](https://github.com/MillenaThalyne/ecommerce-visualization-analysis/tree/main/dados)

## Construção

### Tratamento

Os tratamentos utilizados nesses dados foram:
- **Remoção de colunas defeituosas ou não utilizadas**;
- **Tratamento de tipos**;
- **Tratamento de nulos**;
- **Tratamento de duplicados**.

[![Gráfico](https://img.shields.io/badge/Mais_Informações-blue?style=flat&logo=bar-chart&logoColor=blue)](https://github.com/MillenaThalyne/ecommerce-visualization-analysis/tree/main/tratamento)

### Preparação

Na parte de preparação de dados, é realizado a normalização e padronização dos dados, além de utilizar de Engenharia de Feature para obter novas variáveis pertinentes:
- **MinMaxScaler**: Criação de novas variáveis com a escala das variáveis Nota, N_Avaliações, Desconto e Preço, padronizada;
- **Frequência**: Criação de variável que obtém a frequência de Material.

[![Gráfico](https://img.shields.io/badge/Mais_Informações-blue?style=flat&logo=bar-chart&logoColor=blue)](https://github.com/MillenaThalyne/ecommerce-visualization-analysis/tree/main/prepara%C3%A7%C3%A3o)

### Visualização

Agora, na parte de visualização de dados, foi criado cinco visualizações bem interessantes para os dados:
- **Gráfico de Dispersão**: Nota x Desconto e Preço
- **Mapa de Calor**: Correlação entre variáveis numéricas
- **Mapa de Barras**: Produtos por Gênero
- **Mapa de Pizza**: Produtos por Temporada
- **Mapa de Densidade**: Densidade de Desconto
 
[![Gráfico](https://img.shields.io/badge/Mais_Informações-blue?style=flat&logo=bar-chart&logoColor=blue)](https://github.com/MillenaThalyne/ecommerce-visualization-analysis/blob/main/visualiza%C3%A7%C3%A3o/README.md)

## Insights

📈 A concentração das avaliações estão entre as notas de 5.0 e 4.0. Essas notas são de compras que quase não tiveram desconto e, também, são produtos com preços mais elevados;

⭐ Existe correlação muito forte entre as variáveis: 'Qtd_Vendidos x N_Avaliações', 'Desconto x N_Avaliações', 'Qtd_Vendidos x Desconto' e 'Marca_Freq x Temporada_Cod';

👨‍👩‍👧‍👦 A concentração de produtos são dos gêneros: Feminino, Masculino, Bebês, Sem Gênero, Meninas, Meninos e Sem Gênero Infantil; nesta ordem;

☀️ A concentração de produtos são das temporadas: Primavera/Verão e Outono/Inverno;

💸 Maioria dos produtos não possuem desconto!

## Conclusão 
Esse projeto foi bem interessante de ser realizado e me ajudou bastante a pôr em prática os ensinamentos do curso. Dessa forma, agradeço aos que se dispuseram a ver meu projeto e agradeço qualquer melhoria ou avaliação que puderem me fazer!  
