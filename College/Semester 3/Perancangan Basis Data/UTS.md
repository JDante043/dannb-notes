# Database Development Process
## Data Modelling
Research on the information requirements of a business. Ask questions such as "What does this business do" and "What kind of data do they collect?". This part is pure theory /  research. No SQL yet.

## Database Design
Now that you know the information requirements of a business, it is time for you to model the database. What tables to create, attributes for each table, how do they interact with each other, what are the constraints, etc.

This step will eventually produce models that will visualize the database's final form. These models are called ERMs.

## Database Build
This is where you actually build the database. If you're using SQL, this means writing:
- DDL (Data Definition Language) to define tables, such as `CREATE`, `DROP`, and `ALTER`
- DML (Data Manipulation Language) to manipulate data, such as `INSERT`, `UPDATE`, and `DELETE`
- and maybe DCL (Data Control Language) to control access, such as `GRANT`
- and TCL (Transaction Control Language) to make transactions to the database, such as `ROLLBACK`, `COMMIT`, and `SAVEPOINT`

# Entity Relationship Models / ERMs
An ERM is a model that lists all entities and their attributes as well as their relationship to every other entities. Models are "implementation-free", as it does not depend on a single database system. It should be a blueprint that can work for every database implementation, whether they're SQL, noSQL, or literal paper reports stored in a box.

An ERM is frequently vizualised using an Entity Relationship Diagram. Depending on the complexity / detail of the ERM, there are 3 different diagrams / models:

## Conceptual Model
After completing Data Modelling, you will build a conceptual model. As the name suggests, it is a model of what your database would look like in theory. Think of it as a higher level / simpler diagram. It shows the important tables and how they interact with each other (business rules).

<figure>
	<img src="College/Semester 3/Perancangan Basis Data/Resources/Conceptual Model.png">
	<figcaption style="text-align: center;">Conceptual Model example. Notice that it only contains tables, their names, and their relationships (cardinality & optionality included).</figcaption>
</figure>
## Logical Model
You build a logical model from its conceptual model. Every table and their attributes, optional or mandatory, are defined. Each table's optionality and cardinality to each other are clearly stated.

<figure>
	<img src="College/Semester 3/Perancangan Basis Data/Resources/Logical Model.png">
	<figcaption style="text-align: center;">Logical Model example. Notice it builds upon the conceptual model, clarifying every table's attributes. Usually along with the attribute's optionality</figcaption>
</figure>

## Physical Model
This is the implementation of the logical model. A column / attribute's variable name, a table's constraints and their names, every attribute's data type, etc.

Another difference between a physical model with a logical model is that a logical model is "higher-level". People would use logical models in presentations due to its simplicity, whilst engineers would use physical models in development due to containing more information such as data types and actual variable names.

<figure>
	<img src="College/Semester 3/Perancangan Basis Data/Resources/Physical Model.png">
	<figcaption style="text-align: center;">Physical Model example. Notice it builds upon the logical model, adding data types and replacing attribute names with variable names that would be used in the database.</figcaption>
</figure>

# Entity Relationship Diagram / ERD Conventions
A good model must be able to visualize an idea in a simple yet concise manner. In order to visualize an ERM, we draw an ERD. And thus, we need a standardized way to draw ERDs.

## Relationships
- Depending on its optionality, a relationship can be mandatory (straight line) or optional (dotted line).
- A relationship (optionality and cardinality) of a table to another is drawn on the side of the other table
<figure>
	<img src="College/Semester 3/Perancangan Basis Data/Resources/Procedural Business Rule.png">
	<figcaption style="text-align: center;">A diagram made from a procedural business rule.</figcaption>
</figure>
	Note that **some** employee **must** attend some training events. This diagram visualizes those employees who do attend. The straight line means "an employee must attend several training events", while the dotted line means "a training event may be attended by several employees".<br><br>	
	Look at the location as well. A training event must take place in one of the company's locations. The dotted line means "A training event may take place at a location", while the straight line means "a location must host multiple training events"
## Entities
An entity is basically another name for a "table". Just like object oriented programming, an instance (object) is an occurance of an entity (class).
- Represented by softboxes (rounded edges)
- Names are inside softboxes
- Names are always capitalized
- Names are always singular (JOB instead of JOBS, EMPLOYEE instead of EMPLOYEES)

## Attributes
Are basically variables / properties of a class.
- Listed under their entity name, inside the soft box
- Non-volatile attributes are preferred (use date of birth instead of age if possible)
- **UNIQUE** attributes are marked with hashtags, like so: `#Employee ID`
- **Mandatory** attributes are marked with asterisks, like so: `* Full Name`
- **Optional** attributes are marked with circles, like so: `o Commission`
# Business Rules
Business rules are a set of rules that indicate how a company handles data / what the data flow of a company looks like. It can be described in 2 ways,

## Structural Rules
Indicates data types, optionality (attribute & relationships) and cardinality. For example:
- Each teacher **must** have a valid certificate (an attribute is **NOT** optional)
- A class must be taught by **at least one** teacher (a relationship is **NOT** optional)
- A citizen **may** not have a job (an attribute **IS** optional)

## Procedural Rules
Indicates the flow of data. For example:
- **Some** of our employees are **required to attend mandatory** training events. These events **take place at one** of the company’s existing locations, and the employees travel to the location to take part in the training

Would produce an ERD that looks a bit like:
<figure>
	<img src="College/Semester 3/Perancangan Basis Data/Resources/Procedural Business Rule.png">
	<figcaption style="text-align: center;">A diagram made from a procedural business rule.</figcaption>
</figure>

# Supertypes and Subtypes
Imagine a store that accepts either cash or card payments. Both types of transaction would have the same attribute, that is the nominal amount, let's say, $5. But a card transaction would mean writing down the card number and the customer's name, which is not needed for cash transactions.

To solve this, we use supertypes and subtypes. Same concept as super class / base class / inheritance in object oriented programming, a subtype:
- Inherits all of its superclass's attributes
- Inherits all of its superclass's relationships with other entities
- Is never alone (else it would just be a normal instance)
- May have its own subtypes (and would thus be both a subtype of x and a supertype of y)
- Usually has its own attributes.

And, just like object oriented programming, an instance of a superclass means it is an instance of a subtype (exhaustive) and that subtype only (exclusive). For example:

<figure>
	<img src="College/Semester 3/Perancangan Basis Data/Resources/Supertype and Subtype Example.svg">
	<figcaption style="text-align: center;">An example of a supertype with 2 subtypes. A cat is an instance of a land animal, but it is never a fish. And an animal that is not a land animal or a sea animal cannot exist, according to this diagram.</figcaption>
</figure>

# Matrix Diagrams
A matrix diagram is an easy way to see and identify a relationship between instances. Look at the following matrix diagram:

![[Matrix Diagram.png]]

Here, the diagram is read by row:
- "A traveller visits countries and have seen landmarks"
- "A country is visited by travelers and is the location of landmarks"
- "A landmark is seen by travelers and is located in a country>

Make sure to be consistent when writing matrix diagrams to reduce confusion