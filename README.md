# Introduction
Welcome to **Film Library** service!(like Kinopoisk or IMDb) 
It enables you to get some information about movies and add it to your favourites(if you are a regular user).
---

Getting started
Before launching the app you have to change the connection string to your database. 
You can do it in "appsettings.json" file in FilmLibrary.UI folder.
---

How does it work
---
Logging in

First of all, you need to log in(initially available accounts: login - "Gleb", password - "adminpass" for administrator 
and login - "George", password - "george" for regular user) or to sign up using the new login and password.

Application operation
When you launch the application, you see common list of movies available for everybody. 
- If you are logged in as a common user,
you can add a film to your favourites using star near this film's record. Then you can check your favourites using title "Show favourite movies".
- If you are logged in as an administrator,
you can edit and delete movies using appropriate titles near the movie record.
Also you can check some users favourite movies, using selection bar at the bottom of the page.
##Testing
To run reporitory tests you will need to add your connection string in FilmLibrary.SharedData.UnitTestsConstants.TestsConnectionString.
Also you can check test coverage using command line. Firstly, you have to enter command 'cd Name_Of_Project_With_Tests(FilmLibrary.Business.Tests, 
FilmLibrary.DAL.Tests or FilmLibrary.UI.Tests) && dotnet test --collect:"XPlat Code Coverage"'. This will create xml-format report. 
Then you have to enter command 'reportgenerator -reports:"Path_To_The_Xml-Format_Report" -targetdir:"Name_Of_Directory" -reporttypes:Html'.
Then you have to open chosen directory and open index.html file. There you will see detailed statistics of test coverage.
---

#Restrictions
When you are adding a new film to common list as an administator, you have to specify at least one actor.
