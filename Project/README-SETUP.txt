README for SETUP after cloning this project:

1. Reinstall Entity Framework Packages
2. Restart Visual Studio and reopen the project
2. Go to Tools -> NuGet Package Manager -> Package Manager Console
3. In the Console, type: update-database -targetmigration:0   THEN press enter
4. Then, navigate to your Migrations folder in the Solution Explorer, and delete 
    every file in the Migrations folder EXCEPT for Configuration.cs
5. Back in the Package Manager Console, type: add-migration initial   THEN press enter
6. After that runs, type: update-database   THEN press enter
7. Navigate to View -> Server Explorer -> Connect to Database
8. Select Microsoft SQL server, and hit Continue
9. Under the Server Name field, type: (localdb)\mssqllocaldb
10. Under Select or enter a database name, type: Model.CbDb
11. Hit OK. You are now connected to the database. Accounts can be added manually in the
    back end, which can then be manipulated in the GUI (which should now load properly)