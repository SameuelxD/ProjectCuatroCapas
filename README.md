### ProjectCuatroCapas

### Crear Soluciones
dotnet new sln
dotnet new classlib -o Domain
dotnet new classlib -o Persistence
dotnet new classlib -o Application
dotnet new classlib -o Security
dotnet new webapi -o API

dotnet sln add .\Domain
dotnet sln add .\Persistence
dotnet sln add .\Application
dotnet sln add .\Security
dotnet sln add .\API

### Agregar Referencias entre Proyectos
# Referencias Application
cd Application
dotnet add reference ..\Domain
dotnet add reference ..\Persistence

# Referencias Persistence
cd Persistence
dotnet add reference ..\Domain

# Referencias Security
cd Security
dotnet add reference ..\Application

# Referencias API
cd API
dotnet add reference ..\Application
dotnet add reference ..\Security

### Paquetes WebApi

dotnet add package AspNetCoreRateLimit --version 5.0.0 

dotnet add package AutoMapper.Extensions.Microsoft.DependencyInjection --version 12.0.1

dotnet add package Microsoft.AspNetCore.Authentication.JwtBearer --version 7.0.11

dotnet add package Microsoft.AspNetCore.Mvc.Versioning --version 5.1.0

dotnet add package Microsoft.AspNetCore.OpenApi --version 7.0.11

dotnet add package Microsoft.EntityFrameworkCore.Design --version 7.0.11

dotnet   add package System.IdentityModel.Tokens.Jwt --version 6.32.3

### Paquetes Domain

dotnet add package FluentValidation.AspNetCore --version 11.3.0

dotnet add package itext7.pdfhtml --version 5.0.1

dotnet add package Microsoft.EntityFrameworkCore --version 7.0.11

### Paquetes Persistence

dotnet add package Microsoft.EntityFrameworkCore --version 7.0.11

dotnet add package Pomelo.EntityFrameworkCore.MySql --version 7.0.0

### Paquetes Security

dotnet add package System.IdentityModel.Tokens.Jwt --version 6.32.2

### Referencias entre proyectos

![Captura de pantalla 2023-10-26 103117](https://github.com/SameuelxD/ProjectCuatroCapas/assets/126287892/49fd2eb6-2a6c-447c-9c55-1d827906a1f9)



