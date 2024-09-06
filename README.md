# dotnet_blazor_webapi_identity_example1

## 概要
* Blazor にログイン画面を付けて認証する
* 処理自体は WebAPI 側に実装する

前回：dotnet_asp_webapi_identity_example1  
https://github.com/Tobotobo/dotnet_asp_webapi_identity_example1  

## 詳細

```
dotnet new gitignore
dotnet new sln -n Example

dotnet new webapi --use-controllers  -n Example.WebAPI
dotnet sln add Example.WebAPI
dotnet add Example.WebAPI package Microsoft.AspNetCore.Identity.EntityFrameworkCore
dotnet add Example.WebAPI package Microsoft.EntityFrameworkCore.InMemory

dotnet new blazor -n Example.Blazor
dotnet sln add Example.Blazor
dotnet add Example.Blazor reference Example.WebAPI
```

```
dotnet run --project Example.WebAPI
```
http://localhost:5094/swagger

```
dotnet run --project Example.Blazor
```