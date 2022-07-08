# MySql tutorial for beginners (+AdonisJs)
Understand how orchestrating MySql server, MySql workbench and AdonisJs works.

~Check out this guide to get you started with GitHub: https://swcarpentry.github.io/git-novice/index.html

# MySql SERVER --VS-- MySql WORKBENCH

- MySql server provides your DBMS (database management system) with querying and connectivity capabilities. Translated: Create a server for your database, create an account (or more accounts) for this database so you can query this database via MySql Workbench.
- MySql workbench is a visual database design tool. Translated: Create a connection to the server for each user registered with MySql server, which allows all connected users to access/view/query the databases created on that MySql server. 
- To sum up: MySql server is providing the back end while MySql workbench is providing the front end. Your job is to link the two so to be used as one.
- The idea of this setup: On the server you create multiple users; On the workbench you connect via user's credentials to the server and manipulate databases (create/alter/drop databases).


