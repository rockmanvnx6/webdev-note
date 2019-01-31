# Mongodb

To launch mongodb terminal

```bash
mongo
```

> It's like javascript, you can create function, variable, object, json like javascript

**Example**

```javascript
var usr = {
    "name" : "thang",
    "age": 30,
    "email": "test@gmail.com"
}
```





## To use a database / create a database

```javascript
use database_name
```

## To show database

```mongo
show dbs
```



## To insert an item into the database

```mongo
db.database_name.insert(variablename)
```

**Example**

```mongodb
db.test_1.insert(usr)
```



## To see what item in the database

```mongo
db.database_name.find()
```

or

```mongo
db.database_name.find().pretty()
```

to print the pretty form.





## To update the database:

first update the variable name first. 

```mongo
usr.name = "rockmanvnx6"
```

and then to update.

```mongodb
db.database_name.update({"name": "thang"}, usr)
```

update usr base on the find.

or just updating itself:

```mongo
db.database_name.update({}, usr)
```



## To remove an entry in the database

```mongodb
db.test_1.remove({"name" : "thang pham"})
```





## To remove a key in json element

```mongo
delete usr.array
```



## JS to connect with the database:

```js
var selectDB = function(port, dbName) {
    if(!port) {
        port = 27017;
    }

    if(!dbName) {
        dbName = "test_1"
    }

    db = connect("localhost:" + port + "/" + dbName);

    return db;
}
```



Then in the same folder as the js file

```bash
mongo
> load('test.js')
> selectDB()
```



# Create collection

```mongo
db.createCollection(<name>)
```

Collection is basically a sub folder of database.

## Show collection

```mongo
show collections
```

## To view a collection database

```mongo
db.collection_name.find().pretty()
```



## To delete the collection

```mongo
db.collection_name.drop()
```

