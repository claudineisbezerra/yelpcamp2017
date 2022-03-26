IDE ON CLOUD9
================
>>Created an NodeJs App and package.json file
npm init --yes

>> Clones a repository from a source (in this case GitHub)
git clone https://github.com/claudineisbezerra/yelpcamp2017.git

>> Creates reference to github REPO and updates in REPO
git remote -v
git remote add origin https://github.com/claudineisbezerra/yelpcamp2017.git
git add [filename filename filename ]
git commit -m "Description of a change"
git push -u origin master
    Username for 'https://github.com/claudineisbezerra/': claudineisbezerra@gmail.com
    Password for 'https://github.com/claudineisbezerra/': [Private]
    

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
https://dry-caverns-83776.herokuapp.com/ | https://git.heroku.com/dry-caverns-83776.git

>> Git commands to verify and deploy
git remote -v
git push heroku master

>> Check heroku logs
heroku logs --tail

>>Ensure that at least one instance of the app is running
heroku ps:scale web=1

>> Opp App on given URL (Just eqquivalent a refresh)
heroku open

>>Scale Up and Down your App by changing Dyno Amount
heroku ps:scale web=0
heroku ps:scale web=1
heroku ps:scale web=2


FRAMEWORKS
===========
>>Instal dependency libs
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
