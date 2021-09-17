# SQL
### 17SEP21

---

- 100 Class days left. 
    - Pushing to git dialy. 
    - New repository today for SQL; will be making new repositories about once a week
- Grading
    - Pushing every clas day to github
    - Weekly, will look and see if pushes were made every class day
    - Important, measured for accountability

- Starting to write the same type of code we will likely be using every day in DS career
- SQL most common way to access most stored data in the database world

### VOCABULARY

- **Data Stack:** 
    - Most companies are generating their own data.
        - Website
        - App
        - Manual
- **Database:** location of data stored on a disk somewhere; information held there; sometimes used interchangably with DBMS, but that is the sofrware
- **Client:** Program using to connect to database
    - GUIs common
    - CLIs available also
- **SERVER** computer that runs and stores 
- **Data definition language:** defines structure of database
- **Data Manipulation Language:** Language used to insert, updaet, delete, access information stored in database - where we will be doing most of the interaction
- **DB Management System:**
- **Types of Data stored in SQL server:**
- **How do we use SQL:**
- *****

![Data_Image](data_flow.png)

- Cloud big
    - Amazon
    - Google
    - Azure

## MySQL

- Terminal/Command Line
- GUI
- Main language for most databases
- Couple other options,, but language mostly similar with slight differences

## Table Anatomy

- Similar to Excel 
- **Column Name:**
- **Record:** Single row; all the information about one entry in a table
- **Key:** Unique identifier for each record; each table has a field that must be unique; can be alphaneumeric or string, best practice use a number
- **Field:** Columns
- **Value** information in a cell

- Isn't a way to just look at the whole thing like a spreadsheet; no reason to; resource intensive
- Instead, quety specific values  

- **Table Info** more engineering information, gives create syntax
- **Content** Shows first thousand lines of data - gives you an idea of what is being stored
- **Structure:** Provides additional information about the data type in each column as well as extra info about what is and isn't allowed
- **Triggers** get to later
- **Relations** get to later

- Many databases have a number of tables (i.e., employees)
- Some may be hidden

- Sample initial searches
    - `SELECT * FROM mysql.user;` Command + R to execute (Return)
    - `SELECT * FROM mysql.user;`
    - `SELECT user, host FROM mysql.user;`
    - `SELECT * FROM mysql.help_topic;`
    - `SELECT help_topic_id, help_category_id, url FROM mysql.help_topic;`
- Command R executes the line that the cursor is on

## Curriculum Exercises

- Setup new local and remote repositoty for `database-exercises`
- Save queries as mysql_queries
    - File, save query, pull up dialogue box to save in appropriate path