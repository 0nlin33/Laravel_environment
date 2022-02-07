# Laravel_environment
Laravel environment repo

- Have Docker Installed

- Clone the repor into your system

- Go into the folder where  you cloned this repo and then, 

- In your terminal run the command 
     ~$ docker-compose build
    
Once it is built, you will have to run the follwing commands to make sure the files are updated and all required files are present.
      
      ~$ docker-compose run --rm composer update
            
run this command to update your composer, this is bring in the vendor file which is initially abscent.
      
      ~$ docker-compose run --rm npm install
            
run this command to get your node_modules.
            
      ~$ docker-compose run --rm npm run dev
      
After running above commands, go into the src folder and create an .env file.
You can do this by copying the .env.example file already present in the src folder and renaming it to .env
    
After you have your .env file, run the command,
        
      ~$ docker-compose run --rm artisan migrate
        
Above steps will complete the requirements to setup the environment. Now you can initialize the environment with the command,

      ~$ docker-compose up -d


Port Information:
Mapped Ports: Exposed ports

Nginx-      80:80

Mysql-      3306:3306

phpmyadmin- 8081:80

redis-      6379:6379

npm-        3000:3000 (3001:3001)
            
mailhog-    1025:1025 (8025:8025)
            
You can change the ports to fit your requirements.      
      
