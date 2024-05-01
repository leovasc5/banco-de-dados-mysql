### Visão geral da linguagem SQL

A linguagem SQL (Structured Query Language) é uma linguagem padrão para a comunicação com bancos de dados relacionais, como o MySQL. Nesta seção, exploraremos uma visão geral dos principais elementos e comandos da linguagem SQL.

SQL é uma linguagem de consulta que permite realizar operações de leitura, inserção, atualização e exclusão de dados em um banco de dados. Ela oferece uma abordagem declarativa, o que significa que você especifica o que deseja obter ou fazer, e o banco de dados se encarrega de encontrar a melhor maneira de realizar essa tarefa.

#### Vamos dar uma olhada em alguns dos comandos SQL mais comuns:

<b>SELECT</b>: O comando é usado para recuperar dados de uma tabela ou conjunto de tabelas ele permite especificar as colunas que você deseja obter o filtro e condições para restringir resultados.

```sql
SELECT coluna1, coluna2 FROM tabela WHERE condição;
```

<b>INSERT</b>: O comando INSERT é usado para inserir novos registros em uma tabela.

```sql
INSERT INTO tabela (coluna1, coluna2) VALUES (valor1, valor2);
```

<b>UPDATE</b>: O comando UPDATE é usado para atualizar os valores de um ou mais registros em uma tabela.

```sql
UPDATE tabela SET coluna1 = novo_valor WHERE condição;
```

<b>DELETE</b>: O comando DELETE é usado para excluir registros de uma tabela.

```sql
DELETE FROM tabela  WHERE condição;
```

<b>ORDER BY</b>: A cláusula ORDER BY é usada para ordenar os resultados de uma consulta com base em uma ou mais colunas.

```sql
SELECT coluna1, coluna2 
FROM tabela 
ORDER BY coluna1 ASC;
```

<b>WHERE</b>: A cláusula WHERE é usada para filtrar os resultados de uma consulta com base em uma condição especificada.

```sql
SELECT coluna1, coluna2 
FROM tabela 
WHERE coluna1 = valor;
```

Esses são apenas alguns exemplos dos comandos SQL básicos mais utilizados. A linguagem SQL é bastante extensa e oferece uma variedade de recursos e comandos para manipulação e consulta de dados.

Agora que você tem uma visão geral da linguagem SQL, você está pronto para começar a utilizar os comandos básicos para interagir com o banco de dados MySQL. Nas seções seguintes deste capítulo, vamos explorar em mais detalhes cada um desses comandos e como utilizá-los para realizar operações específicas em um banco de dados.


#### Consultas SELECT

As consultas SELECT são um dos principais componentes da linguagem SQL. Elas permitem recuperar dados específicos de uma ou mais tabelas de um banco de dados. Vamos explorar como as consultas SELECT funcionam e como utilizá-las de forma eficaz.

A estrutura básica de uma consulta SELECT é a seguinte:

```sql
SELECT coluna1, coluna2, ... 
FROM tabela;
```

Nessa estrutura, você especifica as colunas que deseja obter na cláusula SELECT e a tabela da qual deseja recuperar os dados na cláusula FROM. Você pode selecionar todas as colunas de uma tabela utilizando o caractere de asterisco (*).

Aqui estão alguns exemplos práticos de consultas SELECT:

<b>Exemplo 1: Recuperar todas as colunas de uma tabela</b>

```sql
SELECT * 
FROM clientes;
```

<b>Exemplo 2: Recuperar colunas específicas de uma tabela</b>

```sql
SELECT nome, email 
FROM clientes;
```

<b>Aplicando Filtros e Condições com a cláusula WHERE:</b>

A cláusula WHERE é usada para aplicar filtros e condições em uma consulta SELECT, permitindo que você restrinja os resultados com base em critérios específicos. Por exemplo, se você deseja recuperar apenas os clientes cujo nome seja "João", você pode usar a cláusula WHERE da seguinte forma:

```sql
SELECT nome, email 
FROM clientes 
WHERE nome = 'João';
```

<b>Utilizando Funções na Consulta SELECT:</b>

A linguagem SQL fornece uma variedade de funções embutidas que podem ser utilizadas nas consultas SELECT para realizar cálculos ou manipular os dados retornados. Por exemplo, você pode utilizar a função COUNT para contar o número de registros retornados ou a função SUM para obter a soma de valores em uma coluna.

Exemplo: Contar o número de clientes:
```sql
SELECT COUNT(*) 
FROM clientes;
```

Esses são apenas alguns exemplos do uso das consultas SELECT. A linguagem SQL oferece uma ampla gama de recursos para personalizar suas consultas e recuperar os dados desejados de forma eficiente. À medida que avançamos neste livro, você aprenderá mais sobre consultas SELECT avançadas, como usar joins para combinar tabelas, utilizar subconsultas, agrupar dados com GROUP BY e aplicar filtros avançados com a cláusula HAVING.
 

#### Inserção, atualização e exclusão de dados

Na linguagem SQL, além de recuperar dados usando consultas SELECT, também podemos realizar operações para inserir, atualizar e excluir dados em um banco de dados. Essas operações são essenciais para manter os dados atualizados e gerenciar o conteúdo de suas tabelas. Vamos explorar como realizar essas operações.

<b>Inserção de Dados com o comando INSERT INTO:</b>

O comando INSERT INTO é utilizado para inserir novos registros em uma tabela. A sintaxe básica é a seguinte:

Exemplo: Contar o número de clientes:
```sql
INSERT INTO tabela (coluna1, coluna2, ...) VALUES (valor1, valor2, ...);
```

Nessa sintaxe, você especifica a tabela na qual deseja inserir os dados e, entre parênteses, as colunas nas quais os valores serão inseridos. Em seguida, você utiliza a palavra-chave VALUES, seguida pelos valores correspondentes a cada coluna.

Exemplo: Inserir um novo cliente na tabela "clientes":

```sql
INSERT INTO clientes (nome, email) VALUES ('João', 'joao@email.com');
```

<b>Atualização de Dados com o comando UPDATE: </b>

O comando UPDATE é utilizado para modificar dados existentes em uma tabela. A sintaxe básica é a seguinte:

```sql
UPDATE tabela 
SET coluna1 = valor1, coluna2 = valor2
WHERE condição;
```

Nessa sintaxe, você especifica a tabela que será atualizada e utiliza a palavra-chave SET para atribuir novos valores às colunas desejadas. A cláusula WHERE é opcional, mas permite especificar uma condição para atualizar apenas os registros que atendem a essa condição.

Exemplo: Atualizar o e-mail de um cliente na tabela "clientes":

```sql
UPDATE clientes 
SET email = 'novo@email.com'
WHERE id = 1;
```

Exclusão de Dados com o comando DELETE:

O comando DELETE é utilizado para excluir registros de uma tabela. A sintaxe básica é a seguinte:
 
```sql
DELETE FROM tabela
WHERE condição;
```

Nessa sintaxe, você especifica a tabela da qual deseja excluir registros. A cláusula WHERE é opcional, mas permite definir uma condição para excluir apenas os registros que atendem a essa condição.

Exemplo: Excluir um cliente da tabela "clientes":
 
```sql
DELETE FROM clientes
WHERE id = 1;
```

É importante tomar cuidado ao usar os comandos de atualização e exclusão, pois eles podem afetar permanentemente os dados em seu banco de dados. Certifique-se sempre de ter backups adequados e de executar essas operações com cautela.

Essas são as operações básicas de inserção, atualização e exclusão de dados utilizando comandos SQL. Elas permitem que você gerencie o conteúdo das suas tabelas de forma flexível e eficiente. À medida que avançarmos no livro, você aprenderá técnicas mais avançadas e estratégias recomendadas para lidar com essas operações.
 
<b>Ordenação de resultados</b>

Ao recuperar dados de um banco de dados, é comum querermos que os resultados sejam exibidos em uma ordem específica. Para isso, utilizamos a cláusula ORDER BY na consulta SQL. Essa cláusula permite ordenar os resultados com base em uma ou mais colunas.



---
<div align="center">
    <a href="introducao.md"><kbd> <br> Capítulo Anterior <br> </kbd></a>‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ 
    <a href=""><kbd> <br> Próximo Capítulo <br> </kbd></a>
</div>