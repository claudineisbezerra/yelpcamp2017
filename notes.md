IDE ON CLOUD9
================

DATABASE ON MLAB
================
//LOCAL DB    
//mongoose.connect("mongodb://localhost/yelpcamp-db");

//REMOTE MLAB DB   
//mongoose.connect("mongodb://claudineisbezerra:just4now@ds117093.mlab.com:17093/yelpcamp-db");

//Uses ENV variable to connect to DB.
// i.e: export export DATABASEURL=mongodb://claudineisbezerra:just4now@ds117093.mlab.com:17093/yelpcamp-db
var URL = process.env.DATABASEURL || "mongodb://localhost/yelpcamp-db"
console.log("DATABASEURL: "+URL);

DEPLOYMENT ON HEROKU
====================
//You need to update the Heroku CLI if having problems using an HTTP proxy. For that, do:
wget -qO- https://cli-assets.heroku.com/install-ubuntu.sh | sh

>>heropku login
Email: claudineisbezerra@gmail.com
Password: [private]

>>Heroku Created App
https://agile-gorge-85589.herokuapp.com/ | https://git.heroku.com/agile-gorge-85589.git

>> Git commands to verify and deploy
git remote
git push heroku master

FRAMEWORKS
===========

npm install body-parser --save
npm install connect-flash --save
npm install ejs --save
npm install express --save
npm install express-session --save
npm install method-override --save
npm install mongoose --save
npm install passport --save
npm install passport-local --save 
npm install passport-local-mongoose --save
npm install request --save
