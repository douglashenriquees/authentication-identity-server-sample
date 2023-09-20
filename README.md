# Creating Solution

* dotnet new gitignore
* mkdir src
* cd src
* dotnet new sln -n AuthClientCredentialsSample

## Creating Identity Server Project

* dotnet new install identityserver4.templates
* dotnet new --list
* dotnet new is4empty -n IdentityServer
* dotnet sln add ./IdentityServer/IdentityServer.csproj
* check the identity server https://localhost:5001/.well-known/openid-configuration

## Creating WebApi Project

* dotnet new web -o Api --no-https true
* dotnet sln add ./Api/Api.csproj

## Creating Client Project

* dotnet new console -n Client
* dotnet sln add ./Client/Client.csproj
* dotnet add package IdentityModel