# demo-aspnet-angular
Integration Options for an Angular front-end and an ASP.Net Core MVC back-end API

These solutions require ASP.Net Core 2.1 SDK and Visual Studio 2017 (15.7, any edition) to be installed on the developer machine.

# combo
Create two projects with terminal commands:
..\solutionRoot> dotnet new mvc –o CompanyName.Product.MvcWeb
..\solutionRoot> ng new companyname-product-cli

Any version of the Angular CLI can be used, version 6.0.8 was used to generate this sample.

Then edit the MVC Startup.cs middleware and MSBuild steps in the .csproj file.

Run from Visual Studio works with and without debugging.  Debug only debugs the C# code, use Chrome to debug the Angular app. Debug will use the start task in the angular project to start it within node, and will support live reload as the Angular code is changed.

Publish from Visual Studio will run the Angular projects build task and include the output in the published content folder.
