# Lab Report 2

# Part 1

The first step is to go back to the lab we did on week 2 and refresh our memories on how the ```URLHandler Inteface``` works. In our case 
we are going to use ```StringServer.java``` in a similar way to how we used ```NumberServer.java``` in the lab. ```StringServer.java``` is a program with a ```main``` method that takes a unique ```port``` as an argument, and with it, creates a ```URLHandler``` that uses ```Server.java``` to start a web server using that handler. 

The key change in the code happens in the ```else``` statement of the ```handleRequest``` method. We are prompting the code to seek out the string ```add-message``` in the URL path to begin the process of identifying the strings we want to print out onto our web server. If ```add-message``` is present, then we create a new String array that splits the parameters of the arguments at the ```'='``` sign, and looks for the first element in that 
array to be the String ```'s'```, and if it is, then the program procedes to print out the lines at index 1 of the array on a new line using ```"\n"```. 

Another important note is that as soon as we assume there is a string provided as the argument for the parameters array, the code throws an error on the num variable and Integer.parseInt method that had been provided by course staff for NumberServer.java.

!['StringServer code'](Screen Shot 2023-04-21 at 8.46.47 AM.png)


!['Banana'](Screen Shot 2023-04-21 at 8.45.29 AM.png)


!['Banana King'](Screen Shot 2023-04-21 at 8.44.14 AM.png)






