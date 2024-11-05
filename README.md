## Prerequisites

get the docker at here https://docs.docker.com/get-docker/

## Getting Started

1. Clone this repository

2. Build and run the Docker container in development mode

   ```
   docker-compose up --build
   ```


   This will start the server on `http://localhost:3000` with hot-reloading enabled.
3. Database Migration and Seeder

```
npx knex migrate:latest --env development
```
npx knex seed:run --env development
```


## Running in Production

To run the project in production mode:

1. Open the `Dockerfile` and ensure the CMD is set to `CMD ["npm", "start"]`
2. Build and run the Docker container:
   ```bash
   docker build -t build-goal- .
   docker run -p 3000:3000 express-docker-project
   ```