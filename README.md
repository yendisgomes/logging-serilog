# Logging Serilog Project

## Overview
This project demonstrates how to set up and use Serilog for logging in a .NET 8 application. It includes a simple service and uses Swagger for API documentation.

## Libraries Installed
- `Serilog`: A diagnostic logging library for .NET applications.
- `Serilog.AspNetCore`: Serilog integration for ASP.NET Core.
- `Serilog.Sinks.Console`: A Serilog sink that writes log events to the console.
- `Swashbuckle.AspNetCore`: A library to generate Swagger documentation for ASP.NET Core Web APIs.

```
  Install-Package Serilog.AspNetCore
  Install-Package Serilog.Sinks.Seq
  Install-Package Serilog.Enrichers.Environment
  Install-Package Serilog.Enrichers.Process
  Install-Package Serilog.Enrichers.Thread
```

## Prerequisites
- .NET 8 SDK
- Visual Studio 2022 or any other compatible IDE

## Installation
1. Clone the repository:
```
git clone https://github.com/yendisgomes/logging-serilog.git
```
```
cd logging-serilog
```

2. Restore the NuGet packages:
```
dotnet restore
```

## Running the Project
1. Build the project
```
dotnet build
```

2. Run the project
```
dotnet run
```

3. Open your browser and navigate to `https://localhost:5001/swagger` to view the Swagger UI.


## SEQ - Recommended for Local Development
monitor and analyze your application’s structured logs
```
docker run --name seq -d -e ACCEPT_EULA=Y -p 80:80 -p 5341:5341 datalust/seq
```

## Project Structure
- `Program.cs`: The main entry point of the application, setting up Serilog and configuring the web host.
- `Services/IDummyService.cs`: Interface for the dummy service.
- `Services/DummyService.cs`: Implementation of the dummy service.

## Logging
The project uses Serilog for logging. Logs are written to the console. The logging configuration is set up in `Program.cs`.

## Swagger
Swagger is used to generate API documentation. It is configured in `Program.cs` and can be accessed at `https://localhost:5001/swagger`.

## Additional Information
- Ensure that the .NET 8 SDK is installed on your machine.
- The project is configured to use HTTPS. Make sure your development environment supports HTTPS.

