# MongoDB - Aula sobre a utilização da função update() no MongoDb com seus operadores de modificação e de array. 



## Update()

Para alteração de um documento no *mongodb* existem duas formas:

-	Save
-	Update

No *Update*, ao contrario do save não é preciso fazer uma busca no documento para modifica-lo, ele já faz isso **automaticamente**.

- Recebe 3 parâmetros
	* Query
	* Modificação
	* Options

#### Sintaxe

```javascript
	db.collection.update(query, modificação, options);
    //Options não é obrigatorio!
```

## Operadores de Modificação

### $set

- *Modifica um valor ou cria ele, caso não exista.*

#### Sintaxe

```javascript 
{$set: {campo: valor}}
```
### $unset

- *Remove os campos de um documento.*

#### Sintaxe

```javascript 
{$unset: {campo: 1}} *1 = True
```
### $inc

- *Incrementa um valor no campo com a quantidade desejada. Caso não exista, ele irá criar o campo e setar o valor. Para decrementar, basta passar o valor negativo.*

#### Sintaxe

```javascript 
{$inc: {campo: valor}}
```

### $inc

- *Incrementa um valor no campo com a quantidade desejada. Caso não exista, ele irá criar o campo e setar o valor. Para decrementar, basta passar o valor negativo.*

#### Sintaxe

```javascript 
{$inc: {campo: valor}}
```

## Operadores de array 

### $push

- *Adiciona um valor ao campo, caso o campo seja um *Array* existente. Caso não exista irá criar o campo novo, do tipo *Array* com o valor passado no $push.*

#### Sintaxe 

```javascript 
{$push: {campo: valor}}
```

#### Exemplo

```javascript 
var query = {name: "Gotza"};
var mod = {$push: {moves: 'choque do trovão'}};
db.pokemons.update(query, mod);
```

### pushAll

- *Adiciona cada valor do [Array_de_valores], caso o campo seja um *Array* existente. Caso não exista irá criar o campo novo, do tipo *Array* com o valor passado no $pushAll.*

#### Sintaxe

```javascript 
{$pushAll: {campo: [Array_de_valores]}}
```

#### Exemplo

```javascript 
var attacks = ['choque elétrico', 'ataque rápido', 'bola elétrica'];
var mod = {$pushAll: {moves: attacks}};
db.pokemons.update(query, mod);
```

### pull

- *Retira o valor do campo, caso o campo seja um *Array* existente. Caso não exista irá criar o campo novo, do tipo *Array* com o valor passado no $push.*

#### Sintaxe

```javascript 
{$pull: {campo: valor}}
```

#### Exemplo

```javascript 
var mod = {$pull: {moves: 'bola elétrica'}}
db.pokemons.update(query, { $pull: { moves: 'bola elétrica'} } )
```

### pullAll

- *Retira cada valor do [Array_de_valores], caso o campo seja um *Array* existente. Caso não exista irá criar o campo novo, do tipo *Array* com o valor passado no $pullAll*

#### Sintaxe

```javascript 
{ $pullAll : { campo : [Array_de_valores] } }
```














































