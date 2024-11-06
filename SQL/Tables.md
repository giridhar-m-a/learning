
## Creating A Table

- syntax to create a table

```sql

CREATE TABLE <name>(
	<COLUMN NAME> <DATA TYPE>
)

```

###### Example:

```sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  username VARCHAR(50)
);

-- Table with foreign key reference tu users table 

CREATE TABLE photos (
	id SERIAL PRIMARY KEY,
	url VARCHAR(200),
	user_id INTEGER REFERENCES users(id) -- Foreign Key
);
```

### Primary Key
- Primary key has to be an unique value
- It is used to identify the row inside a table
- Either an integer or a UUID
### Foreign Key
- It is used to relate another table 
- Rows only have this if they belong to another record
- Many rows in the same table can have the same foreign key
- exactly equal to the primary key to the referenced row
- Will change if the relationship changes

## Insert Data Into A Table

- syntax to insert data into the table
```sql

INSERT INTO <TABLE NAME>(<COLUMN NAMES>) VALUES(<VALUES FOR THE COLUMNS IN SAME ORDER AS THE COLUMN NAMES>);

-- note : for string values use single quotes
```


## Retrieve Data

- Syntax to retrieve data
```sql
-- to get all the columns

SELECT * FROM <TABLE NAME>;

--to get selected columns

SELECT <COLUMN NAME> FROM <TABLE NAME>

```


### Data Consistency

##### Insertion:

	 Scenario 1:
		 if the referance value doesn't exist it will throw an error
	Scenario 2:
		If the foreign key is null 
	Scenario 3:
		Everything worked fine

##### Deletion

		Scenario 1:
			Deleting an record which is associated with an reference
				ON DELETE RESTRICT : throws error
				ON DELETE NO ACTION : throws error
				ON DELETE CASCADE : delete derated row
				ON DELETE SETNULL : set the reference value to null
				ON DELETE SET DEFAULT : set the value to default if value is provided
		Scenario 2:
			