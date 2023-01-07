## 2NF (Second Normal Form) Rules

-   Rule 1- Be in 1NF
-   Rule 2- Single Column Primary Key that does not functionally dependant on any subset of candidate key relation

It is clear that we can’t move forward to make our simple database in 2nd Normalization form unless we partition the table above.

![2NF Example](https://www.guru99.com/images/Table2.png "Table 1")

![2NF Example in DBMS](https://www.guru99.com/images/Table1.png "Table 2")

We have divided our 1NF table into two tables viz. Table 1 and Table2. Table 1 contains member information. Table 2 contains information on movies rented.

We have introduced a new column called Membership_id which is the primary key for table 1. Records can be uniquely identified in Table 1 using membership id



## Fra Halvards forelesninger

### 2NF - Andre Normalform

-   Databasen må være på 1.normalform
-   Deler av ID skal ikke kune være determinantfelt for andre felt, dvs deler av ID skal ikke entydig kunne bestemme verdier i et annet felt.
-   Før 2NF
    -   ![](https://i.imgur.com/EBRwaqS.png)
-   Etter 2NF
    -   ![](https://i.imgur.com/nu0jzQP.png)

Etter andre normalform, så separerer man ting enda mer så man da kan ha en egen tabell for selgere og kan da enkelt oppdatere selgere uten å måtte oppdatere hele tabelle med varer. Og samme med vare, man trenger ikke å oppdatere alt når man får inn en ny vare, men heller bare oppdatere vare nummer og pris og til slutt ha en Tabell som inneholder en identifikator til Selger og vare og da ha en egen tabell for Selger id og vare id og hvor mye mengde de skal ha :)