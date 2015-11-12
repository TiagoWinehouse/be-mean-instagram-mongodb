# MongoDB


## NoSQL

### *Não Relacional*
*Sugestão para estudo*, **[NoSQL - Arquitetura híbrida para uma rede social](http://nomadev.com.br/nosql-arquitetura-h%C3%ADbrida-para-uma-rede-social/)**.

## Principais grupos de NoSql

- Chave/Valor
- Orientado a documento
- Grafos
- Colunas
- Misto

## Conceito MongoDB

- Escrito em C++
- Schemaless ****Não tem esquema***
- Json/Bson
- Replica
- Sharding
- GridFS
- Geolocation
- Terminologia

| SQL RDBMS | MongoDB |
|---------- |----------|
| Database  | Database |
| Table     | Collection |
| Rows      | Document Json |
| Query     | Query  |
| Index     | Index |
| Partition | Shard |


## Iniciando

- *Servidor* `mongod`
- *Cliente*  `mongo`


## Ferramenta

- [Mongo-Hacker](https://github.com/TylerBrock/mongo-hacker)

# MongoExport

-> Exportar dado de uma coleção para um arquivo **Json**.
### Comando

`mongoexport --db nome_do_database --collection nome_da_coleção -- out minha_coleção.json`

# MongoImport

-> Importar dados de um arquivo **Json** para uma coleção.

### Comando

`mongoimport --db database --collection collection --host=127.0.0.1 --drop --file data.json`


# **CUIDADO**

> Evite usar mongoimport e mongoexport para backups de instância de produção. Eles não preservarão de forma confiável todos os tipos de dados ricos do BSON, porque JSON só pode representar um subconjunto dos tipos suportados pelo BSON. Use mongodump e mongorestore como descrito em [MongoDB Backup Methods](https://docs.mongodb.org/manual/core/backups/) para esse tipo de funcionalidade.



# Exercício da Aula
## [Exercício](https://github.com/Webschool-io/be-mean-instagram/blob/master/apostila/mongodb/export_import.md)
## [Exercício Resolvido](https://github.com/TiagoWinehouse/be-mean-instagram-mongodb/blob/master/exercises/mongodb-aula-01-exercicio.md)


Faculdade EAD [WebSchool-io](https://github.com/Webschool-io)
