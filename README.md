# CREATE A TABLE
CREATE TABLE IF NOT EXISTS people(
    id INTEGER PRIMARY KEY,
    name TEXT,
    age INTEGER,
    gender TEXT,
    description TEXT
);

# Inspect Table
.table
.schema

# INSERTING DATA INTO TABLE
INSERT INTO people(name, age, gender, description)
VALUES('wafula', 30, 'M', 'tall with a tattoo on left arm')

INSERT INTO people(name, age, gender, description)
VALUES('Jayden', 60, 'M', 'has a pot belly')

INSERT INTO people(name, age, gender, description)
VALUES('Shiru', 25, 'F', 'has yellow braids')

INSERT INTO people(name, age, gender, description)
VALUES('Ann', 37, 'F', 'wears black glasses')

INSERT INTO people(name, age, gender, description)
VALUES('Nyamwalo', 19, 'F', 'very beautiful')

INSERT INTO people(name, age, gender, description)
VALUES('Omondi', 23, 'M', 'Heavily Built with long beard')

INSERT INTO people(name, age, gender, description)
VALUES('Kipkirui', 45, 'M', 'Bald head')

INSERT INTO people(name, age, gender, description)
VALUES('Silikhe', 27, 'M', 'Has Long healthy dreadlocks')

# UPDATING EXISTING DATA IN A TABLE
UPDATE TABLE reports
SET statement = "I was chilling under the Old Mugumo tree and I saw a man looking suspiciuos."
WHERE name = "Kamau"

# QUERIES

Start by reading the reports...
SELECT * FROM reports;

Inspect the people table..
SELECT * FROM people;

DELETE FROM people
WHERE id = XX;

Filter by Gender : We know it's a man.
SELECT * FROM people
WHERE gender = 'M';

Determmine the number of suspects?
SELECT COUNT(*) FROM people
WHERE gender = 'M';

Filter by age : We know the age is between 20 & 30
SELECT * FROM people
WHERE age BETWEEN 20 AND 30;

Chaining the 2 conditions
SELECT * FROM people
WHERE gender = 'M' AND age BETWEEN 20 AND 30

Filter by description.
SELECT * FROM people
WHERE gender = 'M' AND age BETWEEN 20 AND 30 AND description LIKE '%beard%'

Case Solved!

# drop table
DROP TABLE people;