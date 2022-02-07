docker pull devopsdockeruh/coursepage:latest
docker tag devopsdockeruh/coursepage registry.heroku.com/josephalbaphcoursepage/web
docker login --username=_ --password=$(heroku auth:token) registry.heroku.com
heroku container:login
docker push registry.heroku.com/josephalbaphcoursepage/web
heroku container:release web --app josephalbaphcoursepage

url: https://josephalbaphcoursepage.herokuapp.com/