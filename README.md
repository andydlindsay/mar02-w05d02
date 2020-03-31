# W5D2 - Database Design

### To Do
- [ ] Primary Keys/Foreign Keys
- [ ] Data Types
- [ ] Relationship Types
- [ ] Naming Conventions
- [ ] Normalization
- [ ] Design Concepts
- [ ] Entity Relationship Diagrams
- [ ] ERD #1: Convert 2 Spreadsheets
- [ ] ERD #2: Student Suggestion(s)

### Primary Key/Foreign Keys
- A PK is a way of uniquely identifying a particular record in a table
- A PK stored in another table is referred to as a Foreign Key
- Primary Keys should always be auto-incrementing integers
- Opinion: PK should have no info about the record that it identifies
- Composite Keys: two or more fields and turn them into a PK
- The data type of the FK MUST match the data type of the PK

### Data Types
- Choosing the right/correct data type used to be a massive deal
- Memory used to equal $$$$$$
- Memory is cheap
- Money is a big deal, don't store as a floating point
- $5.45 === 545 / 100
- varchar(255), char(255)

### Relationship Types
- One of three ways:
  - One-to-one: one record in the 1st table is related to only one record in the 2nd
  - One-to-many: one record in the 1st table is related to one or more in the 2nd
  - Many-to-many: many records in the 1st are related to many in the 2nd
- 1:1 = almost never get used
- M:M = cannot be represented with two tables (you need another table)

### Naming Conventions (opinion)
- Table names are lowercase and plural (users, assets)
- Field names also lowercase and snake_case (first_name)
- Primary keys should always be `id`
- Foreign keys should always be singular of table name plus `_id` (user_id)

### Normalization
- Is a way of standardizing our data and removing redundant data
- Single source of truth
- Calculated fields: full_name, first_name, last_name
- Beware: you can take normalization too far (too many tables to JOIN)
- SELECT's denormalize the data

### Design Concepts
- Make fields required (and unique)
- Make required based on the initial save state of the record
- Intelligent default values (created_at)
- Never delete anything (DELETE) record retention periods
- `active` boolean (default to true)
- Pull repeated values out to a lookup table (vancouver, vancvoue, vancity, van!)
- Never trust your users
- Consider using a `type` field for tables that have most of the same records

### ERD's
- Entity Relationship Diagrams
- 


















### Useful Links
* [Database Normalization](https://en.wikipedia.org/wiki/Database_normalization)
* [Postgres Data Types](http://www.postgresqltutorial.com/postgresql-data-types/)
* [Relationship Types](http://etutorials.org/SQL/Database+design+for+mere+mortals/Part+II+The+Design+Process/Chapter+10.+Table+Relationships/Types+of+Relationships/)
* [draw.io (online ERD)](https://www.draw.io/)
