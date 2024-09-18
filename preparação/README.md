# Preparação de Dados 🎲
- Para essa segunda etapa do projeto, irei realizar a Normalização dos dados e Engenharia de Features:
    - Campos adicionas de escala, utilizando o MinMaxScaler;
    - Campo de frequência para Material.
  
_OBS: Qualquer sugestão para melhoria de qualquer parte desse projeto, pode entrar em contato comigo pelo LinkedIn ou email (link no perfil)._
# Bibliotecas Utilizadas 📋
> Pandas <br>
> Sklearn
# Construção 🔧
## Normalização
### Normalização de Texto

- Normalização de campos de texto a fim de deixar os registros de nomes com a primeira letra em maiúsculo.

### MinMaxScaler

- Como mencionado na etapa anterior, irei realizar novamente o processo de criação dos campos utilizando o MinMaxScaler, pois as variáveis originais tiveram alteração de tratamento e, por isso, ele tipo de trabalho deveria ser realizado novamente;
- Com isso, será criada escalas para Nota, N_Avaliações, Desconto e Preço, a fim de fazer visualizações interessantes na próxima etapa.
## Engenharia de Feature
### Frequência

- Na última etapa, eu tive que fazer a exclusão do campo ‘Material_Freq’, pois precisei fazer tratamento da variável original Material (o que não foi necessário para ‘Marca_Freq’);
- Por causa disso, nessa etapa irei refazer esse campo a fim de ter-se mais uma informação interessante para este projeto.

## Salvando Dados Preparados

- Ao fim da etapa de preparação, tivemos as seguintes informações:
    - Quantidade de Linhas: 1763;
    - Quantidade de Colunas: 22;
    - Adição dos Campos: 'Nota_MinMax', 'N_Avaliações_MinMax', 'Desconto_MinMax', 'Preço_MinMax', 'Material_Freq’.
- Os dados foram armazenados no arquivo ‘ecommerce_preparados.csv’, disponível na pasta ‘dados’.
