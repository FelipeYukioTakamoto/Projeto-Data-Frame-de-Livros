# Projeto Data Frame de Livros e Manipulação de Dados com Pandas

Este projeto é uma demonstração de habilidades em manipulação de dados e programação utilizando a biblioteca pandas do Python. O objetivo é realizar várias operações comuns em DataFrames, como criação, acesso, modificação, transposição e verificação de dados.

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

**### 1. Criação do DataFrame**
```python
import pandas as pd

dados = {
    'Titulo': ['Dom Quixote', 'Guerra e Paz', 'Moby Dick', 'Orgulho e Preconceito', '1984'],
    'Autor': ['Miguel de Cervantes', 'Liev Tolstói', 'Herman Melville', 'Jane Austen', 'George Orwell'],
    'Ano de Publicação': [1605, 1869, 1851, 1813, 1949],
    'Gênero': ['Romance', 'Histórico', 'Aventura', 'Romance', 'Distopia']
}

df = pd.DataFrame(dados)
print(df)
```

### 2. Apresentação do DataFrame

```python
print("DataFrame completo:")
print(df)
```

### 3. Tamanho do DataFrame

```python
print("Tamanho do DataFrame:", df.shape)
```

### 4. Acesso a uma Linha Específica

```python
linha_indice = 2
print(f"Linha {linha_indice}:")
print(df.loc[linha_indice])
```

### 5. Verificação se o DataFrame Está Vazio

```python
print("DataFrame está vazio?", df.empty)
```

### 6. Apresentação dos 5 Primeiros Registros

```python
print("Os 5 primeiros registros do DataFrame:")
print(df.head())
```

### 7. Exclusão de uma Linha

```python
df = df.drop(index=2)
print("DataFrame após exclusão da linha com índice 2:")
print(df)
```

### 8. Adição de uma Linha

```python
novo_livro = {'Titulo': 'Harry Potter', 'Autor': 'J.K. Rowling', 'Ano de Publicação': 1997, 'Gênero': 'Fantasia'}
df = df.append(novo_livro, ignore_index=True)
print("DataFrame após adicionar uma nova linha:")
print(df)
```

### 9. Transposição do DataFrame

```python
df_transposto = df.transpose()
print("DataFrame transposto:")
print(df_transposto)
```

### 10. Exibição das Duas Primeiras Colunas

```python
print("Primeira e segunda colunas do DataFrame:")
print(df.iloc[:, :2])
```

## Contribuição

Sinta-se à vontade para contribuir com este projeto. Você pode fazer isso da seguinte maneira:

1. Faça um fork deste repositório.
2. Crie um branch para suas alterações (`git checkout -b minha-nova-funcionalidade`).
3. Commit suas alterações (`git commit -am 'Adiciona nova funcionalidade'`).
4. Envie para o branch (`git push origin minha-nova-funcionalidade`).
5. Abra um Pull Request.

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo LICENSE para obter mais detalhes.

---

Este arquivo README.md fornece uma visão geral do projeto, instruções de instalação, exemplos de uso, diretrizes de contribuição e informações sobre a licença. Ele pode ser ajustado conforme necessário para se adequar às especificidades do seu projeto.
