[![Autor](https://img.shields.io/badge/Autor-AlanBilly-blue.svg)](https://www.linkedin.com/in/alanbillyteixeirareis)
[![Professor](https://img.shields.io/badge/Professor-AlexSouza-red.svg)](https://github.com/aasouzaconsult) 
![Assunto](https://img.shields.io/badge/Assunto-SQL-yellow.svg)
<!-- Imagem redimensionada -->
<img src="https://digitalcollege.com.br/wp-content/webp-express/webp-images/uploads/2022/05/logo-digital.png.webp" alt="texto alt" width="300">

<!-- Imagem redimensionada -->
<img src="https://itforum.com.br/wp-content/uploads/2018/05/dataanalytics_1193397784-2.jpg?x17029" alt="texto alt" width="600">

# Desafio SQL
Este projeto tem como objetivo demonstrar o gerenciamento de dados pessoais em um banco de dados fictício usando SQL e fornecer exemplos de consultas SQL  .

## Status
![Badge em Desenvolvimento](https://img.shields.io/static/v1?label=STATUS&message=FINALIZADO&color=GREEN&style=for-the-badge)

# Desafio

- Criar uma tabela: tbpessoa com os campos: cod, nome, cpf e datanasc
- Inserir 10 registros aleatórios (dados fictícios)
- Alterar a datanasc do cod de número 5 para 08/03/2022
- Deletar o registro do cod de número 10
- Alterar o tipo de dado do campo: cod para smallint, se tiver smallint, 
mude para bigint
- Criar uma outra tabela, relacionar com a de cima e gerar 
selects´s, joins entre elas e inove

## Sobre
Este projeto tem como objetivo demonstrar a manipulação de dados em um banco de dados utilizando SQL. Vamos criar tabelas, inserir registros, fazer alterações e realizar consultas em um banco de dados fictício.

## História do SQL 📜
O SQL (Structured Query Language) é uma linguagem de programação utilizada para gerenciar sistemas de gerenciamento de banco de dados relacionais (RDBMS). Foi desenvolvido na década de 1970 por Donald D. Chamberlin e Raymond F. Boyce na IBM, e a primeira versão padronizada foi lançada em 1986. Desde então, o SQL tem desempenhado um papel fundamental na gestão e recuperação de dados em bancos de dados.

## Funcionalidades 💡
O SQL oferece diversas funcionalidades, incluindo:
- Criação e gerenciamento de tabelas.
- Inserção, atualização e exclusão de registros.
- Consultas complexas com operações como SELECT, JOIN e GROUP BY.
- Definição de restrições de integridade e chaves estrangeiras.
- Controle de permissões de acesso aos dados.

## Pré-requisitos 🛠️
Antes de começar, certifique-se de que você tenha o seguinte:
- Um sistema de gerenciamento de banco de dados instalado (por exemplo, MySQL, PostgreSQL, SQLite).
- Conhecimento básico em SQL.
- Um ambiente de desenvolvimento ou ferramenta de gerenciamento de banco de dados (por exemplo, MySQL Workbench, pgAdmin, DBeaver).

## 🏁 Começando 🚀
A seguir, os passos para realizar as operações descritas no projeto:

### Passo 1: Criar um banco de dados :computer:
```sql
CREATE DATABASE Desafio_sql ;
```

### Passo 2: Criar uma tabela 📋
  - Clientes
    ```sql
    CREATE TABLE tbpessoa(
          codpes INT PRIMARY KEY, 
          nome VARCHAR (80),
          cpf VARCHAR (11),
          datanasc DATE);  
    ```
### Passo 3: Inserir 10 registros aleatórios 📥
 - INSERINDO DADOS
    ```sql
    INSERT INTO tbpessoa VALUES
          (1, 'João da Silva', '12345678901', '1990-05-15'),
          (2, 'Maria Oliveira', '98765432101', '1985-12-20'),
          (3, 'Pedro Santos', '45678912301', '1998-07-10'),
          (4, 'Ana Pereira', '32165498701', '1992-03-25'),
          (5, 'Carlos Fernandes', '78945612301', '1987-09-05'),
          (6, 'Laura Almeida', '65432198701', '2000-11-30'),
          (7, 'Fernando Souza', '14725836901', '1995-06-18'),
          (8, 'Mariana Ribeiro', '85236974101', '1989-08-12'),
          (9, 'Ricardo Gomes', '36914725801', '1993-04-02'),
          (10, 'Isabel Lima', '74185236901', '1997-01-22');
    ```
### Passo 4: Alterar a datanasc do cod 5 🔄
```sql
UPDATE tbpessoa
SET datanasc = '2022-03-08'
WHERE codpes = 5
```
### Passo 5: Deletar o registro do cod 10 🗑️
``` sql
DELETE FROM tbpessoa
WHERE codpes = 10
```
### Passo 6: Alterar o tipo de dado do campo cod 🔢
 - Verificando qual o tipo de dado
    ```sql
    SELECT column_name, data_type
    FROM information_schema.columns
    WHERE table_name = 'tbpessoa';
    ```
    ou olhando so o pedido
    ```sql
    SELECT data_type
    FROM information_schema.columns
    WHERE table_name = 'tbpessoa' AND column_name = 'codpes';
    ```
 - Alterando
    ```sql
    ALTER TABLE tbpessoa
    ALTER COLUMN codpes TYPE smallint
    ```       
### Passo 7: Criar outra tabela e realizar consultas 🔍 
```sql

```
