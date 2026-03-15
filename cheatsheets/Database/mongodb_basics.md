# MongoDB Basics (NoSQL)

## CRUD Operations
- `db.collection.insertOne({ ... })`
- `db.collection.find({ ... })`
- `db.collection.updateOne({ filter }, { $set: { ... } })`
- `db.collection.deleteOne({ ... })`

## Operators
- `$gt`, `$gte`, `$lt`, `$lte`: Comparison.
- `$in`, `$nin`: Value in/not in array.
- `$or`, `$and`: Logical operators.
- `$set`, `$unset`: Modifying fields.
- `$push`, `$pull`: Modifying arrays.

## Indexes
- `db.collection.createIndex({ field: 1 })`: Ascending index.
- `db.collection.createIndex({ field: -1 })`: Descending index.

## Mongoose (ODM)
```javascript
const userSchema = new mongoose.Schema({
  name: String,
  email: { type: String, required: true, unique: true }
});

const User = mongoose.model('User', userSchema);
```
