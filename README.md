# 🏁 1. Start MongoDB Shell

Open your terminal and run:

```bash
mongosh
```

You will now see the MongoDB shell prompt:

```
>
```

---

# 🗄️ A) Create & Drop Database

## ⭐ Create a Database

Use the `use` command:

```javascript
use collegeDB
```

If the database does not exist, MongoDB will create it when you insert data.

---

## 🗑️ Drop a Database

Switch to the database you want to remove:

```javascript
use collegeDB
```

Then drop it:

```javascript
db.dropDatabase()
```

**Output:**

```
{ ok: 1 }
```

---

# 📁 B) Create & Drop Collection

## ⭐ Create a Collection

```javascript
db.createCollection("students")
```

---

## 🗑️ Drop a Collection

```javascript
db.students.drop()
```

**Output:**

```
true
```

---

# ✍️ C) Insert Documents (Insert One & Insert Many)

## 1️⃣ Insert One Document

```javascript
db.students.insertOne({
  name: "Prasad",
  age: 20,
  course: "Full Stack"
})
```

---

## 2️⃣ Insert Many Documents

```javascript
db.students.insertMany([
  { name: "Sakshi", age: 19, course: "Data Science" },
  { name: "Rohit", age: 21, course: "AI & ML" },
  { name: "Varun", age: 22, course: "Cyber Security" }
])
```

---

# ❌ D) Delete Documents (Delete One & Delete Many)

## 1️⃣ Delete One Document

```javascript
db.students.deleteOne({ name: "Prasad" })
```

---

## 2️⃣ Delete Many Documents

```javascript
db.students.deleteMany({ age: { $gt: 20 } })
```

This will delete all students whose age is greater than **20**.

---

# 🔍 Example: View All Documents

```javascript
db.students.find()
```

---

# 📘 Summary of Commands

| Operation         | Command                           |
| ----------------- | --------------------------------- |
| Create DB         | `use dbName`                      |
| Drop DB           | `db.dropDatabase()`               |
| Create Collection | `db.createCollection("name")`     |
| Drop Collection   | `db.collection.drop()`            |
| Insert One        | `db.collection.insertOne({...})`  |
| Insert Many       | `db.collection.insertMany([...])` |
| Delete One        | `db.collection.deleteOne({...})`  |
| Delete Many       | `db.collection.deleteMany({...})` |
| View Data         | `db.collection.find()`            |

---
