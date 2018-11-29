In order to Create an Angular 7 project using Net Core 2.1 as back-end follow theese steps

1)
Update SPA Net Templates:
dotnet new --install Microsoft.AspNetCore.SpaTemplates::*

2)
Create the Project
dotnet new angular -o angular7core2test

3)
Open the project file with Visual Studio and Save the Solution

4)
Modify package.json:
Remove "--extract-css" because it's now defined in "angular.json" -> "extractCss": true,
"start": "ng serve",
"build": "ng build",

5)
Update Angular Version to latest (command line on ClientApp folder):
ncu -u
npm install

6)
Update to "angular.json" -> Migration -.angular-cli.json to angular.json (command line on ClientApp folder):
ng update @angular/cli

7)
Fix audit: npm audit fix

8)
Modify "again" package.json to this version of bootstrap:
"bootstrap": "3.3.7"

9)
If publishing on IIS modify angular.json adding:
"baseHref": "/Angular5Core2/"
