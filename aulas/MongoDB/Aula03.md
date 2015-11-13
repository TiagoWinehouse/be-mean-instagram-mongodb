# MongoDB - Correção do exercício da Aula 02 e find-findOne (Retrive)


## Comandos

### `db.find()`

### ou

### `db.findOne()`

- Fazendo uma busca.

## _id

- É um [UUID](https://en.wikipedia.org/wiki/Universally_unique_identifier).
- **Obs: No mongodb não tem auto-increment**
- O _id é formado pelo seguintes dados:

	**4-bytes: valor que representa os segundos desde a época Unix;**

	**3-bytes: identificador de máquina;**

	**2-bytes: ID do processo;**

	**3-bytes: contador, começando com um valor aleatório.**


## Sintaxe

### `db.collection.find({clausulas}, {campos})`

- Aceita 2 campos.

### Query
#### `	var query = {name:'nome_a_ser_pesquisado'}`
#### `	db.collection.find(query)`

### Fields
- Campos desejado na busca da query.
- Especificamos os campos desejados **True:1; False:0;**

### `var fields = {name:1, description:1}`

- Negando o campo _id

### `var fields = {campo:1, campo_1:1, _id:0}`

## Operadores Aritméticos

### `< é $lt {less than}`

`db.collection.find({ "campo" : { $lt: value } } )` **Retorna objetos com valores menores que value.**

### `<= ou $lte - less than or equal`

`db.collection.find({ "campo" : { $lte: value } } )` **Retorna objetos com valores menores ou igual que value.**

### `> ou $gt - greater than`

`db.collection.find({ "campo" : { $gt: value } } )` **Retorna objetos com valores maiores que value.**

### `>= ou $gte - greater than or equal`

`db.collection.find({ "campo" : { $gte: value } } )` **Retorna objetos com valores maiores ou igual que value.**

## Operadores Lógicos

### `$or`
 `db.collection.find( { $or : [ { a : 1 } , { b : 2 } ] } ) db.foo.find( { name : "bob" , $or : [ { a : 1 } , { b : 2 } ] } )` **Retorna objetos caso a cláusula OU for verdadeira.**

### `$nor`

`db.collection.find( { $nor : [ { a : 1 } , { b : 2 } ] } )` **Retorna objetos caso a cláusula negação do OU for verdadeira, ou seja, não pode encontrar nenhuma cláusula verdadeira.**

### `$and`

`db.foo.insert( { a: [ 1, 10 ] } ) db.foo.find( { $and: [ { a: 1 }, { a: { $gt: 5 } } ] } )`
 **Retorna objetos caso a cláusula E for verdadeira.**

---

### Dúvida no fórum sobre esses Operadores lógicos

#### [Dúvida Fórum](http://aprenda.dagora.net/discussao/18/1/duvida-query/)
---

## Operadores "Existênciais"

### `$exists`

### `$exists db.collection.find( { campo : { $exists : true } } )`
- Retorna o objeto caso o campo exista.


## Exercício da Aula
### [Exercício](https://github.com/Webschool-io/be-mean-instagram/blob/master/apostila/classes/mongodb/class-03-resolved.md)
### [Exercício Resolvido](https://github.com/TiagoWinehouse/be-mean-instagram-mongodb/blob/master/exercises/class-03-resolved-tiagowinehouse.md)

---


Faculdade EAD [WebSchool-io](https://github.com/Webschool-io)
