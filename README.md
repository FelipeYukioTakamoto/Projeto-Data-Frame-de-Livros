# Projeto Data Frame de Livros e Manipulação de Dados com Pandas

Este projeto é uma demonstração de habilidades em manipulação de dados e programação utilizando a biblioteca pandas do Python. O objetivo é realizar várias operações comuns em DataFrames, como criação, acesso, modificação, transposição e verificação de dados.

O tema deste projeto foi inspirado pela vida real, especificamente pela minha biblioteca pessoal em casa. A base de dados contém informações sobre alguns dos livros dessa coleção particular, incluindo títulos, autores, anos de publicação e gêneros. 

A criação de um DataFrame de livros permite organizar, manipular e analisar esses dados de forma estruturada e eficiente. Através deste projeto, demonstramos como utilizar a biblioteca pandas do Python para realizar operações comuns em DataFrames e obter insights valiosos sobre a coleção de livros.

Neste projeto, utilizamos a estrutura de dados DataFrame fornecida pela biblioteca Pandas. A escolha pelo DataFrame se deve a diversas características que fazem dele uma ferramenta robusta e eficiente para manipulação e análise de dados tabulares. Dentro do código foi utilizada a estrutura de Dicionário que serão posteriormente convertidos em um DataFrame pandas.

https://colab.research.google.com/drive/1BcOVPYmkfiXGLJf7G61c9MDArARhdvjP?usp=sharing

## Descrição

O projeto aborda as seguintes etapas:

1. **Criação do DataFrame:** Criação de uma base de dados (DataFrame) com informações sobre livros.
2. **Apresentação da Base de Dados:** Exibição completa da base de dados criada.
3. **Tamanho do DataFrame:** Apresentação do número de linhas e colunas do DataFrame.
4. **Acesso a uma Linha Específica:** Acesso e exibição das características de uma linha específica do DataFrame.
5. **Verificação de DataFrame Vazio:** Verificação se o DataFrame está vazio.
6. **Apresentação dos 5 Primeiros Registros:** Exibição dos primeiros 5 registros do DataFrame.
7. **Exclusão de uma Linha:** Remoção de uma linha específica do DataFrame.
8. **Adição de uma Linha:** Adição de uma nova linha ao DataFrame.
9. **Transposição do DataFrame:** Transposição do DataFrame, trocando linhas por colunas.
10. **Exibição de Colunas Específicas:** Exibição somente das duas primeiras colunas do DataFrame.

## Instalação

Para executar este projeto, você precisa ter o Python e a biblioteca pandas instalados. Você pode instalar a biblioteca pandas usando pip:

```bash
pip install pandas
```

## Como Usar

Aqui está um exemplo de como você pode usar o código fornecido para realizar cada uma das etapas mencionadas:

### Criação do DataFrame
```python
import pandas as pd

# Definindo os dados para o DataFrame em um dicionário
dados = {
    'Titulo': [
        'Dom Quixote', 'Guerra e Paz', 'Moby Dick', 'Orgulho e Preconceito', '1984',
        'O Grande Gatsby', 'Ulisses', 'Cem Anos de Solidão', 'O Senhor dos Anéis', 'Crime e Castigo',
        'O Apanhador no Campo de Centeio', 'As Vinhas da Ira', 'Lolita', 'O Estrangeiro',
        'O Processo', 'A Metamorfose', 'O Sol é Para Todos', 'A Odisséia', 'Hamlet',
        'O Hobbit', 'O Nome da Rosa', 'O Retrato de Dorian Gray', 'O Conde de Monte Cristo', 'A Divina Comédia',
        'Os Miseráveis', 'A Montanha Mágica', 'Germinal', 'A Peste', 'Don Juan',
        'O Médico e o Monstro', 'Memórias Póstumas de Brás Cubas', 'Grande Sertão: Veredas', 'A Moreninha',
        'Iracema', 'Senhora', 'Mar Morto', 'Vidas Secas', 'Capitães da Areia', 'O Pequeno Príncipe'
    ],
    'Autor': [
        'Miguel de Cervantes', 'Liev Tolstói', 'Herman Melville', 'Jane Austen', 'George Orwell',
        'F. Scott Fitzgerald', 'James Joyce', 'Gabriel García Márquez', 'J.R.R. Tolkien', 'Fiódor Dostoiévski',
        'J.D. Salinger', 'John Steinbeck', 'Vladimir Nabokov', 'Albert Camus',
        'Franz Kafka', 'Franz Kafka', 'Harper Lee', 'Homero', 'William Shakespeare',
        'J.R.R. Tolkien', 'Umberto Eco', 'Oscar Wilde', 'Alexandre Dumas', 'Dante Alighieri',
        'Victor Hugo', 'Thomas Mann', 'Émile Zola', 'Albert Camus', 'Lord Byron',
        'Robert Louis Stevenson', 'Machado de Assis', 'João Guimarães Rosa', 'Joaquim Manuel de Macedo',
        'José de Alencar', 'José de Alencar', 'Jorge Amado', 'Graciliano Ramos', 'Jorge Amado', 'Antoine de Saint-Exupéry'
    ],
    'Ano de Publicação': [
        1605, 1869, 1851, 1813, 1949,
        1925, 1922, 1967, 1954, 1866,
        1951, 1939, 1955, 1942,
        1925, 1915, 1960, -800, 1600,
        1937, 1980, 1890, 1844, 1320,
        1862, 1924, 1885, 1947, 1819,
        1886, 1881, 1956, 1844,
        1865, 1875, 1936, 1938, 1937, 1943
    ],
    'Gênero': [
        'Romance', 'Histórico', 'Aventura', 'Romance', 'Distopia',
        'Romance', 'Modernismo', 'Realismo Mágico', 'Fantasia', 'Ficção Psicológica',
        'Romance', 'Drama', 'Ficção', 'Ficção Filosófica',
        'Ficção', 'Ficção', 'Drama', 'Épico', 'Tragédia',
        'Fantasia', 'Mistério', 'Ficção', 'Aventura', 'Poesia',
        'Drama', 'Ficção', 'Realismo', 'Ficção Filosófica', 'Poesia',
        'Terror', 'Romance', 'Modernismo', 'Romance',
        'Romance', 'Romance', 'Ficção', 'Ficção', 'Ficção', 'Infantil'
    ],
    'Editora': [
        'Companhia das Letras', 'Editora Record', 'Editora Rocco', 'Editora Arqueiro', 'Companhia das Letras',
        'Editora Rocco', 'Companhia das Letras', 'Editora Record', 'Companhia das Letras', 'Editora Record',
        'Companhia das Letras', 'Editora Rocco', 'Companhia das Letras', 'Editora Rocco',
        'Companhia das Letras', 'Companhia das Letras', 'Editora Record', 'Companhia das Letras', 'Companhia das Letras',
        'Companhia das Letras', 'Editora Rocco', 'Companhia das Letras', 'Editora Record', 'Companhia das Letras',
        'Editora Rocco', 'Companhia das Letras', 'Editora Rocco', 'Editora Rocco', 'Companhia das Letras',
        'Editora Rocco', 'Companhia das Letras', 'Editora Record', 'Companhia das Letras',
        'Editora Record', 'Editora Record', 'Editora Rocco', 'Companhia das Letras', 'Editora Record', 'Companhia das Letras'
    ],
    'Número de Páginas': [
        863, 1225, 635, 279, 328,
        218, 730, 417, 1216, 430,
        277, 464, 336, 123,
        304, 201, 281, 374, 342,
        310, 592, 254, 1243, 426,
        1488, 720, 556, 308, 128,
        138, 192, 624, 192,
        140, 268, 256, 176, 288, 96
    ]
}

# Criando o DataFrame usando o dicionário de dados
df = pd.DataFrame(dados)

# Exibindo o DataFrame completo
print("DataFrame completo:")
print(df)
```
Apresentação de Toda a Base de Dados: Uma vez que o DataFrame é criado, podemos exibi-lo na tela usando a função print(df). Isso mostra todas as linhas e colunas do DataFrame.

### 1. Apresentação do DataFrame

```python
print("DataFrame completo:")
print(df)
```
Apresentação do Tamanho do DataFrame: O atributo .shape retorna uma tupla com o número de linhas e colunas do DataFrame. Isso é útil para entender a dimensão do DataFrame e sua estrutura.

### 2. Tamanho do DataFrame

```python
print("Tamanho do DataFrame:", df.shape)
```
Acesso e Apresentação de uma Linha Específica: Para acessar uma linha específica do DataFrame, usamos o método .loc[]. Este método permite acessar uma linha pelo seu rótulo. Após acessar a linha, ela pode ser apresentada na tela usando print(df.loc[linha_indice]).

### 3. Acesso a uma Linha Específica

```python
linha_indice = 2
print(f"Linha {linha_indice}:")
print(df.loc[linha_indice])
```
Verificação se o DataFrame Está Vazio: O atributo .empty retorna True se o DataFrame estiver vazio (não contiver linhas) e False caso contrário. Isso é útil para verificar se o DataFrame contém dados antes de realizar operações nele.

### 4. Verificação se o DataFrame Está Vazio

```python
print("DataFrame está vazio?", df.empty)
```
Apresentação dos 5 Primeiros Registros: O método .head() retorna as primeiras linhas do DataFrame. O padrão é retornar as primeiras 5 linhas, mas esse número pode ser especificado. Isso é útil para uma rápida visualização dos dados.

### 5. Apresentação dos 5 Primeiros Registros

```python
print("Os 5 primeiros registros do DataFrame:")
print(df.head())
```
Exclusão de uma Linha da Base de Dados: O método .drop() é usado para excluir linhas ou colunas do DataFrame. Passamos o índice da linha que desejamos excluir como argumento. Isso permite remover dados indesejados do DataFrame.

### 6. Exclusão de uma Linha

```python
df = df.drop(index=2)
print("DataFrame após exclusão da linha com índice 2:")
print(df)
```
Adição de uma Linha à Base de Dados: O método .append() é usado para adicionar uma nova linha ao DataFrame. Podemos passar um dicionário contendo os dados da nova linha como argumento. Isso é útil para inserir novos dados no DataFrame.

### 7. Adição de uma Linha

```python
novo_livro = {'Titulo': 'Harry Potter', 'Autor': 'J.K. Rowling', 'Ano de Publicação': 1997, 'Gênero': 'Fantasia'}
df = df.append(novo_livro, ignore_index=True)
print("DataFrame após adicionar uma nova linha:")
print(df)
```
Transposição da Coluna para a Linha: A transposição de um DataFrame significa trocar suas linhas por colunas e vice-versa. Isso é útil para alterar a orientação dos dados, especialmente em análises onde essa forma de apresentação é mais adequada.

### 8. Transposição do DataFrame

```python
df_transposto = df.transpose()
print("DataFrame transposto:")
print(df_transposto)
```
Apresentação das Duas Primeiras Colunas: Podemos selecionar as colunas desejadas do DataFrame usando indexação ou o método .iloc[]. Usando .iloc[:, :2], selecionamos todas as linhas (:) e as duas primeiras colunas (:2). Isso nos permite exibir apenas as informações relevantes.

### 9. Exibição das Duas Primeiras Colunas

```python
print("Primeira e segunda colunas do DataFrame:")
print(df.iloc[:, :2])
```
Primeiro abstrai da vida real um conteúdo para o meu DataFrame, depois abri o Google Colaboratory para criar o meu DataFrame usando Python.

## Contribuição

Sinta-se à vontade para contribuir com este projeto. Você pode fazer isso da seguinte maneira:

1. Faça um fork deste repositório.
2. Crie um branch para suas alterações (`git checkout -b minha-nova-funcionalidade`).
3. Commit suas alterações (`git commit -am 'Adiciona nova funcionalidade'`).
4. Envie para o branch (`git push origin minha-nova-funcionalidade`).
5. Abra um Pull Request.

## Referências

Python Academy. DataFrames do Pandas. Disponível em: https://pythonacademy.com.br/blog/dataframes-do-pandas. Acesso em: [21 maio 2024].

PyData. pandas.DataFrame. Disponível em: https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html. Acesso em: [21 maio 2024].

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo LICENSE para obter mais detalhes.

---

Este arquivo README.md fornece uma visão geral do projeto, instruções de instalação, exemplos de uso, diretrizes de contribuição e informações sobre a licença. Ele pode ser ajustado conforme necessário para se adequar às especificidades do seu projeto.
