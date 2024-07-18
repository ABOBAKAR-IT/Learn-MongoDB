#  Replacing a Document in MongoDB
To replace documents in MongoDB, we use the replaceOne() method. The replaceOne() method takes the following parameters:

- filter: A query that matches the document to replace.

- replacement: The new document to replace the old one with.

- options: An object that specifies options for the update.

In the previous video, we use the _id field to filter the document. In our replacement document, we provide the entire document that should be inserted in its place. Here's the example code from the video:

```javascript

db.books.replaceOne(
  {
    _id: ObjectId("6282afeb441a74a98dbbec4e"),
  },
  {
    title: "Data Science Fundamentals for Python and MongoDB",
    isbn: "1484235967",
    publishedDate: new Date("2018-5-10"),
    thumbnailUrl:
      "https://m.media-amazon.com/images/I/71opmUBc2wL._AC_UY218_.jpg",
    authors: ["David Paper"],
    categories: ["Data Science"],
  }
)

```

