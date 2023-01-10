In Table 2, Membership_ID is the Foreign Key

![Foreign Key Example](https://www.guru99.com/images/foreign_key_table.png)

![Foreign Key in DBMS](https://www.guru99.com/images/ForeignKey.png)

Foreign Key in DBMS

Foreign Key references the primary key of another Table! It helps connect your Tables

-   A foreign key can have a different name from its primary key
-   It ensures rows in one table have corresponding rows in another
-   Unlike the Primary key, they do not have to be unique. Most often they aren’t
-   Foreign keys can be null even though primary keys can not

![Foreign Key in Database](https://www.guru99.com/images/ForeignKeyRelationWithPrimary.png)

## Why do you need a foreign key?

Suppose, a novice inserts a record in Table B such as

![Why Foreign Key is important in Database](https://www.guru99.com/images/WhyDataBaseIsImportant.png)

You will only be able to insert values into your foreign key that exist in the unique key in the parent table. This helps in referential integrity.

The above problem can be overcome by declaring membership id from Table2 as foreign key of membership id from Table1

Now, if somebody tries to insert a value in the membership id field that does not exist in the parent table, an error will be shown!