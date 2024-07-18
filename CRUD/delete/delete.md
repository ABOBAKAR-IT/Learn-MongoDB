# Deleting Documents in MongoDB
To delete documents, use the deleteOne() or deleteMany() methods. Both methods accept a filter document and an options object.
### Delete One Document
The following code shows an example of the deleteOne() method:
```javascript
db.podcasts.deleteOne({ _id: Objectid("6282c9862acb966e76bbf20a") })y
```

### Delete Many Documents
The following code shows an example of the deleteMany() method:
```javascript
db.podcasts.deleteMany({category: “crime”})
```