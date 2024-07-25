# Using $out Stages in a MongoDB Aggregation Pipeline
Store the aggregation output into a collection
- Writes the documents that are returned by an aggregation pipeline onto a collection
- Must be the last stage
- Creates a new collection if it does not already exist
- If collection exists, $out replaces the existing collection with new data
 
```javascript
$out:{
  db: "<db>",
coll:"<newCollection>"
}
```


example 
```javascript
db.zips.aggregate([
  {
    $group: { _id: "$state", totalPop: { $sum: "$pop" } },
  },
  {
    $out: "states_pop"
  }
]);
```