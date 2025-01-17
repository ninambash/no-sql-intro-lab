![General Assembly Logo](https://camo.githubusercontent.com/1a91b05b8f4d44b5bbfb83abac2b0996d8e26c92/687474703a2f2f692e696d6775722e636f6d2f6b6538555354712e706e67)

# NoSQL Research Lab

## Explainer

Up until now in the cohort we have stored data only in what are known as relational databases (SQL is the most well known type of relational DB querying language). Relational databases structure our data into tables. Today we will learn about a different type of database: a non-relational one.

## Lab

In this lab you will be researching, either individually or in groups, answer to the following questions about noSQL databases. The intention is for you to spend some time learning about the fundamental differences between the type of databases we have seen before and the new type we will be learning about today. Even more importantly, you will learn about why two types of databases are used, and what situations fit each type of db.

## Setup

Fork and clone this repository and answer questions as you research directly in the README. You do not have to submit this lab, but you will want to have it on hand for reference in the future.

## Questions:

1. What does the term noSQL refer to, and what other term is often used synonymously with noSQL?

NoSQL stands for "not only SQL" and refers to a type of database management system (DBMS) that does not use a fixed schema and does not rely on the relational model. These databases are often used for big data and real-time web applications. The term "non-relational" is often used synonymously with NoSQL.

NoSQL stands for "not only SQL" and refers to a type of database that does not use a fixed schema and does not rely on SQL for querying data. These databases are often used for big data and real-time web applications. The term "non-relational" is often used synonymously with NoSQL to describe these types of databases.

NoSQL refers to a type of database management system that does not use a fixed schema and is not based on the relational model. The data is typically stored in a non-tabular format, such as a document, key-value, graph, or object store.
NoSQL databases are often used to store and manage large amounts of unstructured or semi-structured data, and are designed to scale horizontally.
The term "non-relational" is often used synonymously with NoSQL.

2.  In this class we will be using the document style of non-relational databases. What are the charecteristics of a document based db?

    A document-based NoSQL database uses a document data model, which stores data in semi-structured formats, such as JSON or XML. Each document typically contains a set of fields, and each field has a name and a value. The documents are stored in a collection, which is similar to a table in a relational database. Some of the main characteristics of a document-based database include:

    Flexible schema: Each document can have a different set of fields and structure, which allows for easy evolution of the data model over time.

    Strong consistency: All the data of a document is stored together, which allows for strict consistency model and easy querying of the data.

    High scalability: They can handle large amounts of unstructured data and are designed to scale horizontally. --also called horizontal
    scaling.

    Rich query capabilities: Document databases often have built-in support for rich querying and indexing, which allows for efficient retrieval of data based on various criteria.

    High performance: Document databases are optimized for high-performance read and write operations, which makes them well-suited for use cases such as online transaction processing and real-time analytics.

    2---------------
    A document-based database, also known as a document store or document-oriented database, is a type of NoSQL database that stores data in the form of documents, typically represented in a format such as JSON or BSON. Some characteristics of a document-based database include:

          Schema-less: A document-based database does not have a fixed schema, which means that the structure of the data can vary from document to document. This makes it easy to add new fields or change the structure of the data without having to update the schema.

          Self-contained: Each document in a document-based database contains all the information about that particular piece of data, including any related data. This makes it easy to retrieve and update data without having to perform joins across multiple tables.

          Strong Consistency: Document-based databases are strong consistent in nature. Each document is atomic and will always be in a consistent state.

          Easily Scalable: Document-based databases are easily scalable, as they are typically designed to scale horizontally by distributing the data across multiple servers.

          Good for unstructured data: Document-based databases are well suited for storing unstructured or semi-structured data, such as text, images, and multimedia.

3.  In this class we will be using Mongo specificially as our no-SQL db. Look into Mongo and answer this question: what is the priamry difference between how Mongo is maintained vs SQL?

    MongoDB is a popular document-based NoSQL database management system. The primary difference between MongoDB and SQL databases is in the way they handle data and maintain consistency.

    Data model: MongoDB uses a document-based data model, which means that data is stored in a format similar to JSON or BSON. This makes it easy to store and query unstructured and semi-structured data. In contrast, SQL databases use a table-based data model, where data is stored in a series of rows and columns.

    Schema: MongoDB is a schema-less database, which means that it does not enforce a fixed schema on the data. This allows for more flexibility in how data is stored, but also means that it may be more difficult to enforce data consistency across documents. SQL databases, on the other hand, have a fixed schema, which makes it easier to enforce data consistency, but also means that it can be more difficult to add new fields or change the structure of the data.

    Consistency: MongoDB uses a concept called "eventual consistency" which means that all copies of the data will eventually be consistent with each other, but there may be a delay before all copies are updated. SQL databases, on the other hand, use a concept called "strong consistency" which means that all copies of the data are updated immediately and are always in a consistent state.

    Scale: MongoDB is designed to scale horizontally, which means that it can easily handle large amounts of data by distributing it across multiple servers. SQL databases, on the other hand, are more limited in how they can scale, and may require more complex solutions such as sharding or partitioning to handle large amounts of data.

    Query Language: MongoDB uses its own query language called the MongoDB Query Language (MQL) which is different from SQL. It's also has an API interface to interact with the MongoDB databases.

---

    MongoDB is a popular open-source document-based database that is often used as a NoSQL alternative to traditional SQL databases. The primary difference between how MongoDB is maintained versus SQL databases is in the way data is stored and queried.

    Data storage: MongoDB stores data in the form of documents, which are similar to JSON or BSON format. Each document contains all the information about a particular piece of data, including any related data. This makes it easy to retrieve and update data without having to perform joins across multiple tables. On the other hand, SQL databases store data in tables with predefined schema, data is stored in row-column format.

    Data querying: MongoDB uses a query language called MongoDB Query Language (MQL) for querying the data. MQL is designed to be similar to JavaScript and is optimized for querying document-based data. SQL databases, on the other hand, use Structured Query Language (SQL) for querying the data, which is designed to work with relational data.

    Scaling: MongoDB is built to be horizontally scalable, which means that it can easily scale by adding more servers to the cluster. This allows MongoDB to handle large amounts of data and high levels of concurrency. SQL databases can also scale horizontally, but the process is more complex and requires more expertise.

    Performance: MongoDB is generally faster than SQL databases for read-heavy workloads, as it does not require joins or complex relationships between tables. MongoDB also supports indexing for faster queries, but its write performance is not as good as SQL databases.

    Data Consistency: MongoDB supports both Eventual and Strong consistency, unlike SQL databases which are ACID compliant and supports only strong consistency.

    In summary, MongoDB is a document-based database that is optimized for storing and querying unstructured or semi-structured data, and is designed to scale horizontally. It uses a different query language and data storage format than SQL databases and is generally faster for read-heavy workloads.

---

4.  Mongo DBs are organized into documents. Describe an example of a table in SQL that contains users, and then describe the equivalent DB setup in Mongo.

          In SQL, a table for storing users might have the following columns:

          id (integer, primary key)
          username (string)
          email (string)
          password (string)
          created_at (datetime)
          In MongoDB, the equivalent setup would be a collection called "users" with documents that have the following fields:

          _id (ObjectId)
          username (string)
          email (string)
          password (string)
          created_at (date)
          Note that in MongoDB, the primary key is automatically added as the _id field, which is of the BSON type ObjectId, and the date type is date.

5.  What is an example situation where a non-relational database makes more sense versus a relational db?

    A non-relational database, such as MongoDB, is often a better choice when the data structure is highly nested, or when there are many one-to-many relationships between entities.

    For example, consider an application that deals with a large number of sensor data. Each sensor can generate many different types of data, and each type of data may have different properties. In this case, it would be difficult to model the data in a relational database because of the many-to-many relationships between sensors, types of data, and properties. Instead, a non-relational database like MongoDB would be a better choice because it allows for flexible, nested data structures, making it easier to store and query the data.

    Another example is a real-time analytics system that needs to handle a high volume of data and perform complex queries on it. Non-relational databases, such as Apache Cassandra, can handle such high-scale writes, high availability and perform fast queries without any joins as it is distributed in nature.

    In summary, when the data structure is highly nested and/or when there are many one-to-many relationships between entities, a non-relational database makes more sense as it allows to store and query the data in a more flexible and efficient way.

6.  A non-relational database, such as MongoDB, is often a better choice when the data structure is highly nested, or when there are many one-to-many relationships between entities.

    For example, consider an application that deals with a large number of sensor data. Each sensor can generate many different types of data, and each type of data may have different properties. In this case, it would be difficult to model the data in a relational database because of the many-to-many relationships between sensors, types of data, and properties. Instead, a non-relational database like MongoDB would be a better choice because it allows for flexible, nested data structures, making it easier to store and query the data.

    Another example is a real-time analytics system that needs to handle a high volume of data and perform complex queries on it. Non-relational databases, such as Apache Cassandra, can handle such high-scale writes, high availability and perform fast queries without any joins as it is distributed in nature.

    In summary, when the data structure is highly nested and/or when there are many one-to-many relationships between entities, a non-relational database makes more sense as it allows to store and query the data in a more flexible and efficient way.

What are the benefits of SQL databases? NoSQL Databases?
SQL databases, also known as relational databases, have several benefits:

      They use a structured query language (SQL) which makes it easy for users to access and manipulate data in a consistent and efficient manner.
      They have a well-defined schema, which means that the structure of the data is fixed and known in advance.
      They support transactions, which allow multiple operations to be grouped together and treated as a single unit of work.
      NoSQL databases, on the other hand, have the following benefits:

      They are designed to handle large amounts of unstructured and semi-structured data.
      They can scale horizontally, meaning they can easily handle a large number of concurrent users and a large amount of data by adding more machines to the system.
      They often have more flexible data models, which can make it easier to handle changes to the structure of the data over time.
      They often have better performance and lower latency than SQL databases for certain types of workloads.

      ------------------------------------------------------------------------
      Well-established and widely-used, with a large number of tools and resources available for managing and querying data
      Strong support for data integrity and consistency, with features such as primary keys, foreign keys, and transactions to ensure data is accurate and consistent
      Support for complex queries, making it easy to retrieve and manipulate large amounts of data
      NoSQL databases, on the other hand, have the following benefits:

      Designed to handle large amounts of unstructured or semi-structured data, making them well-suited for big data and other types of data that don't fit well into a traditional relational model
      Scales horizontally, meaning that you can easily add more servers to a NoSQL database cluster to increase capacity and performance
      Typically have lower latency than SQL databases, making them well-suited for real-time, high-performance applications
      Flexible schema, you can add fields or sub-documents without affecting existing data or the application using it.

--------------------------------------------------------------------------------------------------------------------------------

    SQL databases, also known as relational databases, have several benefits including:

        Structured data storage: Data is stored in organized tables with defined columns and relationships, making it easy to query and retrieve specific information.

        Data Integrity: SQL databases enforce data integrity constraints, such as primary and foreign keys, to maintain the accuracy and consistency of the data.

        Scalability: SQL databases can handle large amounts of data and support horizontal scaling by adding more machines to a database cluster.

        Concurrent Access: SQL databases support concurrent access, allowing multiple users to access and update the database at the same time without conflicts.

  NoSQL databases, on the other hand, have several benefits including:

        Flexible data storage: NoSQL databases do not enforce a strict schema, allowing for more flexible and dynamic data storage.

        High scalability: NoSQL databases are designed to handle high levels of read and write operations and can easily scale horizontally by adding more machines to a cluster.

        High performance: NoSQL databases are optimized for high-speed data access, making them well-suited for large-scale, high-traffic applications.

        Handling unstructured data: NoSQL databases are better at handling unstructured or semi-structured data, such as JSON documents, images, and videos.

7.  Explain the differences between ACID and BASE models.

        ACID and BASE are two different models that describe how a database system should behave.

        ACID stands for Atomicity, Consistency, Isolation, and Durability. It is a set of properties that guarantee that a database transaction is processed reliably.

        Atomicity: A transaction is an atomic unit of work, it is either completed in its entirety or not at all.
        Consistency: A transaction brings the database from one valid state to another, meaning that the database is always in a consistent state after a transaction.
        Isolation: A transaction is isolated from other transactions, meaning that the changes made by one transaction are not visible to other transactions until the current transaction is committed.
        Durability: Once a transaction is committed, its effects are permanent and survive any subsequent failures.
        BASE, on the other hand, stands for Basically Available, Soft-State, Eventually Consistent. It is a model that prioritizes high availability and scalability over consistency.

        Basically Available: The system is always available to serve requests, even if it means returning stale or inconsistent data.
        Soft-State: The state of the system may change over time, even without input.
        Eventually Consistent: The system will eventually reach a consistent state, but it may take some time.
        In summary, the ACID model prioritizes consistency, while the BASE model prioritizes availability and scalability. ACID-compliant databases are often used for transactional systems where data consistency is critical, such as financial systems, while BASE-compliant databases are often used for systems that need to scale horizontally and handle high-throughput, such as real-time analytics systems.

## Visual Comparisons

### Structure

![](https://media.git.generalassemb.ly/user/16103/files/65db7f00-afd5-11ea-926a-e51b2fd2be08)

### Relationships

![](https://media.git.generalassemb.ly/user/16103/files/5eb47100-afd5-11ea-8cae-0a65c924be4b)

### Use Cases

![](https://media.git.generalassemb.ly/user/16103/files/7f7cc680-afd5-11ea-82c8-10ed74ee2222)

## Additional Readings

Pick an additional reading to go through with a classmate. Reflect on how the
article changes the discussion. What have you learned?

_**Note:** You do not have to read about the different types of SQL and NoSQL. We will use PostgreSQL and MongoDB in this course._

- [ACID vs. BASE Explained](https://neo4j.com/blog/acid-vs-base-consistency-models-explained/)
- [PostgreSQL Use Cases](https://www.cybertec-postgresql.com/en/postgresql-overview/solutions-who-uses-postgresql/)
- [MongoDB Use Cases](https://www.mongodb.com/use-cases)
- [What the heck are you actually using NoSQL for?](http://highscalability.com/blog/2010/12/6/what-the-heck-are-you-actually-using-nosql-for.html)
- [A co-Relational Model of Data for Large Shared Data Banks](http://queue.acm.org/detail.cfm?id=1961297&repost)
- [A brief history of databases](http://avant.org/media/history-of-databases)
- [NoSQL Databases: An Overview | ThoughtWorks](http://www.thoughtworks.com/insights/blog/nosql-databases-overview)
- [When to choose CouchDB vs RDBMS?](http://stackoverflow.com/a/2731207/402618)
- [CAP Twelve Years Later: How the "Rules" Have Changed](http://www.infoq.com/articles/cap-twelve-years-later-how-the-rules-have-changed)
