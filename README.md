# Address Book IV

This repository contains the files for each part of our final assignment. There is an Android client and JavaFX client which can be run from within your IDE, and a web service which is currently being hosted on Digital Ocean, so the directory containing that code is just meant to be viewed, not run.

One note to the person grading this, because my AWS has had permissions issues, I have had to resort to hosting my database on a Digital Ocean MySQL server and the web service on a VPS form them. I have been running into issues where the Tomcat server idles despite the config being set to not allow that, so if my clients fail to connect to the web service, please contact me so I can reload the Tomcat server.

If you'd like, you can also do this yourself using the [Tomcat Manager](http://143.198.226.185:8080/manager/html "Tomcat manager for my web app"). To do this, you will have to login with these credentials:

  Username: admin
  Password: Nelson77
  
Then in the "/AddressBookIVService-1.0-SNAPSHOT" application row, press the reload button in the commands column.

## Application Functions

### List Contacts
- This function will display all contacts stored in the database.
- Check this first when testing my app because it will show you if the Tomcat server is working properly. Like I mentioned earlier, if the connection to the database is unsuccessful it is because the Tomcat session idled and you will need to contact me to reload it.
- Note: when looking at the list of contacts, the one that you added most recently won't necessarily show up on the bottom of the list because the primary key in the MySQL database is set to the phone number.

### Add Contact
- You will have to enter all values that you are prompted to in the app and then press the add button.
- Your input will not be accepted if you leave any category empty.

### Delete Contact
- Before using this section of the app, make not of the phone number of the contact you want to delete. You will have to enter it in the text field provided in order to remove the contact that corresponds to this number.

### Edit Contact
- Similarly to the delete function, you will need to know the phone number of the contact you want to delete. Enter this value along with all of the new values for the contact you want to edit.

## Android Client
- To run the Android client, you will have to open the corresponding folder in this repository with Android Studio.
- To use the app, you will need to have a virtual device setup and run it on that.
- I tested the app on a virtual Pixel 4 XL with Android 7 and 11.

## JavaFX Client
- I have placed my whole project directory for the JavaFX client in this repository rather than an executable file, so you will have to compile and run it yourself.
- This can be done by opening the project in your IDE and running it there, or through command line if you know how. Just make sure the module-info is included if it is not run through an IDE.
- I used IntelliJ IDEA to write this program and tested it on Java 14, but it should work fine with other IDEs and Java versions.

## Web Service
- Because of the issues that I ran into that prevented me from using AWS, I resorted to using Digital Ocean for my web service and database.
- The database is running on one of their services that hosts a MySQL server.
- The web service had to be hosted on a VPS which is using Ubuntu 20 and has a Tomcat 9 server running on it.
