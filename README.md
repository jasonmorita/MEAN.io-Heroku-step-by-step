# Step-by-step to get Mean.io running on Heroku
## Based on this YouTube tutorial by Mark Tucker: [http://www.youtube.com/watch?v=B1E0YXXITWg](http://www.youtube.com/watch?v=B1E0YXXITWg)

Download mean.io, unzip, cd to directory. Be sure to get all hidden files. 

> "npm install" 

Set up Heroku account

Then https://devcenter.heroku.com/articles/quickstart

Install Heroku Toolbelt

> bower install

Edit .gitignore to remove public/lib

> git init

> git add .  

> git commit -m "init commit"

> heroku login

> heroku create

> heroku keys:add

> git push heroku master

https://dashboard.heroku.com/apps

Click on app

Click on Run Production Check

Add free tier Papertrail addon

Add free tier MongoHQ

Go back to Apps, click on app, then MongoHQ

Click Admin collection, then Users

Add a user w usr/pwd

Click Overview and copy Mongo URI

Depending on mean.io at the time of install, the file to update is config/env/development.js. Change the db: property to new URI w correct usr/pwd.

> git add .

> git commit -m "add db"

> git push heroku master

> heroku open 

Marvel. 
