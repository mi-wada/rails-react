1. docker-compose run api rails new . --force --no-deps --database=postgresql --api
2. docker-compose build
3. docker-compose run --rm front sh -c "npm install -g create-react-app && create-react-app app"
4. write in 'api/config/database.yml'
   ```
   default: &default
   adapter: postgresql 
   encoding: unicode 
   host: db 
   username: postgres 
   password: password 
   pool: 5
   ```
5. docker-compose run api rake db:create
6. docker-compose up
