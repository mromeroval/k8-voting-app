## Kubernetes - Example Voting App
This is a distributed application for setting up an online voting system. It consists of the following components:

#### Front-end Web App (Python)
This is a Python-based web application that allows users to vote between two options. It interacts with the Redis service to record new votes.

#### Redis
An in-memory data store used to collect new votes from the Front-end Web App before they are persisted in the database.

#### .NET Worker
A background worker process built with .NET. It consumes votes from Redis and stores them in the Postgres database.

#### Postgres Database
A Postgres database instance used to persist and store all the votes. It is backed by a Docker volume for data persistence.

#### Node.js Web App
A Node.js web application that displays the real-time results of the voting by querying the Postgres database.

#### Deployment
The entire application is deployed and managed using Kubernetes. Each component runs as a separate microservice within the Kubernetes cluster, allowing for scalability, high availability, and easy management.

#### Architecture

