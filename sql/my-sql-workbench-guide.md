# MySQLWorkbench

## Resources

1. [MySQL Official Docummentation](https://dev.mysql.com/doc/workbench/en/)
2. [MySQL Official Site](https://www.mysql.com/)
3. [MySQL Forum](https://forums.mysql.com/list.php?152)

## Chapter 1; General Information

- Graphical tool for working with MySQL servers and databases
    - Supports MySQL server v5.6 and higher

- Functionality:
    - ***SQL Delelopment:*** Create and manage connetions to database servers
        - Configure connection parameters
        - Execute queries with built-in SQL Editor
    - ***Data Modeling (Design)*** Create models of your database schema graphically
        - Reverse/forward engineer between schema ans live database
        - Comprehensive Table Editor.
    - ***Server Administration:*** Administer users, perform backup and revocery, inspect audit data, view database health
    - ***Data Migration:*** From Microsofot SQL, Access, Sybase, ASE, SQliet, other RDBMSs
    - ***MySQL Enterprise Support:***

    I am using the free community edition. We will primarily be using the development tools above. (v 8.0.26)

## Chapter 3: Configuration

### 3.2 Workbench Preferences

- Edit Preferences
    - Query editor
        - Code completion
        - Auto UPPERCASE keywords
    - Sql mode

## Chapter 4: Home Screen Tab

- Saved connection information to connect to CodeUp.

## Chapter 8: Database Development

###8 8.1 Visual SQL Editor

- Specialized editors (query, schema, table, etc.)
- Three Panels:
    - Sidebar
    - Secondary Sidebar
    - Output area
- Each editor opens in a separate secondary tab within an active MySQL connection tab.
- Editors and panels enable you to:
    - Build, edit, and run queries
    - Create and edit data
    - View and export results
    - Perform basic admin tasks
- Color syntax highlighting, context help, and code completion assist in writing and debugging SQL statements

- SQL query tab. The SQL query tab is a secondary tab that opens by default when you make a connection to a MySQL server. 
- Each query tab is uniquely identified by an incrementing number: query 1, query 2, and so on. 
- All SQL query tabs provide an area to edit queries. 
- You can open other specialized editors within tabs in this same central area. 
    - For example, you can edit schemas, tables, columns, and so on. 
    - Administration tabs also open in this area.
- Main toolbar. The quick actions in this toolbar are (ordered from left to right):
    - Create a new SQL tab for executing queries
    - Open an SQL script file in a new query tab
    - Open Inspector for the selected object
    - Create a new schema in the connected server
    - Create a new table in the active schema in the connected server
    - Create a new view in the active schema in the connected server
    - Create a new stored procedure in the active schema in the connected server
    - Create a new function in the active schema in the connected server
    - Search table data for text in objects selected in the sidebar schema tree
    - Reconnect to DBMS
- Shortcut actions. Provides the following shortcuts (ordered from left to right):
    - Show preferences dialog (see Section 3.2, “Workbench Preferences”)
    - Hide or show the sidebar panel
    - Hide or show the output area panel
    - Hide or show the secondary sidebar panel
- Sidebar panel. The sidebar has two main labels: 
    - Navigator:
        - `Administration` (previously named Management) 
        - `Schemas` You can merge (or separate) the content of the two tabs into a single list by clicking merge ().
    - Information. (The labels are omitted on some hosts.)
        - Object Info and Session subtabs, which include read-only information about a selected object and about the active connection     
- Secondary sidebar panel (SQL Additions). The SQL Additions area provides the following subtabs:
    - Context Help 
    - Snippets 
- Output area panel. The output panel can display a summary of the executed queries in the following forms: 
    -Action Output
    - Text Output,
    - History Output

### SQL Query Tab

- You can enter SQL statements directly into the query editor area. 
- The statements entered can be saved to a file or snippet for later use. 
- At any point, you can also execute the statements you have entered.
- To save a snippet of code entered into the query editor:
    - Click Save SQL to Snippets List (Star icon) from the SQL query toolbar
    - Enter a name (optional), and click OK. 
- Executing a `SELECT` query will display the associated result set in the SQL View panel, directly below the SQL Query panel.
- **NOTE** *To quickly enter the name of a table, view, or column, double-click the item in the Schema Palette. The item name will be inserted into the SQL Query panel.*

### SQL Query Toolbar

- SQL query tools (from left to right) are:

    - **Open a script file in this editor:** Loads content from a saved SQL script into the SQL editor.

    - **Save the script to a file:** Enables you to save the current content of the SQL editor to a file.

    - **Execute the selected portion of the script or everything, if there is no selection:** Provides a simple way to execute the entire query or a subset of the query.

    - **Execute the statement under the keyboard cursor:** Uses the position of the keyboard cursor to identify and execute the query.
    
    - **Execute the EXPLAIN command on the statement under the keyboard cursor:** Uses the keyboard cursor's position to identify the query and then executes EXPLAIN. A result grid tab is also displayed when executing an EXPLAIN statement.
    
    - **Stop the query being executed:** Halts execution of the currently executing SQL script. The connection to the database server is not restarted, and all open transactions remain open.
    
    - **Toggle whether the execution of SQL script should continue after failed statements:** If the red “breakpoint” circle is displayed, the script terminates on a statement that fails. If you click the button so that the green arrow is displayed, execution continues past the failed code, possibly generating additional result sets. In either case, any error generated from attempting to execute the faulty statement is recorded in the `Output` pane. You can also set this behavior from the `SQL Execution` user preferences panel.

    - **Commit the current transaction:** All query tabs in the same connection share the same transactions. To have independent transactions, you must open a new connection.

    - **Rollback the current transaction:** All query tabs in the same connection share the same transactions. To have independent transactions, you must open a new connection.

    - **Toggle auto-commit mode:** When enabled, each statement is committed immediately. All query tabs in the same connection share the same transactions. To have independent transactions, you must open a new connection. Autocommit is enabled by default. To disable the default behavior, see the SQL Execution section of the MySQL Workbench Preferences dialog.

    - **Set limit for the number of rows returned by queries:** MySQL Workbench automatically adds the LIMIT clause with the configured number of rows to SELECT queries. The default value is 1000. The default value (1000) can be changed from the SQL Execution section of the MySQL Workbench Preferences dialog.

    - **Save current statement or selection to the snippet list:** For more information about the snippet list, see Section 8.1.5, “SQL Additions - Snippets Tab”.

    - **Beautify/reformat the SQL script:** By default, SQL keywords are changed to uppercase. This functionality can be changed from the SQL Execution section of the MySQL Workbench Preferences dialog.

    - **Show the Find panel for the editor:** Click Done to close the panel.

    - **Toggle display of invisible characters:** When selected, displays invisible characters, such as newlines, spaces, and tabs. A new line is represented as [LF], a space as a single dot (.), and a tab as a right arrow.

    - **Toggle wrapping of long lines:** When selected, wraps long lines in the SQL editor to eliminate the need to scroll. Deselecting this feature for long files is recommended.

### Query and Edit Menus

- The Query menu features the following items:

    - **Execute (All or Selection):** Executes all statements in the SQL Query area, or only the selected statements.

    - **Execute (All or Selection) to Text:** Executes all statements in the SQL Query area, or only the selected statements, and displays it in plain text like the standard MySQL command line console.

    - **Execute Current Statement:** Executes the current SQL statement.

    - **Execute Current Statement (Vertical Text Output):** Executes all statements in the SQL Query area, or only the selected statements, and displays it in plain text like the MySQL command line console does vertically (\G).

    - **Explain Current Statement:** Describes the current statement by using the MySQL EXPLAIN statement.

    - **Visual Explain Current Statement:** Visually describes the current statement, based on EXPLAIN information provided by MySQL Server 5.6 and above. MySQL Workbench parses the EXPLAIN (JSON) output from MySQL server 5.6+, and outputs a visual representation.

    - **Stop:** Stops executing the currently running script.

    - **Stop Script Execution On Errors:** If enabled, MySQL Workbench stops executing the query if errors are found. It can be enabled/disabled from this menu.

    - **Limit Rows:** By default, the number of returned rows (LIMIT) is 1000. Values defined here affect subsequent statements. The number ranges from 10 to 50000, and "Don't Limit."

    - **Collect Performance Schema Stats:** Provides data to the Query Stats result set view, which includes statement-specific information about Timing, Rows processed, Temporary tables, Joins per type, Sorting, and Index usage.

    - **Collect Resultset Field Metadata:** Provides data to the Form Editor and Field Types result set views.

    - **Reconnect to Server:** Reconnects to the MySQL server.

    - **New Tab to Current Server:**Creates a duplicate of the current SQL Editor tab.

    - **Auto-Commit Transactions:** Enable to auto-commit transactions.

    - **Commit Transaction:** Commits a database transaction.

    - **Rollback Transaction:** Rolls back a database transaction.

    - **Commit Result Edits:** Commits any changes you have made to the server.

    - **Discard Result Edits:** Discards any changes you have made.

    - **Export Results:** Exports result sets to a file. Selecting this option displays the Export Query Results to File dialog. The dialog enables you to select which result set you wish to export, the file format (CSV, HTML, XML), and the name and location of the output file. Then click Export to export the data.

**Edit Menu**
`
- The `Edit` menu provides the `Format` submenu. The `Format` submenu includes the following menu items:

    - **Beautify Query:** Reformats the query selected in the query tab and lays it out in a nicely indented fashion.

    - **UPCASE Keywords:** Converts keywords to uppercase in the currently selected query in the query tab.

    **lowercase Keywords:** Converts keywords to lowercase in the currently selected query in the query tab.

    - **Un/Comment Selection:** Comments the lines currently selected in the query tab. If the lines are already commented, this operation removes the comments.

    **Auto-complete:** Triggers the auto-completion wizard. This is enabled (and triggered) by default, and can be disabled with Preferences, SQL Editor, Automatically Start Code Completion. Auto-completion will list functions, keywords, schema names, table names and column names.

### Results Grid

The results area of the screen shows the results from executed statements. If the script contains multiple statements, a result subtab will be generated for each statement that returned results. 

**Note** *MySQL Workbench handles quoting and escaping for strings entered into the result grid, so adding quotes and proper escaping here is optional.*

**Note** *It is possible to enter a function, or other expression, into a field. Use the prefix \func to prevent MySQL Workbench from escaping quotation marks. For example, for the expression md5('fred'), MySQL Workbench normally would generate the code md5(\'fred\'). To prevent this, enter the expression as \func md5('fred') to ensure that the quoting is not escaped.*

**Result Grid Toolbar**
- Elements of the result grid toolbar include:

    - **Reset:** Resets all sorted columns.

    - **Refresh:** Refreshes all data by re-executing the original statement.

    - **Filter Rows:** performs a search of all cells (not case-sensitive). It automatically refreshes, and there is also the refresh button to perform this action manually.

    - **Edit Current Row:** Edit the current row.

    - **Add New Row:** Adds a new empty row, and highlights it in edit mode. Click Apply to execute (and review) the insert row query.

    - **Delete Selected Rows:** Deletes the selected rows. Click Apply to execute (and review) the delete query.

    - **Export:** Writes a result set to a CSV, HTML, JSON, SQL INSERT, Excel, XML, or Tab separated file as required.

        **Note ** *This exports a result set. To export an entire table or schema, see Data Export.*

    - **Import:** Import records from an external CSV file.

    - **Wrap Cell Content:** If the contents of a cell exceeds the cell width, then the data will be cut off with an ellipses. This option will instead wrap the contents within the cell, and adjust the cell height accordingly.

        **Note** *The "Refresh" button automatically adjusts the column width to match the longest string one of its cells. You may also manually adjust the column width.*

### Snippits Tab

- The Snippets secondary tab includes built-in, local, and shared custom snippets.
- The My Snippets option stores custom snippets in a file under the MySQL Workbench user's configuration directory. 
- Select the Shared option for shared snippets.

**Using Snippets**
- Snippets can be inserted into the SQL editor or the system's clipboard.
- To insert (use) a snippet, either use the snippet icons or right-click on the desired snippet and choose Insert. 

----
NOTE: Ended at section 8.1.5