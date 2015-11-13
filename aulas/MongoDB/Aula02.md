# MongoDB - Correção do exercício da Aula 01 e inserção de novos dados


## Comandos

### `use nome_database`

- Específica *database* que deseja usar dentro do console do mongo.

### ou

### `mongo nome_database`

- Específica *database* que deseja usar.

### `show dbs`

- Listamos a nossa databases

### `show collections`

- Listamos toda as coleções.

### `db.sua_collection.insert({nome: 'Mara Jeannie', profissao: 'Professora'})`

- Inserindo algo na database.

### `db.createCollection()`

- Cria uma coleção vazia.

## Insert com variável

```
var json = {escola: 'EAD WebSchool', active: true}
db.sua_collection.insert(json)
```

### `db.sua_collection.find()`

- Conferindo os documentos de uma coleção.

### `db.sua_collection.save(obj)`

- Insere e salva um objeto.
`var json = {nome: 'bla'}; db.sua_collection.save(json)`

## Modificando um objeto

- Cria uma query de busca: **`var query = {name: 'nome_a_ser_buscado'}`**

- Passando a variável para o find(): **`var _p = db.sua_collection.find(query)`**

*Obs: Fazendo assim o nosso Objeto é retornado em forma de *curso* e não conseguimos acessar diretamente os seus valores. É preciso fazer a utilização do **findOne()**.

**`var _p = db.sua_collection.findOne(query)`**

Assim acessamos e podemos modificar o documento.

**`_p.documento = 'valor_a_ser_passado'`**

Depois é só salvar a modificação

**`db.sua_collection.save(_p)`**

## Exercício da Aula
### [Exercício](https://github.com/Webschool-io/be-mean-instagram/blob/master/apostila/classes/mongodb/class-02-resolved.md)
### [Exercício Resolvido](https://github.com/TiagoWinehouse/be-mean-instagram-mongodb/blob/master/exercises/class-02-resolved-tiagowinehouse.md)

---


Faculdade EAD [WebSchool-io](https://github.com/Webschool-io)
