# MySql tutorial for beginners (+AdonisJs)
Understand how orchestrating MySql server, MySql workbench and AdonisJs works.

~Check out this guide to get you started with GitHub: https://swcarpentry.github.io/git-novice/index.html

# MySql SERVER --VS-- MySql WORKBENCH

- MySql server provides your DBMS (database management system) with querying and connectivity capabilities. Translated: Create a server for your database, create an account (or more accounts) for this database so you can query this database via MySql Workbench.
- MySql workbench is a visual database design tool. Translated: Create a connection to the server for each user registered with MySql server, which allows all connected users to access/view/query the databases created on that MySql server. 
- To sum up: MySql server is providing the back end while MySql workbench is providing the front end. Your job is to link the two so to be used as one.
- The idea of this setup: On the server you create multiple users; On the workbench you connect via user's credentials to the server and manipulate databases (create/alter/drop databases).


# Install MySql Server & Workbench

1. Start the setup using: mysql-installer-web-community-8.0.29.0
![MySql-devdefault](https://user-images.githubusercontent.com/63293696/178057522-41ad1063-4d51-4640-a8b8-9255f23ca3d3.PNG)
![MySql-servonly](https://user-images.githubusercontent.com/63293696/178057663-29ffc462-39ec-4404-a72a-7c5c6c42fbb7.PNG)
![MySql-clieonly](https://user-images.githubusercontent.com/63293696/178057714-b960b084-f452-47d1-971d-7313bf907696.PNG)
![MySql-full](https://user-images.githubusercontent.com/63293696/178057756-ea3fe969-de8e-4cc5-ac12-75c6a415f1a7.PNG)
![MySql-custom](https://user-images.githubusercontent.com/63293696/178057943-b2f5a85f-fde7-47b9-a3b2-a5e189777457.PNG)

2. Check requirements: Install python >v3.7
![MySql-checkreq](https://user-images.githubusercontent.com/63293696/178058494-758903c0-f782-48d6-a28a-dbf563b8902b.PNG)

3. Select product: MySQL Server 8.0.29 - X64 && MySQL Workbench 8.0.29 -X64
![MySql-selectprod](https://user-images.githubusercontent.com/63293696/178058312-a45e294b-371f-4b0c-8729-65e4a8b6ed07.png)

4. Ready to download
![MySql-confidownl](https://user-images.githubusercontent.com/63293696/178058628-c5d12ae9-59b3-477f-bf2d-9e28d7ff4315.png)

5. Ready to install
![MySql-readyinst](https://user-images.githubusercontent.com/63293696/178058693-972f34bc-c8e7-4c94-ad46-25ff81845db9.png)

6. Ready to configure MySql Server
![MySql-rdytoconf](https://user-images.githubusercontent.com/63293696/178058858-eb191def-b7d3-4eb3-a57b-118efac6073b.png)

7. Type of network
![MySql-typenetwork](https://user-images.githubusercontent.com/63293696/178058926-45190180-643b-4441-9991-9b86b1b31ce0.png)

8. Authentication method: is you select the new auth method like in the picture below, this will apply to the 'root' user so you will have to create another user 'sqluser' that uses the old auth method so we can make migrations (instructions provided in AdonisJs API Bash Commands.txt)
![MySql-authmeth](https://user-images.githubusercontent.com/63293696/178059013-45413e50-79c3-4623-9c7d-377b2fd389d3.png)

9. Create accounts page: by adding a password I just created the root user.
![MySql-accrols](https://user-images.githubusercontent.com/63293696/178059397-f5bf9658-162d-4b63-b81b-e572a3ed8246.png)

10. Windows service: unless you tick that box to make MySql server start on startup, you will have to manually start the service every time you need to use it
![MySql-windserv](https://user-images.githubusercontent.com/63293696/178059763-996c8417-e275-4405-8e11-24feb793a253.png)

11. Apply configurations
![MySql-applyconfig](https://user-images.githubusercontent.com/63293696/178059797-c216bdd2-414b-486d-b6bd-9f76db1f0318.png)

12. Configurtion is complete
![MySql-prodconf](https://user-images.githubusercontent.com/63293696/178059931-ae42f7b5-4460-45ed-8a87-cdd359b5cabc.png)

13. Installation is complete
![MySql-inscompl](https://user-images.githubusercontent.com/63293696/178059965-7ac5b5f3-18e3-4ac7-8c5d-c3d55e85bce9.png)


# MySql Workbench setup

1. You should have that 'root' user connection present already.
![W8-MySql Connections](https://user-images.githubusercontent.com/63293696/178060112-fa94b1fc-909c-4d84-bc89-828e9765a9a7.png)

2. When you click on the connection you will be required to provide the password for that user ('root' 'password' as per this tutorial)
![W8-MySql Password](https://user-images.githubusercontent.com/63293696/178060293-708abc73-098c-4838-8f2c-f152330b06a0.png)

3. This is how it looks like inside:
![W8-MySql Interface Connected](https://user-images.githubusercontent.com/63293696/178060365-6f699767-9f0b-4853-85e6-2850241b83be.png)

4. To create a new schema click on that ![image](https://user-images.githubusercontent.com/63293696/178061126-3ce4c04d-9c9a-46dc-a16c-86a48ce5f8c0.png)
![W8-MySql New Schema Create](https://user-images.githubusercontent.com/63293696/178060569-5b73f5bc-a22b-4bf5-a389-f126894c8e63.png)

5. Apply schema
![W8-MySql New Schema Script Review](https://user-images.githubusercontent.com/63293696/178060640-4dbcb976-5343-4522-afcc-714ca27579d1.png)

6. Finish schema
![W8-MySql New Schema Script Finish](https://user-images.githubusercontent.com/63293696/178060660-baa3b330-106f-44c0-b4d1-a281d7f43bd8.png)

7. Click on Schemas to reveal the databases
![W8-MySql Schema Users Table](https://user-images.githubusercontent.com/63293696/178060800-8a240dba-8b55-4379-b56b-0941ae0e1b8f.png)


# Setup AdonisJs : https://adonisjs.com/

1. Follow the instructions under AdonisJs API Bash Commands.txt and below by Solomon Eseme: https://www.section.io/engineering-education/build-a-restful-api-with-adonisjs/
![Untitled](https://user-images.githubusercontent.com/63293696/178062072-d47e323b-3861-4162-abff-d5a9fecc5e3f.png)


