# Finding Documents in a MongoDB

### Find a Document with Equality
When given equality with an _id field, the find() command will return the specified document that matches the _id. Here's an example:

```javascript
db.zips.find({ _id: ObjectId("5c8eccc1caa187d17ca6ed16") })
```

### Find a Document by Using the $in Operator
Use the $in operator to select documents where the value of a field equals any value in the specified array. Here's an example:

```javascript
db.zips.find({ city: { $in: ["PHOENIX", "CHICAGO"] } })
```

## Finding Documents by Using Comparison Operators

Review the following comparison operators: $gt, $lt, $lte, and $gte.

### $gt
Use the $gt operator to match documents with a field greater than the given value. For example:

```javascript

db.sales.find({ "items.price": { $gt: 50}})

```

### $lt
Use the $lt operator to match documents with a field less than the given value. For example:
```JavaScript
db.sales.find({ "items.price": { $lt: 50}})
```

### $lte
Use the $lte operator to match documents with a field less than or equal to the given value. For example:
```javascript
db.sales.find({ "customer.age": { $lte: 65}})
```

### $gte
Use the $gte operator to match documents with a field greater than or equal to the given value. For example:

```javascript
db.sales.find({ "customer.age": { $gte: 65}})
```
