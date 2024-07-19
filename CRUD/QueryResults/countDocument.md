# Counting Documents in a MongoDB Collection
Review the following code, which demonstrates how to count the number of documents that match a query.
### Count Documents
Use `db.collection.countDocuments()` to count the number of documents that match a `query.countDocuments()` takes two parameters: a query document and an options document.

Syntax:

`db.collection.countDocuments( <query>, <options> )`

The query selects the documents to be counted.

Example 1:
```javascript
// Count number of docs in trip collection
db.trips.countDocuments({})
```

Example 2:
```javascript
// Count number of trips over 120 minutes by subscribers
db.trips.countDocuments({ tripduration: { $gt: 120 }, usertype: "Subscriber" })
```