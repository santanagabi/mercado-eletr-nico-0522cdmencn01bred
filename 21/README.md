# Aula 21 - Introdução à banco de dados

## DDL

Na DDL temos os comandos da linguagem SQL para definir a estrutura (modelagem) em nosso banco de dados. Quando falamos de definição estamos nos referindo ao comando para criar (CREATE), para alterar (ALTER) e para deletar (DROP) um objeto da modelagem.

### CREATE

Por meio do comando CREATE é possível criar tanto uma nova tabela no modelo quanto o próprio esquema de banco de dados. Como sabemos uma tabela não existe sem um banco de dados então primeiro iremos executar a criação do nosso esquema de banco.

A sintaxe do comando CREATE é:

**Criar um banco**

```
CREATE DATABASE nomedobanco;
```

**Criar tabela**

```
CREATE TABLE nomedatabela(
    coluna1 TIPO [COMANDO],
    coluna2 TIPO [COMANDO],
    coluna3 TIPO [COMANDO]
)
```

**Nota:** O tipo pode ser um dos vários que já vimos na seção anterior. Já os comandos podem ser nenhum ou vários dos disponiveis iremos ver melhor os comandos mais a baixo. Mas saiba que os seguintes comandos podem ser aplicados: PRIMARY KEY, NOT NULL, NULL, IDENTITY, FOREIGN KEY, dentre outros.

### ALTER

O comando ALTER destina-se a realizar alterações na estrutura de um objeto do banco. Por exemplo em nossa tabela de endereço ficou ausente o campo para informar a cidade. Então teremos de incluir uma alteração na estrutura da tabela para receber este novo campo. E também vamos alterar a precisão do campo complemento que ficou pequena.

- [ ] Incluir coluna cidade.

```
ALTER TABLE endereco ADD cidade NVARCHAR(50) NULL;
```

- [ ] Alterar coluna complemento.

```
ALTER TABLE endereco ALTER COLUMN complemento NVARCHAR(20) NULL;
```

- [ ] Adicionar um novo relacionamento entre Endereco e UF.

```
ALTER TABLE endereco ADD CONSTRAINT FK_ENDERECO_UF FOREIGN KEY (id_uf) REFERENCES uf(id);
```