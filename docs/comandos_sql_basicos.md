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
SELECT coluna1, coluna2, ... FROM tabela;
```

Nessa estrutura, você especifica as colunas que deseja obter na cláusula SELECT e a tabela da qual deseja recuperar os dados na cláusula FROM. Você pode selecionar todas as colunas de uma tabela utilizando o caractere de asterisco (*).

Aqui estão alguns exemplos práticos de consultas SELECT:

<b>Exemplo 1: Recuperar todas as colunas de uma tabela</b>

```sql
SELECT * FROM clientes;
```

<b>Exemplo 2: Recuperar colunas específicas de uma tabela</b>

```sql
SELECT nome, email FROM clientes;
```

---
<div align="center">
    <a href="introducao.md"><kbd> <br> Capítulo Anterior <br> </kbd></a>‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ ‎ 
    <a href=""><kbd> <br> Próximo Capítulo <br> </kbd></a>
</div>