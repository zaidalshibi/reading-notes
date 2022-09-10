# SQL database, ORM, Sequelize

## Review, Research, and Discussion

### What's the difference between SQL  and NoSQL?

<table>
  <thead>
    <tr>
      <th>SQL</th>
      <th>No-SQL</th>
    </tr>
   </thead>
   <tbody>
     <tr>
       <td>Relational Databases (RDBMS)</td>
       <td>non-relational or distributed database</td>
     </tr>
     <tr>
       <td>table based databases</td>
       <td>document based, key-value pairs, graph databases or wide-column stores</td>
     </tr>
     <tr>
       <td> predefined schema</td>
       <td>dynamic schema for unstructured data</td>
     </tr>
     <tr>
       <td>uses SQL ( structured query language ) for defining and manipulating the data</td>
       <td>queries are focused on collection of documents. Sometimes it is also called as UnQL (Unstructured Query Language). The syntax of using UnQL varies from database to database</td>
     </tr>
  </tbody>
</table>

### What is Sequlize and how to use it with Node js?

- a modern TypeScript and Node.js ORM for Postgres, MySQL, MariaDB, SQLite and SQL Server

```bash
npm install pg sequelize // install 
sqlstart
```

```node.js
const user = '<postgres user>'
const host = 'localhost'
const database = '<postgres db name>'
const password = '<postgres password>'
const port = '<postgres port>'

import { Sequelize, Model, DataTypes } from 'sequelize'

const sequelize = new Sequelize(database, user, password, {
    host,
    port,
    dialect: 'postgres',
    logging: false
})

// example :
const class Dog extends Model {}
Dog.init({
    name: {
        type: DataTypes.STRING,
        allowNull: false
    },
    age: {
        type: DataTypes.INTEGER,
        allowNull: false
    }
    }, {
    sequelize,
    modelName: 'dog',
    timestamps: false
})
```

#### for more info checkout [How to use Sequelize to interact with PostgreSQL](https://flaviocopes.com/sequelize/)

<br/>

### What is an ORM, how does it work, and how should I use one?

- Object-Relational Mapping

> ORM resolves the object code and relational database mismatch with three approaches: bottom up, top-down and meet in the middle. Each approach has its share of benefits and drawbacks. When selecting the best software solution, developers must fully understand the environment and design requirements.
> In addition to the data access technique, ORM's benefits also include:
>
>> Simplified development because it automates object-to-table and table-to-object conversion, resulting in lower development and maintenance costs
>>
>> Less code compared to embedded SQL and handwritten stored procedures
>>
>> Transparent object caching in the application tier, improving system performance
>>
>> An optimized solution making an application faster and easier to maintain
>>
> ORM’s emergence in multiple application development has created disagreement among experts. Key concerns are that ORM does not perform well and that stored procedures might be a better solution. In addition, ORM dependence may result in poorly-designed databases in certain circumstances.

#### for more info checkout [Object-Relational Mapping (ORM)](https://www.techopedia.com/definition/24200/object-relational-mapping--orm)

<br/>

### Document the following Vocabulary Terms

- SQL
- NoSQL
- Database schema
- WRRC

## Preview

### Which 3 things had you heard about previously and now have better clarity on?

- ORM
- Postgresql
- SQL databases

### Which 3 things are you hoping to learn more about in the upcoming lecture/demo?

- ORM
- Postgresql
- SQL databases

### What are you most excited about trying to implement or see how it works?

- Sequelize

## Preparation Materials

- [SQL database](https://www.techtarget.com/searchdatamanagement/definition/SQL)
- [Sequelize](https://sequelize.org/)
- [ORM](https://www.techopedia.com/definition/24200/object-relational-mapping--orm)
- [CRUD system](https://zellwk.com/blog/crud-express-mongodb/)
