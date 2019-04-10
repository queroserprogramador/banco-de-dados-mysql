# 02 Como criar tabelas no mysql 
## Vídeo

https://youtu.be/QgWfHKyT4sE 

## Exercícios 

### 01 
No vídeo citado acima nós criamos uma tabela usando o comando  `create table usuarios (nome varchar(255), senha varchar(255), apelido varchar(30), verificado tinyint(1), data_cadastro datetime);
`

| Usuarios  |
|---|
| nome  |
| email  |
| senha  |
| apelido  |
| verificado  |
|data_cadastro|

Logo em seguida nós citamos uma tabela de tweets. Observando a estrutura dessa tabela, escreva e rode e comando para criá-la. 

| Tweets  |
|---|
| texto  |
| usuario  |
|data_cadastro|

### 02
Assim como os tipos de colunas que vemos no vídeo (varchar, tinyint e datetime), o mysql possui vários outros ([documentação oficial em inglês](https://dev.mysql.com/doc/refman/8.0/en/data-types.html) ). Cria uma tabela chamada `mensagens` que é identica a tabela tweets, porém ela usa o tipo de coluna text ao invés de varchar. Não se esquece de usar o comando `desc mensagens` para confirmar a estrutura da tabela.  

### 03 
