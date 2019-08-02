# rest-web  
## required  
- docker >= 18.09  
- docker-compose >= 1.23.2  

## How  to set up  

```
$ cd ~/rest-web

$ docker-compose up -d

$ docker-compose run web ./bin/rails db:create

$ docker-compose run web ./bin/rails db:migrate

$ docker-compose ps -d 
rest-web_db_1    docker-entrypoint.sh mysqld      Up      3306/tcp, 33060/tcp   
rest-web_web_1   bundle exec rails s -p 300 ...   Up      0.0.0.0:3000->3000/tcp
``` 
- localhost:3000 on web brouser