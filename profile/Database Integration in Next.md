## Next.js Database Integration: A Step-by-Step Complete Guide
    Index : 
    1.  Using MySQL with Next.js (MySQL Integration)
    2.  Using MongoDB with Next.js (MongoDB Integration)
    3.  Using PostgreSQL with Next.js (PostgreSQL Integration)
        https://nextjs.org/learn/dashboard-app/fetching-data
    4.  Using SQLite with Next.js (SQLite Integration)
    5.  Using CockroachDB with Next.js (CockroachDB Integration)
    6.  Using Firebase with Next.js (Firebase Integration)
    7.  Using Cloud Firestore with Next.js (Cloud Firestore Integration)
    8.  Using Oracle Database with Next.js (Oracle Database Integration)

    Note:
    -   MySQL is a relational database management system that uses SQL for data storage and retrieval.
    -   MongoDB is a NoSQL database that stores data in a JSON-like format.
    -   Both MySQL and MongoDB are popular choices for building scalable applications.

#### 1.  Using MySQL with Next.js (MySQL Integration) :-
MySQL is a popular database management system that uses structured query language (SQL) to store and retrieve data.Next.js is a popular front-end framework that uses React to build server-side rendered (SSR) pages.
##### Here are some popular packages for database integration in Next.js:
```bash
-   prisma: A powerful ORM (Object-Relational Mapping) tool that provides a database client for Next.js API routes. It supports MySQL, PostgreSQL, MongoDB and more.
        1.  https://www.dhiwise.com/post/next-js-prisma-mysql-integration-to-boost-your-nextjs-app#configuring-mysql-database-connection
        2.  https://www.prisma.io/docs/getting-started
-   mysql2: A MySQL driver for Next.js API routes that supports Promise, async/await, callbacks, and sync.
        1.  https://datalab.medium.com/nextjs-14-json-api-with-mysql-9f635b5ecb1d
-   next-api-mysql: A MySQL driver for Next.js API routes that supports serverless deployments and supports Promise, async/await, callbacks and sync.

-   serverless-mysql: A MySQL driver for Next.js API routes that supports serverless deployments.
-   next-auth-mysql: A MySQL driver for Next.js API routes that supports serverless deployments and supports Promise, async/await, callbacks and sync.
```
##### To use MySQL with Next.js, you can use the next-api-mysql package.
```bash
- This package provides a MySQL driver for the Next.js API routes that supports serverless deployments and supports Promise, async/await, callbacks and sync, and works well with the Next.js API routes.
- To use the package, you need to install it by running the command npm install --save next-api-mysql.
- Then, you can import the package in your Next.js API route and use the db object to interact with the MySQL database.
- You can also use the package to create a MySQL database connection pool, which can be used to share the database connection across multiple API routes.
- You can also use the package to execute raw SQL queries, execute stored procedures, and more.
- For example, you can create a API route to fetch data from the MySQL database and return it as JSON:

  To connect to a MySQL database in a Next.js API route, you can use the mysql package.
    First, install the package by running the command npm install --save mysql.
    Then, import the package in your API route and use the createConnection method to create a connection to the MySQL database.
    For example, you can use the following code to create a connection to a MySQL database and fetch data from a table:

// Import the mysql package
import mysql from 'mysql';

// Create a connection to the MySQL database
const connection = mysql.createConnection({
  host: 'localhost', // Replace with your database host
  user: 'root', // Replace with your database username
  password: '', // Replace with your database password
  database: 'your_database_name', // Replace with your database name
});

// Connect to the database
connection.connect((err) => {
  if (err) {
    console.error('Error connecting to MySQL:', err.stack);
    return;
  }
  console.log('Connected to MySQL as id', connection.threadId);
});

// Example function to fetch data from a table
export default function handler(req, res) {
  connection.query('SELECT * FROM your_table_name', (error, results) => {
    if (error) throw error;
    res.status(200).json(results);
  });
}
```
    
    
### Reference sources:
1.  https://clouddevs.com/next/mysql-postgresql-sqlite/
2.  https://medium.com/@asishpanda444/next-js-api-connect-to-mysql-database-using-next-js-c020fa17a299
3.  https://www.simplenextjs.com/posts/next-mysql

2.  Using MongoDB with Next.js (MongoDB Integration)
```bash
    -   MongoDB is a popular NoSQL database that uses JSON-like documents to store and retrieve data.
    -   To use MongoDB with Next.js, you can use the next-api-mongodb package.
    -   This package provides a MongoDB driver for the Next.js API routes.
    -   To use the package, you need to install it by running the command npm install --save next-api-mongodb.
    -   Then, you can import the package in your Next.js API route and use the db object to interact with the MongoDB database.

```
