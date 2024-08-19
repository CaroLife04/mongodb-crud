# Simple mongodb crud with fastapi

# create atlas db and copy url and paste it in the file .env it will be automatically use via library python-decouple
MONGO_DETAILS=your_url



python -m venv venv

venv/bin/activate

pip install -r requirements.txt

git init
git add .
git commit -m "My fastapi and mongo application"

# Heroku lets you deploy, run and manage applications written in Ruby, Node.js, Java, Python, Clojure, Scala, Go and PHP.
heroku create

heroku config:set MONGO_DETAILS="your_mongo_connection_url"

git push heroku master
heroku ps:scale web=1

heroku config:set MONGO_DETAILS="your_mongo_connection_url"

git push heroku master

heroku ps:scale web=1

# open to open your app in your default browser.

heroku open

deploying of a project with heroku

