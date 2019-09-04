#SQL day 2 (aka sqewl, aka skl)

- Student can add foreign key to new table
- Student can add foreign key to existing table
- Student can use join
- Student can use sub-selects/nested queries
- Student can set null values
- Student can Group by
- Student can update rows
- Student can delete rows
- Student can use distinct
- Student can describe one-to-one relationships
- Student can describe one-to-many relationships
- Student can describe many-to-many relationships

### **First Normal form:**

a relation is in first normal form if and only if the data ion each column is indivisible.

- good data:

  - string
  - number/ integer
  - boolean
  - null
  - float

* avoid:

  - objects
  - arrays

### **Second normal form:**

- A relation is in second normal form if it is in 1NF and every non key attribute is fully functionally dependent on the primary key.
- needs to be in first normal form, table must have a primary key and all non primary key column's are dependents of the primary key.

### data types:

- null

- integer => round number
- decimal => unlimited decimal places
- float => 15 decimal places
- serial => incrementing integer usually used for primary key

- text => unlimited characters
- varchar(n) => default to 64

### **Third normal form**

- third noraml form is the third step in normalizing a database and it builds on the first and second forms.
- third normal form states that all column reference in referenced data that are not dependent on the primary key should be removed.
- must be in second normal form.
- contains only columns that are non transitively-dependent on a primary key.

  - transitive: A is greater than B, and B is greater thn C then it would make sense that A is greater than C.

  A, B, Primary-Key, if the value of A relies on the PK, and B relies on the PK and A also relies on B then you can say that A relies on the PK through B.

  ```sql
    personId, firstName, lastName => non transitively dependant.

    personId, bodyMassIndex, isObese =>transitively dependant.
  ```

  **one to one relationship**

  - in a one to one relationship, on recor in a table is associated with one and only one record in another file. for example, In a school database, each student has only one student ID, and each student ID is assigned to only one person.
  - one column in a table is associated with one and only one column from another table.

  <img width='500px' src='https://upload.wikimedia.org/wikipedia/commons/thumb/f/f7/CPT-Databases-OnetoOne.svg/500px-CPT-Databases-OnetoOne.svg.png'>

  **one to many realationships**

  -one column in a table can be associated with one or more columns in another table.

  <img width='500px' src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/d7/CPT-Databases-OnetoMany2.svg/500px-CPT-Databases-OnetoMany2.svg.png">

**Many to Many**

- multiple columns in a table can be associated with multiplecolumns from another table.

<img width='500px' src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c4/CPT-Databases-ManytoMany.svg/500px-CPT-Databases-ManytoMany.svg.png">

<img width='500px' src="https://upload.wikimedia.org/wikipedia/commons/0/02/Databases-ManyToManyWJunction.jpg">
