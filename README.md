# Create/Build dotnet project in VSCode

## dotnet cli 
### new 
```
dotnet new list
```

## Step1 Create solution
```
dotnet new sln --name dotnet-cli-demo
```
## Step2 Add gitignore
```
dotnet new gitignore
```
## Step3 Create console app project
```
 dotnet new console --name console-ui
```
### Step4 Create lib project
```
dotnet new classlib --name helper-lib  
```
### Step5 Add project list to solution
```
dotnet sln dotnet-cli-demo.sln add console-ui/console-ui.csproj
dotnet sln dotnet-cli-demo.sln add helper-lib/helper-lib.csproj
```
### Step5 Add Reference project in `console-ui`
```
dotnet add console-ui/console-ui.csproj reference helper-lib/helper-lib.csproj 
```
### Step6 Add NuGet package in `helper-lib`
```
cd helper-lib
dotnet add package Dapper
```
### Step7 Start debug app
`ctrl+shift+P` to run the app