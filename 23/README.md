## DML - Data Manipulation Language (Linguagem de Manipulação de Dados)

Na DML temos as definições das linguagens SQL para manipular nossos registros em banco de dados. Quando nos referimos a manipulação estamos falando das operações de Seleção (SELEC), Deleção (DELETE), Inserção (INSERT) e Atualização (UPDATE).

Após termos definido a estrutura de nosso banco de dados por meio dos comandos DDL utilizados na seção anterior. Nesta seção iremos trabalhar com os dados (registros) em nosso banco de dados.

### INSERT

```sql
INSERT INTO tabela(coluna1, coluna2, coluna3) 
VALUES ('valor1', valor2, 'valor3');
```

O Comando INSERT é responsável por inserir registros em uma tabela do banco de dados. É um comando simples sua sintaxe é:

- [ ] Inserir Registros nas nossas tabelas.

**Nota:** Quando queremos inserir mais de um registro com uma única instrução INSERT basta colocar "," (vírgula) e declarar os valores tal como o nosso exemplo abaixo. Observe como está sendo inserido.

```sql
INSERT INTO contato (nome, apelido, email_principal, sexo, data_nascimento)
VALUES ('John Doe', null, 'john@gmail.com', 'M', CONVERT(DATE,'1993-04-20')),
('Jane Doe', null, 'jane@gmail.com', 'F', CONVERT(DATE,'1978-08-21')),
('Maria Betânia', null, 'maria.b@gmail.com', 'F', CONVERT(DATE,'1949-12-01')),
('Paulo Augusto', null, 'paulo.augusto@outlook.com', 'M', CONVERT(DATE,'1966-12-19')),
('José Linhares', 'zé', 'ze@outlook.com', 'M', CONVERT(DATE,'2000-01-09')),
('Mônica', 'moniquinha', 'monicab@yahoo.com', 'F', CONVERT(DATE,'1998-08-21')),
('Magali', 'maga', 'magali@gmail.com', 'F', CONVERT(DATE,'1997-06-04')),
('Cebola Acelga', 'cebolinha', 'cebola@gmail.com', 'M', CONVERT(DATE,'1999-08-02')),
('Isabella Furtado', null, 'bella@yahoo.com', 'F', CONVERT(DATE,'1993-10-05')),
('Cascão Suginho', 'cascao', 'cascao@gmail.com', 'M', CONVERT(DATE,'1997-01-01'));
```

### SELECT

```sql
SELECT colunas FROM tabela
```

O comando SELECT é responsável por realizar as famosas consultas ao banco de dados. Por meio dele recuperamos os registros que temos disponíveis em nossa base de dados. E também conseguimos realizar condições de busca, agrupamento e ordenação. É possível atender qualquer necessidade de consulta por meio do SELECT e seus comandos adicionais.

```sql
SELECT * FROM contato;
SELECT nome, sexo, data_nascimento FROM contato;
```

### WHERE

```sql
SELECT colunas FROM tabela WHERE condicao
```

O WHERE especifica as condições de busca para o retorno de uma consulta.

```sql
SELECT * 
  FROM contato 
 WHERE nome like 'Joh%';
 
SELECT * 
  FROM contato 
 WHERE sexo = 'F' AND apelido IS NOT NULL
```

Abaixo temos um guia com os operadores mais utilizados na criação de condições lógicas nas consultas:

**L