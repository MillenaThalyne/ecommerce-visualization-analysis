# Tratamento de Dados 🎲
- Para essa primeira etapa do projeto, irei realizar o tratamento dos dados focado em: Remoção de algumas colunas, tratamento de tipos, tratamento de nulos e
tratamento de duplicados. A seguir irei detalhar melhor as abordagens que tomei e o porquê delas;
- Qualquer sugestão para melhoria de qualquer parte desse projeto, pode entrar em contato comigo pelo LinkedIn ou email (link no perfil).
# Bibliotecas Utilizadas nessa Etapa 📋
> Pandas <br>
> Matplotlib <br>
> Seaborn
# Construção dos Tratamentos 🔧
## Remoção de Colunas
- Nessa parte do projeto, notei que existia uma coluna de índice desnecessária, pois o Pandas cria, assim que lê seus arquivos, uma coluna exatamente igual a essa;
- Também exclui as colunas do MinMaxScaler para poder refazê-las na etapa de preparação, pois, como irei fazer diversas alterações nas colunas originais, estas serão inviesadas;
- Por conta desse ponto, decidi por excluir essa coluna, que foi relacionada ao DataFrame ‘df_eco’ para distinção do original.
## Tratamento de Tipos
### Coluna 'Qtd_Vendidos'
- Minha ideia de tratamento para essa coluna foi transformar em inteiro para poder fazer análises futuras;
- Para isso, removi o '+', substitui 'mil' por '000' e 'Nenhum' por '0', para depois tranformá-los em inteiro; 
- Quando terminei meu trabalho, notei que já existia uma coluna com essas informações, a 'Qtd_Vendidos_Cod', porém com o tipo *float*. Dessa forma, decidi por excluir essa coluna lá cima também para deixar somente a que eu havia tratado.
## Tratamento de Nulos
- Logo de cara, vemos uma quantidade bem grande de dados nulos em diversas colunas, sendo sua maior quantidade presente no campo ‘Desconto’, com 1325 registros nulos;
- Como cada um dos elementos tem sua importância, não posso simplesmente excluir tudo. Por isso, farei o tratamento de acordo com o contexto do campo. Por exemplo, em Desconto, faria sentido que os dados nulos presentes nele seja porque não houve desconto. Nesse caso, se o tipo dele é float, seria interessante substituir os dados nulos por 0.0, o que caracterizaria uma não inclusão de desconto naquela compra;
- Cada campo terá seu tratamento específico, por isso, em cada etapa irei detalhar melhor a abordagem que tomei.
### Tratamento de 'Nota'
- Meu primeiro pensamento ao ver dados nulos em notas é que poderia ser 0, mas não, isso seria dizer que as pessoas não gostaram nem um pouco do produto e não sabemos nisso. Também pensei em preencher com a média, mas também seria impreciso, pois não temos como saber exatamente o porquê de não terem preenchido esse campo na hora da avaliação e, por isso, seria uma presunção;
-  Por isso, a abordagem que pensei nesse caso seria preencher esses registros nulos pela mediana deles, pois excluí-los reduziria drasticamente nossos dados. Então, como esses dados são importantes, utilizar a mediana deles para suprir essa falta seria uma abordagem interessante, uma vez que a quantidade de registros totais já é bastante pequena e ainda teremos diversos tratamentos posteriores que o reduzirão ainda mais.
### Tratamento de 'N_Avaliações'
- Nesse caso, eu posso crer que quando não temos número de avaliações, quer dizer que ela é igual a 0, ou seja, não tem avaliações desse produto;
- Então fica bem simples, pois pode-se somente substituir os valores nulos por 0 para informar isso.
### Tratamento de Desconto
- Como falei anteriormente, a ausência de registro nesse campo significaria que não houve desconto, ou seja, desconto = 0.
### Tratamento de 'Material'
- Antes de verificar qual a melhor abordagem para os registros nulos nesse campo, eu verifiquei do que ele se trata, sendo a categoria do material daquele produto. Com isso, acredito que a ausência de um material seria, então, desconhecido ou indeterminado.
### Tratamento de 'Gênero'
- Primeiro verifiquei qual os registros únicos e notei que existia uma categoria ‘Sem gênero’ que se encaixaria nesse contexto. Por isso, fiz o tratamento de nulos substituindo para essa categoria porque esse campo possui uma porcentagem bem baixa de registros nulos (4%) e fazendo isso, não influenciaria tanto, afinal, se não tem registro de gênero, muito provavelmente ele não é necessário para aquele contexto.
### Tratamento de 'Reviews'
- Pegando a lógica de Gênero, se não existe registro de review, quer dizer que o cliente não deixou um comentário. Por isso, podemos substituir essa ausência por ‘Sem comentários’, por exemplo.
### Tratamento de 'Preço'
- Esse tratamento vai ser o mais complicado, pois todos os produtos deveriam ter preço. Então, se não tem preço, o que aconteceu? Provavelmente foi erro de extração, mas não podemos colocar ‘Não informado’ por exemplo, porque esse campo é do tipo *float* e esse tratamento iria ir contra isso. Também não podemos fazer uma aproximação (usando alguma medida estatística) dele, pois iria ser provavelmente diferente do preço real e esse campo é muito importante. O que não seria o caso se fosse a idade (e não usaríamos esse campo pra análise, por exemplo), mas o preço será utilizado posteriormente, então provavelmente eu irei desconsiderar eles da minha análise;
- E pensando sobre isso, se eu vou desconsiderar esses registros da minha análise, não seria melhor excluí-los? Bom, ele representa 11% dos dados, o que é mediano, mas, como falei, esses dados são importantes e insubstituíveis, portanto, é uma abordagem interessante (se tiver uma sugestão melhor, eu adoraria ouvir!).
### Tratamento de 'Material_Freq'
- Esse campo representa a frequência das categorias de Material nos dados. Ela tem a mesma porcentagem de dados nulos que Material, o que leva a crer que foi criada enquanto os dados de Material contia nulos. Com isso, eu vou excluir ele agora e refazê-lo na etapa de preparação.
## Tratamento de Duplicados
- Com esse tratamento, notamos que 201 registros foram excluídos por estarem duplicados. Como não temos algum dado que necessariamente precisa ser único para ser válido (como um registro de clientes por CPF), esse tratamento será feito em toda base de dados e o Python irá fazer seu critério para duplicidade.
## Visualização de Outliers (EXTRA)
- Pode-se visualizar as variáveis numéricas de Nota, N_Avaliações, Desconto e Preço estão com bastante valores discrepantes;
- Porém isso é o esperado, já que são registro de produtos e alguns produtos podem ser mais populares que outros, e, por isso, terem uma nota maior, um desconto maior ou um preço maior. Por causa disso, não irei fazer o tratamento dessas outliers, mas deixarei aqui a nível de conhecimento (e como exemplo de como fazer esse tipo de gráfico comparativo).
## Verificando Dados Tratados 
- Ao final de todo esse trabalho, obtemos as seguintes informações:
  - **Quantidade de Registros Originais**: 2199
  - **Quantidade de Registros com Tratamento**: 1763
  - **Quantidade de Colunas Originais**: 24
  - **Quantidade de Colunas com Tratamento**: 17
  - **Nomes das Colunas Usadas**:<br> ['Título', 'Nota', 'N_Avaliações', 'Desconto', 'Marca', 'Material', 'Gênero', 'Temporada', 'Review1', 'Review2', 'Review3', 'Qtd_Vendidos', 'Preço', 'Marca_Cod', 'Material_Cod', 'Temporada_Cod', 'Marca_Freq']
  - **Quantidade de Nulos**: 0 (por coluna)
  - **Quantidade de Duplicados**: 0
- Esses dados foram salvos no arquivo 'ecommerce_tratado.csv', disponível na pasta 'dados'. 
