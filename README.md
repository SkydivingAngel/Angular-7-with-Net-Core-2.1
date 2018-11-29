## In order to Create an Angular 7 project using Net Core 2.1 as back-end follow theese steps:
#### Angular 7 now supports Typescript 3.1, RxJS 6.3 and Node 10

* Update SPA Net Templates:
dotnet new --install Microsoft.AspNetCore.SpaTemplates::*

* Create the Project
dotnet new angular -o angular7core2test

* Open the project file (csproj) with Visual Studio and Save the Solution

* Modify package.json:
Remove "--extract-css" from "start "and "build".
It's now defined in "angular.json"

* Update Angular Version to latest (command line on ClientApp folder):
ncu -u then npm install

* Update to "angular.json" -> Migration -.angular-cli.json to angular.json (command line on ClientApp folder):
ng update @angular/cli

* Fix audit: npm audit fix

* Modify "again" package.json to this version of bootstrap:
"bootstrap": "3.3.7"

* If publishing on IIS modify angular.json adding:
"baseHref": "/Angular5Core2/"

