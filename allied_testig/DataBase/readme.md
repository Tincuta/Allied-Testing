Task: Create an application that makes queries to a database and shows the result on a html page.

In order to run this programme you will need several tools to install:

* MongoDB 
* Node.js


[This video will guide you how correctly to install ```MongoDB``` on a OSX](https://www.youtube.com/watch?v=jasqfcfOnfM&index=6&list=PLRQuJcU2aZG-aMedJxa7p7ylYmOn5iMlS)

[This video will guide you how correctly to install ```Node.js``` on OSX and updating ```npm```](https://www.youtube.com/watch?v=wREima9e6vk)

After you have successfully installed MongoDB and Node.js you will need to do 2 more things:

1. Open terminal and cd into the directory containing this project. Write ```npm install```, this will install all the dependency that our app requires.

2. Insert data to ou newly installed MongoDB

* First of all we will need to run mongo server. For this just type mongod --dbpath=/data/db in terminal
* Second we will need to run a mongorestore command in the project folder using terminal. For this just type mongorestore dump.

Now we are all set and ready to run our application. For this just type ```node app.js``` in the project folder in terminal.

Open any browser you have on address: ```localhost:3000```

There you will see ```3368``` movies with it's title and year and also a hyperlink to imdb link of each movie obtained from the database ```video```, ```movies``` collections.

Here is an example of one movie:
```
{
	"_id" : ObjectId("56f3f121e07ebcf4358965e2"),
	"title" : "Jaws",
	"year" : 1975,
	"imdb" : "tt0073195"
}
{
	"_id" : ObjectId("56f3f1a2e07ebcf4358965e3"),
	"title" : "Mad Max 2: The Road Warrior",
	"year" : 1981,
	"imdb" : "tt0082694"
}
```

Each movie has 4 data that refers to it: 
* ```_id``` (that is default added by mongodb)
* ```title``` of the movie
* ```year``` of release
* ```imdb``` address


Screenshots:

Starting ```MongoDB``` server:
![alt tag](https://raw.githubusercontent.com/CristianChris/Allied-testing-Homeworks/master/HW_3/screenshots/mongod.png)
Starting ```app.js```
![alt tag](https://raw.githubusercontent.com/CristianChris/Allied-testing-Homeworks/master/HW_3/screenshots/node.png)
Open Safari on ```localhost:3000``` url.
![alt tag](https://raw.githubusercontent.com/CristianChris/Allied-testing-Homeworks/master/HW_3/screenshots/safari.png)