##MongoDB

https://www.mongodb.com/docs/languages/python/pymongo-arrow-driver/current/quick-start/

$ python -m pip install pymongoarrow

from pymongoarrow.monkey import patch_all

patch_all()

from pymongoarrow.api import Schema

schema = Schema({'_id': int, 'amount': float, 'last_updated': datetime})

df = client.db.data.find_pandas_all({'amount': {'$gt': 0}}, schema=schema)


MongoDB Shell Commands 🍃🌲
Show Database
show dbs
This command will show all the databases in your MongoDB server.

Use Database
use <database_name>
This command will switch to the database you want to use.

Show Collections
show collections
This command will show all the collections in the database you are using.

Drop Database
db.dropDatabase()
This command will drop the database you are using.

Create Collection
db.createCollection("<collection_name>")
This command will create a collection in the database you are using.

Insert a Document
db.<collection_name>.insertOne({
    <key>: <value>,
    <key>: <value>,
    ...
})
This command will insert a document in the collection you are using.

Insert Multiple Documents
db.<collection_name>.insertMany([
    {
        <key>: <value>,
        <key>: <value>,
        ...
    },
    {
        <key>: <value>,
        <key>: <value>,
        ...
    },
    ...
])
This command will insert multiple documents in the collection you are using.

Find Documents
db.<collection_name>.find()
This command will find all the documents in the collection you are using.

Find Documents with Query
db.<collection_name>.find({
    <key>: <value>
})
This command will find all the documents in the collection you are using that match the query.

Count Documents
db.<collection_name>.find({
    <key>: <value>
    }).count()
This command will count all the documents in the collection you are using that match the query.

Limit Documents
db.<collection_name>.find().limit(<number>)
This command will limit the number of documents returned by the find command.

forEach()
db.<collection_name>.find().forEach(function(doc) {
    print("Key: " + doc.<key> + " Value: " + doc.<value>);
})
This command will iterate through all the documents in the collection you are using and print the key and value of each document.

Find One Document
db.<collection_name>.findOne({
    <key>: <value>
})
This command will find the first document in the collection you are using that matches the query.

Update a Document
db.<collection_name>.updateOne({
    <key>: <value>
}, {
    $set: {
        <key>: <value>
    }
})
This command will update the first document in the collection you are using that matches the query. $set is used to update the document.

Increment a Document
db.<collection_name>.updateOne({
    <key>: <value>
}, {
    $inc: {
        <key>: <value>
    }
})
This command will increment the value of the key in the first document in the collection you are using that matches the query. $inc is used to increment the value of the key.

Delete a Document
db.<collection_name>.deleteOne({
    <key>: <value>
})
This command will delete the first document in the collection you are using that matches the query.

Add new field to a Document
db.<collection_name>.updateOne({
    <key>: <value>
}, {
    $set: {
        <new_key>: <new_value>
    }
})
This command will add a new field to the first document in the collection you are using that matches the query.

Greater than
db.<collection_name>.find({
    <key>: {
        $gt: <value>
    }
})
This command will find all the documents in the collection you are using that have a key greater than the value.

Greater than or equal to
db.<collection_name>.find({
    <key>: {
        $gte: <value>
    }
})
This command will find all the documents in the collection you are using that have a key greater than or equal to the value.

Less than
db.<collection_name>.find({
    <key>: {
        $lt: <value>
    }
})
This command will find all the documents in the collection you are using that have a key less than the value.

Less than or equal to
db.<collection_name>.find({
    <key>: {
        $lte: <value>
    }
})
This command will find all the documents in the collection you are using that have a key less than or equal to the value.

Not equal to
db.<collection_name>.find({
    <key>: {
        $ne: <value>
    }
})
This command will find all the documents in the collection you are using that have a key not equal to the value.

And
db.<collection_name>.find({
    $and: [
        {
            <key>: <value>
        },
        {
            <key>: <value>
        }
    ]
})
This command will find all the documents in the collection you are using that match the query.

Or
db.<collection_name>.find({
    $or: [
        {
            <key>: <value>
        },
        {
            <key>: <value>
        }
    ]
})
This command will find all the documents in the collection you are using that match the query.

Sort
db.<collection_name>.find().sort({
    <key>: <value>
})
This command will sort all the documents in the collection you are using by the key.

Sort Descending
db.<collection_name>.find().sort({
    <key>: -1
})
This command will sort all the documents in the collection you are using by the key in descending order.

Drop Collection
db.<collection_name>.drop()
This command will drop the collection you are using.
