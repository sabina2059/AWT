***SQL(SQLITE) and NOSQL(MongoDB)***
-----
**SQL(SQLLITE)**

1. Stores data in tables with rows and columns.
2. Structured schema with predefined tables and types.
3. Stores data in a single file on disk.

**EXAMPLE**


```
CREATE TABLE users (
  id INTEGER PRIMARY KEY,
  name TEXT,
  age INTEGER
);
```

***MONGODB***

1. Stores data in JSON-like BSON documents.
2. Flexible schema, fields can vary between documents.
3.  Uses BSON-based query syntax
   
   **EXAMPLE**

   ```
   {
  "_id": ObjectId("..."),
  "name": "Alice",
  "age": 25
}
```
-------

**Prisma**

Prisma is a modern ORM (Object-Relational Mapping) tool for Node.js and TypeScript.

- It acts like a bridge between our code and our database, making it easier to read/write data. That means it simplifies database interaction.

**Without Prisma, we have to:**

- Write raw SQL queries manually
- Handle database connections yourself
- Deal with inconsistent data manually
  
**With Prisma, we can:**

- Use JavaScript/TypeScript code to interact with our database
- ensure type safety, autocompletion, and easy migrations
  
  **Working with prisma**

  Before starting working with prisma, I installed Prisma CLI and Client
```
npm install prisma --save-dev 

npm install @prisma/client
```

I added the Prisma CLI as a dev dependency (--save-dev) because it’s only needed during development and build time, not in the production environment. The @prisma/client package is a runtime dependency used by the application to query the database.

1. I defined schema/ database structure in a `schema.prisma` file.

for example:
```
model User {
  id    Int     @id @default(autoincrement())
  name  String
  email String  @unique
}
```
2. I configured the database connection by setting the DATABASE_URL in the .env file, telling Prisma where my database is located.

3. I ran Prisma migrations to create the database and tables based on the schema: `npx prisma migrate dev` then named migration

**How it simplified my work**

- I only needed to define my data models once in the schema.prisma file. Prisma took care of translating that into database tables.
  
- Instead of writing SQL migration scripts manually, Prisma generates and applies them automatically, saving time and reducing errors.
  
---
   **ROUTING**

Directs incoming requests to specific functions or controllers in a web app.

```
app.get('/home', (req, res) => res.send('Welcome Home'));
```
---
**ORM (Object Relational Mapping)**

Allows you to interact with a database using object-oriented code instead of SQL.

```
class User(Base):
    __tablename__ = 'users'
    id = Column(Integer, primary_key=True)
    name = Column(String)

```
---
**Middleware**

Functions that process requests before they reach the final route handler.

```
app.use((req, res, next) => {
  console.log('Request received');
  next();
});
```
---
**JSON (JavaScript Object Notation)**

Lightweight data format used for data exchange between client and server.

```
json
Copy
Edit
{ "name": "Alice", "age": 30 }
```
---
**API (Application Programming Interface)**

A set of endpoints that allows communication between software components.

```
Copy
Edit
GET /api/users
```
---
**Git Basics**

Version control system to track code changes and collaborate.

```
bash
Copy
Edit
git init          # Initialize a repo
git add .         # Stage changes
git commit -m "msg"  # Save changes
git push          # Upload to remote
```

