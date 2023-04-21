# Lab Report 2

# Part 1

The first step is to go back to the lab we did on week 2 and refresh our memories on how the ```URLHandler Inteface``` works. In our case 
we are going to use ```StringServer.java``` in a similar way to how we used ```NumberServer.java``` in the lab. ```StringServer.java``` is a program with a ```main``` method that takes a unique ```port``` as an argument, and with it, creates a ```URLHandler``` that uses ```Server.java``` to start a web server using that handler. They key change in the code happens in the ```else``` statement of the ```handleRequest``` method. We are prompting the code to seek out the string ```add-message``` in the URL path to begin the process of identifying the strings that we want to print out onto our web server.  

!['StringServer code'](Screen Shot 2023-04-21 at 8.46.47 AM.png)


!['Banana'](Screen Shot 2023-04-21 at 8.45.29 AM.png)


!['Banana King'](Screen Shot 2023-04-21 at 8.44.14 AM.png)






