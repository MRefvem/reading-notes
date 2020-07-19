# Read:10 - MVC

## Microsoft: Overview of ASP.NET Core MVC

ASP.NET Core MVC is a rich framework for building web apps and APIs using the Model-View-Controller design pattern.

The Model-View-Controller architectural pattern separates an application into three main groups of components: Models, Views, and Controllers. User requests are routed to a Controller which is responsible for working with the Model to perform user actions and/or retrieve results of queries. The Controller chooses the View to display to the user, and provides it with any Model data it requires.

![Model-View-Controller](assets/MVC.png)

The reason why we do this is because its easier to code, debut and test something that has a single job. It's more difficult to update, test and debug code that has dependencies spread across two or more of these three areas.

### Model Responsibilities

The Model in an MVC application represents the state of the application and any business logic or operations that should be performed by it. Business logic should be encapsulated in the model, along with any implementation logic for persisting the state of the application.

### View Responsibilities

Views are responsible for presenting content through the user interface. They use the Razor view engine to embed .NET code in HTML markup. If you want to perform a lot of logic in your views, consider using a View Component to simplify the view.

### Controller Responsibilities

Controllers are the components that handle user interaction, with with the model, and ultimately select a view to render. In an MVC application, the view only displays information; the controller handles and responds to the user input and interaction. In the MVC pattern, the controller is the initial entry point, and is responsible for selecting which model types to work with and which view to render.

## ASP.NET Code MVC

The ASP.NET Core MVC framework is a lightweight, open source, highly testable presentation framework optimized for use with ASP.NET Core.

ASP.NET Core MVC provides a petterns-based way to build dynamic websites that enables a clean separation of concerns. It gives you full control over markup, supports TDD-friendly development and uses the latest web standards.

## Features

ASP.NET Core MVC includes the following:

- Routing
- Model binding
- Model validation
- Dependency injection
- Filters
- Areas
- Web APIs
- Testability
- Razor view engine
- Strongly typed views
- Tag helpers
- View Components