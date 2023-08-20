## Environment
create file .env file and copy content to file
POSTGRES_HOST = 127.0.0.1
POSTGRES_DB = fantasy_worlds
POSTGRES_DB_DEV = fantasy_worlds_dev
POSTGRES_USER = postgres
POSTGRES_PASS = password
ENV = test
PEPPER=haha
SALT_ROUNDS = 10
TOKEN_SECRET = 52938f609c937763d72a390f76627292e3c81191812a735d16644a5b2e3e3a2d
PORT = 3000

## database.json
create file database.json file and copy content to file
{
  "dev": {
    "driver": "pg",
    "host": "127.0.0.1",
    "database": "fantasy_worlds_dev",
    "user": "postgres",
    "password": "password"
  },
  "prod": {
    "driver": "pg",
    "host": "127.0.0.1",
    "database": "fantasy_worlds",
    "user": "postgres",
    "password": "password"
  }
}
# Project Name
API Store front backend

## Installation
npm install

## Formatting the Source Code
npm run prettier

## Checking the Source Code
npm run lint

## Running Tests

npm run test


## Running the Project

nodemon

## docker compose file
create file docker-compose.yml file and copy content to file
version: '3.8'

services:
  db:
    image: postgres:latest
    environment:
      POSTGRES_PASSWORD: password
      POSTGRES_USER: postgres
      POSTGRES_DB: fantasy_worlds_dev
    ports:
      - "5432:5432"
    volumes:
      - db_data:/var/lib/postgresql/data
volumes:
  db_data:

## Running docker compose
docker-compose up


Access project at [http://localhost:3000].
