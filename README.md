# Introduction:

Well, this is a task from Hahn Softwareentwicklung & is a CRUD Frontend and Backend developed by Josué Lackwood M. 

# Task Description:

The assigned task involved the following objectives:

1. Development of a Web API using the DDD (Domain-Driven Design) pattern in .Net6.

2. Creation of an Angular CRUD (Create, Read, Update, Delete) application to manage data with front-end and back-end validation, utilizing FluentValidation syntax in both.

3. Implementation of an overview feature with a grid layout within the Angular application.

4. Ensuring the application can be easily started using Docker Compose and is verifiable for functionality.

# Entire development:

Entities and Value Objects:

The primary entity is ReportAggregate, encompassing details about the reported fires' location and county. It also includes a list of individual reports and basic fire index statistics. ReportItem serves as the value object representing an individual report contained within a ReportAggregate.

Back-End Development:

To implement the Web API infrastructure, I utilized .NET 6 and followed the principles of Domain-Driven Design (DDD), employing a "clean" architecture approach. The API is divided into three distinct layers: Application layer (WebAPI folder), Domain layer, and Infrastructure layer.

Relevant Details:

For the project's database requirements, I chose to use LiteDB due to its user-friendly nature and minimal resource overhead. I implemented the repository pattern to interact with the LiteDB database.

To control the repositories and validate the ReportAggregate entities, I developed the IReportService. The validation process relies on FluentValidation, located within the infrastructure layer.

Front-End Development:

As my experience with browser-based frameworks like Angular was limited, the front-end design may be considered rudimentary. Nonetheless, it encompasses the following aspects:

1) Material-based design, incorporating Material widgets as inspired by Google's design guidelines.

2) A primary table that lists all ReportAggregates and their associated properties.

3) Functionality to create, update, and delete ReportAggregates and their respective ReportItems.

To enhance the project's appeal, I decided to center it around a police reporting service. The focus is on enabling users to view and submit reports (ReportItem) related to forest fires occurring at specific locations within a county (ReportAggregate).

## How to use?

**__To run the project, please type ```docker compose up --build``` in the root directory of the repository (```/DDD-CRUD```).__**
**__And then navigate to [Angular application](http://localhost:4200/) (```http://localhost:4200```) to access the Angular Front-end application.__**

Also, to recreate the image with the testing values in the database, please use ```docker compose up --force-recreate```.

