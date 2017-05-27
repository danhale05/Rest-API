REST API - Using Node, Express and MongoDB

Prereq's: 
1. [Node](http://www.nodejs.org) 
2. [MongoDB](http://www.mongodb.com) to run the database locally 

A quickstart for MongoDB is to create a folder called "data" in the root directory of your main drive, for example "C:\data". Inside the "data" folder, create another folder called "db" so "C:\data\db".

Once you've created them, you can run `C:\Program Files\MongoDB\Server\3.4\bin\mongod.exe` (the 3.4 would need updated if you have a different version) in your terminal window to start MongoDB. You may also navigate to the folder and open the "mongod.exe" file to start the program. There's more information at [MongoDB's](http://www.mongodb.com) website if you run into any trouble. MongoDB needs to be running behind the scene's for this all to work.

Also, you may consider using [Postman](https://www.getpostman.com/) to "POST".. ha yea, the ninja's to the database and [RoboMongo](https://robomongo.org/) to ensure they haven't Ninja'd their way free. RoboMongo will allow us to see what's inside the local database collection in MongoDB.

Once Node and MongoDB are installed, run `npm install` in the root directory. This will install the needed node modules listed in the package.json file to use in this application -Mongoose, Body-Parser and Express. After that run, `node index.js` from the console in the root directory. With index.js running, MongoDB running in the background, we can begin adding our Ninjas with Postman.

Also, if you don't like restarting the server each time you make a change, run `npm install nodemon -g` you may then use Nodemon in any project. It will restart the server each time a change is detected. To run Nodemon, use `nodemon index.js` instead of `node index.js`.

To use Postman, select the "POST" option from the dropdown menu. To the right of it enter `localhost:4000/api/ninjas`. Below that, select the "Headers" tab and the key/value should be - Content-Type":"application/json". Beside it, select the "Body" tab (ensure "raw" is selected) and here you may copy and paste in the Ninja's either from the text file included in the repo under "ninjas.txt" or by creating your own, using the examples as a template.

I'll be making changes to this in the future but if you see anything that needs corrected, feel free to submit some changes. Thanks!