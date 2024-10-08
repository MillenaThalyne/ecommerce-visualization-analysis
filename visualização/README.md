# Visualização e Dados 📊
- Para essa última etapa do projeto, criei algumas visualizações interessantes para nossos dados: 
  - **Gráfico de Dispersão**: Nota x Desconto e Preço
  - **Mapa de Calor**: Correlação entre variáveis numéricas
  - **Mapa de Barras**: Produtos por Gênero 
  - **Mapa de Pizza**: Produtos por Temporada
  - **Mapa de Densidade**: Densidade de Desconto

_OBS: Qualquer sugestão para melhoria de qualquer parte desse projeto, pode entrar em contato comigo pelo LinkedIn ou email (link no perfil)._

# Bibliotecas Utilizadas 📋
> Pandas <br>
> Matplotlib <br>
> Seaborn <br>

# Visualizações 📊
- Nota x Desconto e Preço
- A partir desse gráfico, podemos notar que a concentração das avaliações estão entre as notas de 5.0 e 4.0. Essas notas são de compras que quase não tiveram desconto e, também, são produtos com preços mais elevados.
- Com isso, observamos que ter ou não desconto não é um fator muito relevante para a qualidade das avaliações (mesmo que alguns produtos tenham algum desconto). Também é possível notar que quanto maior o preço do produto, maior a possibilidade dele ter uma avaliação condizente, pois apresenta maior concentração na área esquerda superior. <br>

[![Gráfico](https://img.shields.io/badge/Visualizar_Gráfico-yellow?style=flat&logo=bar-chart&logoColor=blue)](https://github.com/MillenaThalyne/ecommerce-visualization-analysis/blob/main/visualiza%C3%A7%C3%A3o/Nota%20x%20Desconto%20e%20Pre%C3%A7o.png)

## Mapa de Calor

- Correlação entre variáveis numéricas
  - A partir desse gráfico, é possível notar a correlação das seguintes variáveis:
    - Qtd_Vendidos x N_Avaliações: Com uma correlação alta, podemos perceber que o número de avaliações está diretamente ligado com a quantidade de produtos vendidos. Ou seja, quanto mais produtos forem vendidos naquele anúncio, a tendência é que haja mais avaliações também;
    - Desconto x N_Avaliações: Mesmo não sendo uma correlação tão forte quanto a primeira, essa correlação existe. Podemos verificar que se o produto possui algum desconto, isso impacta no número de avaliações;
    - Qtd_Vendidos x Desconto: Também é uma correlação baixa, porém existente. É possível perceber que se um produto possui desconto, sua quantidade vendida também tende a ser maior;
    - Marca_Freq x Temporada_Cod: A frequência da marca tem correlação com o código da temporada, mesmo que levemente. A tendência é que a frequência da marca vai ser um pouco relativa a temporada que esta se encontra.

## Mapa de Barras

- Produtos por Gênero
    - Neste gráfico, é possível notar que a concentração de produtos são dos gêneros: Feminino, Masculino, Bebês, Sem Gênero, Meninas, Meninos e Sem Gênero Infantil; nesta ordem. As demais categorias são bem inferiores as demais e chegam bem próximas da linha 0.

## Mapa de Pizza

- Produtos por Temporada
    - Neste gráfico, é possível notar que a concentração de produtos são das temporadas: Primavera/Verão, Outono/Inverno e Primavera/Verão e Outono/Inverno, nessa ordem;
    - OBS: As categorias precisavam ser tratadas, pois havia diferenças em um mesmo dado, que foram substituídas por “Primavera/Verão e Outono/Inverno”.

## Mapa de Densidade

- Gráfico de Densidade - Desconto
    - Nesse gráfico, é possível notar que maioria dos produtos não possuem desconto, fazendo um pico bem alto no 0. A segunda concentração de descontos está em 10%, diminuindo ainda mais a partir dos 20% até 30% para, depois, existir pouquíssimos produtos com desconto entre 40-70%;
    - Isso nos mostra que realmente existem diversos produtos que não possuem desconto, ou seu desconto está concentrado nos 10-20%.
