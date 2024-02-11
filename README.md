![NodeJS](https://img.shields.io/badge/node.js-6DA55F?style=for-the-badge&logo=node.js&logoColor=white)
![NestJS](https://img.shields.io/badge/nestjs-%23E0234E.svg?style=for-the-badge&logo=nestjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=for-the-badge&logo=typescript&logoColor=white)
![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white)
![Swagger](https://img.shields.io/badge/-Swagger-%23Clojure?style=for-the-badge&logo=swagger&logoColor=white)

## Project structure

```
src/
├── config/          => configuration files
├── constant/        => global constants
└── enum/            => global enums
└── exception/       => custom exceptions
└── modules/         
    ├── prisma/      => prisma module to work with database
    └── ...          => other modules
└── utils/           => global utility functions
└── app.module.ts    => main module
└── main.ts          => entry point
└── test/            => test files
Dockerfile           => configuration for Docker container
docker-compose.yml   => configuration for Docker compose to run multiple containers
env-example          => example of environment variables
```
Each module has its own folder with the following structure:

```
module/
├── dto/                        => data transfer objects
├── exceptions/                 => module specific exceptions
├── guards/                     => module specific guards
├── interfaces/                 => module specific interfaces
├── <module>.module.ts          => module definition
├── <module>.service.ts         => business logic
├── <module>.controller.ts      => request handlers
├── <module>.repository.ts      => database queries
```

## Swagger
Project has Swagger documentation. It can be accessed by the following URL:

```
https://<HOST>:<PORT>/docs
```

## Environment variables
Copy env-example file and update .env file with your environment variables
```
cp env-example .env
```

## Drizzle ORM

Prisma is an advanced ORM (Object-Relational Mapping) tool for Node.js and TypeScript. It operates over a database client that simplifies database operations by turning database queries into simple function calls. Unlike traditional ORMs, Prisma uses a schema-first approach, allowing developers to define their database schema with Prisma's own modeling language. This schema is then used to generate a Prisma Client, which provides type-safe database access and migrations. Prisma supports multiple databases, including PostgreSQL, MySQL, SQLite, and more, making it a versatile tool for a wide range of projects.

## Run application

```
docker-compose up --build
```

### Run only specific container in Docker:

```
docker-compose up -d <container>
```

E.g.

```
docker-compose up -d postgres
```

### Run application using Docker:

```
docker-compose down
```

```
docker-compose build && docker-compose up
```

### Create database migration:

```
npm run migrate:dev:create
```

### Run migrations:

```
npm run migrate:deploy
```

### Seed database

```
npm run seed:run
```

## About us
### Ready to see what's beyond? Check out our website to discover more projects and learn how we're making a difference: [Discover More](https://lnoks.com).
<img src="https://api.lnoks.com/api/files/gpdni4nbyo5aj5b/ckzlbh3iiyt5n83/logo_purple_pure_hqhbjiEXbL.svg?token=" alt="drawing" width="200" height="100"/>

