# Blog
The NestAngularBlog project integrates NestJS and Angular to create a powerful, full-stack web application. The backend uses NestJS with TypeORM and ElephantSQL for robust data management, while Angular and Angular Materials ensure a dynamic, modern frontend. RxJS Observables streamline real-time data handling, and Angular Universal enhances server-side rendering for improved performance and SEO. Comprehensive testing with Cypress ensures reliability, making this project a showcase of efficient and scalable web development.
# Instructions to run the Project

## With Docker

Command:  
`docker-compose up`  
and then visit `localhost:4200`

### Tipps & Tricks for docker

If you need to remove docker images or containers you can use one of the following commands.

Command to remove all images:  
`docker rmi -f $(docker images -a -q)`

Command to remove all containers:  
`docker rm -vf $(docker ps -a -q)`

## Without Docker

### 2. Add an environment file to the project

Add a .env file in the api folder (at the top of your api folder, so nest can find it)

- add your own DATABASE_URL in the .env file
- add your own JWT_SECRET in the .env file

Database:  
You can use the free database from www.elephantsql.com (explained in the first video)

JWT Secret:  
Explained in the third video - https://www.youtube.com/watch?v=bbDDSylRM04

Example of file:

    DATABASE_URL=<your url>
    JWT_SECRET=jklasjdoij897231na

### Start the Backend in dev Mode after you added the .env file

`cd api`  
`npm install`  
`npm run start:dev`

### Start the Frontend in dev Mode after you added the .env file

`cd frontend`  
`npm install`  
`ng serve`

# Start the e2e tests

`cd e2e`  
`npm install`  
`npm run cypress:open`

### Generate e2e Report (html)

`npm run cypress:report`

etc. would be great.
