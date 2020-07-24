# JWT Auth Demo

This repository demos an ASP.NET Core web API application using JWT auth, and an integration testing project for a set of actions including login, logout, refresh token, impersonation, authentication, and authorization.

## Medium Articles

- [Using JWT in ASP.NET Core](https://codeburst.io/using-jwt-in-asp-net-core-148fb72bed03)

  In this article, I will show you how to implement an ASP.NET Core web API application using JWT authentication and authorization.

## Solution Structure

This repository includes two applications: an Angular SPA in the `angular` folder, and an ASP.NET Core web API app in the `webapi` folder. The SPA makes HTTP requests to the server side (the `webapi` app) using an API BaseURL `https://localhost:5001`. The API BaseURL is set in the `environment.ts` file and the `environment.prod.ts` file, which can be modified based on your situation.

- `angular`
  The SPA is served using NGINX on Docker. The application demonstrates JWT authorization in the front-end.
- `webapi`
  The ASP.NET Core web API app is served by Kestrel on Docker. This app has implemented HTTPS support.

## Usage

The demo is configured to run by Docker Compose. The services are listed in the `docker-compose.yml` file. You can launch the demo by the following command.

```bash
docker-compose up --build --remove-orphans
```

You can also move the folders around to consolidate the solution to be one ASP.NET Core web app using SPA service.

## Screenshots

- **Front-end** ([http://localhost:8080](http://localhost:8080))

  ![angular app](./localhost_8080.png)

- **Back-end** ([https://localhost:5001](https://localhost:5001))

  ![web api](./localhost_5001.png)
