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
Supondo que você acompanhou nosso vídeo e criou a tabela de usuarios. Rode o seguinte comando para popular essa tabela com outras linhas: 

```
insert into usuarios (nome, senha, apelido, verificado, data_cadastro)
 values 
('Quero ser programador', 'minhasenha2019', 'well',  1, '2018-11-21'),
('Claudson Oliveira', 'bar','cloudson',  1, '2019-01-01'),
('Joe Jobs', 'foo', 'well',  1, '2017-03-12'),
('Quero ser programador','zas', 'qsprogramador',  1, '2019-01-01'),
('Amanda Diniz', '', 'well',  1, '2019-01-01'),
('Adriana silva', 'adriana123', 'adr2019',  1, '2019-01-10'),
('Claudio Souza', 'claudio121','claudio',  0, '2019-01-01'),
('Bruna Oliveira', 'foo', 'bruna',  1, '2017-03-12'),
('Quero ser programador de novo', 'zas2', 'qsprogramador',  1, '2019-01-01'),
('Carol Schmit', 'foo', 'carol2019',  1, '2017-03-12');
```
Perceba que podemos usar apenas um comando insert definindo vários values e que também não passamos a coluna email, mesmo assim o mysql aceitou gravar as linhas sem esse valor, ou melhor, com valor `null` (vazio). 

### 04 

Além de definir os tipos de colunas voce pode definir que uma tabela não aceita valores null. Para isso basta na definição da coluna colocar no fim `not null`. 
Delete a tabela mensagens usando o comando `drop table mensagens` e após isso crie ela novamente definindo que a coluna texto é not null. 
Após isso tente inserir uma mensagem sem texto e veja se o mysql mostra um erro. 
