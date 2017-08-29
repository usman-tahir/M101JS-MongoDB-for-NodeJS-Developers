# M101JS
## JSON Quiz
Which of the following value types are defined by the JSON spec? Check all that apply

[x] object

[x] array

[ ] date

[x] string

[ ] integer

[x] number

## BSON Quiz
Mongo stores data as BSON. Mongo drivers map BSON to native data types for any programming language.
Json data types are limited. Json can't differentiate between floating and number and Json stores dates as strings. Bson can. Bson extends data type capabilities.

True or False? BSON plays the role of a canonical (i.e. "unique") representation of documents shared across all drivers and tools.
[x] True
[ ] False

## CRUD Operation Concepts
Create, Read, Update, or Delete.

### Commands

`./mongod` to start the mongo db

`./mongo` to enter the mongo db shell

`show dbs` show current databases

`help` display help

`video.movies` would show the movies collection in the videos db

`use video` will switch to database or create database if it does not exist in a "lazy" manner

`db.movies.insertOne({"title":"Jaws", "year":1975, "imdb": "tt0073195"})` will create the database and the collection if they do not exist and insert the document. Each document has an unique object id.

`db.movies.insertOne({"title":"Mad Max 2: The Road Warrior", "year":1981, "imdb": "tt0082694"})` additional doc

`db.movies.insertOne({"title":"Raiders of the Lost Ark", "year":1981, "imdb": "tt0082971"})` additional doc

`db.movies.find().pretty()` OR `db.movies.find({}).pretty()` .find() displays all docs in the movies collection and .pretty() outputs them in a readable format

`db.movies.find({"title":"Jaws"}).pretty()` to query by title

`db.movies.find({"year":1981}).pretty()` to query by year

`var c = db.movies.find()` The MongoDB shell is a fully functional javascript interpertor

We can then iterate via `next()` or `hasNext()`
~~~~
c.hasNext()
=true
~~~~
To grab the document
~~~~
c.next()
~~~~
We should be able to class `next()` three times. Afterwards `hasNext()` will return `false`




