#  ASP.net Core 2.1 Identity Server 4 - Full Stack Development
IdentityServer4 is an OpenID Connect and OAuth 2.0 framework for ASP.NET Core 2. visit: http://docs.identityserver.io/en/release/
###  Installing the packages

- Download and Install the .NET Core SDK and .NET Core Runtime from this link https://www.microsoft.com/net/download

- Go to Terminal or cmd and write dotnet --version. It will ensure that your dotnet CLI is installed and working. Mine show the version 2.1.403.
- Download and Install PostgreSQL.
- Download and Install Node.js Stable version.
- Download and Install as text editor Visual Studio Code (Optional).
- We created a directory and named it ASP.IS4Host.

 > ***dotnet new --help*** command will show help how to start new project.
 
 ### Create new Project
 Check the dotnet cli working
  ```sh
 dotnet --version
 ```
 Install the templates the identity server 4 has provided
 ```sh
 dotnet new -i identityserver4.templates
 ```
 Now you can see new packages of Identity Server 4 are installed. It will also show the different template that are available with dotnet cli.
 We are going to create a new project of Identity Server 4 with Asp.net core identity. Type inside the  ASP.IS4Host directory tree in the Terminal / cmd or cmdr. 
  ```sh
 dotnet new is4aspid
 ``` 
 > it will ask to dotnet run /seed you should answer with N (No)
 
 Now if we see inside the directory we will see the project created with files the template has provided us.
 
### Installing Dependencies
In this project we will use entity framework as ORM. 
1. Entity Framework
	  ```sh
	 dotnet add package Microsoft.EntityFrameworkCore --version 2.1.0
	 ``` 
  2. Entity Framework Design
	  ```sh
	  dotnet add package Microsoft.EntityFrameworkCore.Design --version 2.1.0
	  ```
2. Npgsql Dependency
	```sh
	dotnet add package Npgsql.EntityFrameworkCore.PostgreSQL --version 2.1.0
	```
3. Npgsql Design Dependency
	```sh
	dotnet add package Npgsql.EntityFrameworkCore.PostgreSQL.Design --version 2.2.0
	```
4. Identity Server Packages
	```sh
	dotnet add package IdentityServer4 --version 2.2.0
	dotnet add package IdentityServer4.EntityFramework --version 2.1.1
	dotnet add package IdentityServer4.AspNetIdentity --version 2.1.0
	```
5. Microsoft CodeAnalysis
	```sh
	dotnet add package Microsoft.CodeAnalysis --version 2.8.2
	```
> This because sometimes your machine may give warning that it did find the Code Analysis package. 

Finally we will add these to our project by
```sh
dotnet restore
```