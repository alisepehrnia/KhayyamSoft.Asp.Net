# 🧰 KhayyamSoft.Asp.Net – ASP.NET Project Templates

A collection of **ASP.NET project templates** maintained by KhayyamSoft.  
The repository contains three independent starter kits covering both **ASP.NET Core** and **classic ASP.NET MVC 5**:

| Template | Stack | Target | Purpose |
|----------|-------|--------|---------|
| **`ASP5Bootstrap`** | ASP.NET Core Razor Pages | `net5.0` | A minimal ASP.NET Core 5 Razor Pages starter with Bootstrap |
| **`ASPMVC5FaBootstrapBoilerplate`** | ASP.NET MVC 5 | .NET Framework **4.5.2** | A Farsi/Persian Bootstrap boilerplate for MVC 5 |
| **`ASPMVC5FaLayered`** | ASP.NET MVC 5 (layered) | .NET Framework **4.8** | A layered MVC 5 solution (Core / Infrastructure / WebUI) with tests |

> **Repository description:** *“KhayyamSoft.Asp.Net”* — the committed `README.md` contains only this line.

---

## 📖 Overview

`KhayyamSoft.Asp.Net` collects reusable starting points for ASP.NET development:

- **`ASP5Bootstrap`** gives you a clean ASP.NET Core 5 Razor Pages skeleton — useful for modern .NET web apps.
- **`ASPMVC5FaBootstrapBoilerplate`** is aimed at **Persian/Farsi** MVC 5 applications that want Bootstrap styling out of the box.
- **`ASPMVC5FaLayered`** demonstrates a **layered architecture** for MVC 5, splitting domain contracts (`X.Core`), data/identity infrastructure (`X.Infrastructure`), and the web UI (`X.WebUI`), with unit, integration, and functional test projects.

Each template is self-contained. You can copy the folder you need into a new solution, or open its `.sln`/`.csproj` directly.

---

## 🗂️ Repository Structure

```text
KhayyamSoft.Asp.Net/
├── README.md
└── templates/
    ├── ASP5Bootstrap/                       # ASP.NET Core 5 Razor Pages
    │   ├── Pages/
    │   ├── Properties/
    │   ├── wwwroot/
    │   ├── ASP5Bootstrap.csproj              # net5.0
    │   ├── Program.cs
    │   ├── Startup.cs
    │   └── appsettings.Development.json
    │
    ├── ASPMVC5FaBootstrapBoilerplate/        # MVC 5 + Bootstrap (Farsi)
    │   ├── App_Start/
    │   ├── Assets/
    │   ├── Controllers/
    │   ├── Properties/
    │   ├── Views/
    │   ├── ASPMVC5FaBootstrapBoilerplate.csproj   # .NET Framework 4.5.2
    │   ├── ASPMVC5FaBootstrapBoilerplate.sln
    │   └── Global.asax / Web.config
    │
    └── ASPMVC5FaLayered/                     # Layered MVC 5 solution
        ├── src/
        │   ├── X.Core/                       # Domain contracts, constants, extensions
        │   ├── X.Infrastructure/             # Data, Identity, Logging (EF 6, Identity 2.2.3)
        │   └── X.WebUI/                      # MVC 5 web application
        ├── tests/
        │   ├── UnitTests/
        │   ├── IntegrationTests/
        │   └── FunctionalTests/
        ├── ASPMVC5FaLayered.sln
        └── LICENSE                           # Apache License 2.0
```

## 🧩 Template 1 – `ASP5Bootstrap` ([ASP.NET](https://asp.net/) Core 5 Razor Pages)

### What it is

A minimal **[ASP.NET](https://asp.net/) Core 5 Razor Pages** starter.  
The project targets **`net5.0`** and is named `IVC_WebApp` in code.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASP5Bootstrap/ASP5Bootstrap.csproj)[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASP5Bootstrap/Program.cs)

### What it includes

- **Razor Pages** enabled via `services.AddRazorPages()` and `endpoints.MapRazorPages()`.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASP5Bootstrap/Startup.cs)
    
- **Static files** served with `app.UseStaticFiles()` — this is where the Bootstrap assets live (`wwwroot/`).[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASP5Bootstrap/Startup.cs)
    
- **Developer exception page** in Development, and an `/Error` handler in other environments.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASP5Bootstrap/Startup.cs)
    
- **Routing** and **authorization** wired in `Startup.Configure`.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASP5Bootstrap/Startup.cs)
    
- **Generic Host** startup via `Host.CreateDefaultBuilder(args).ConfigureWebHostDefaults(...)` in `Program.cs`.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASP5Bootstrap/Program.cs)
    

### How to run

```bash
git clone https://github.com/KhayyamSoft/KhayyamSoft.Asp.Net.git
cd KhayyamSoft.Asp.Net/templates/ASP5Bootstrap
dotnet run
```

Or open `ASP5Bootstrap.csproj` in Visual Studio 2022 and press **F5**.

> ⚠️ **.NET 5 is out of support.** The project builds with the .NET 5 SDK/targeting pack. For new work, retarget the `.csproj` to a supported LTS (e.g. `net8.0`) and re-test.

---

## 🧩 Template 2 – `ASPMVC5FaBootstrapBoilerplate` (MVC 5 + Bootstrap, Farsi)

### What it is

A **classic [ASP.NET](https://asp.net/) MVC 5** boilerplate aimed at **Persian/Farsi** applications, with Bootstrap included in the `Assets/` folder.  
It targets **.NET Framework 4.5.2**.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)

### Dependencies (from the `.csproj`)

|Package|Version|
|---|---|
|Microsoft.AspNet.Mvc|**5.2.9**[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)|
|Microsoft.AspNet.Razor|**3.2.9**[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)|
|Microsoft.AspNet.WebPages|**3.2.9**[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)|
|Newtonsoft.Json|**13.0.1**[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)|
|Microsoft.AspNet.Web.Optimization|**1.1.3**[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)|
|WebGrease|**1.6.0**[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)|
|Antlr|**3.5.0.2**[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)|
|Microsoft.CodeDom.Providers.DotNetCompilerPlatform|**3.6.0**[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)|

### Structure

- `App_Start/` — MVC configuration, including `RouteConfig` with the default `{controller}/{action}/{id}` route pointing at `Home/Index`.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/App_Start/RouteConfig.cs)
    
- `Controllers/`, `Views/` — standard MVC 5 folders.
    
- `Assets/` — Bootstrap and other front-end assets.
    
- `Global.asax`, `Web.config` — classic [ASP.NET](https://asp.net/) application entry and configuration.
    

### How to run

1. Open `ASPMVC5FaBootstrapBoilerplate.sln` in **Visual Studio 2022** (with the **[ASP.NET](https://asp.net/) and web development** workload).
    
2. Right-click the solution → **Restore NuGet Packages** (the project uses `packages.config`; packages are not committed).
    
3. Set `ASPMVC5FaBootstrapBoilerplate` as the startup project.
    
4. Press **F5**.
    

> The project is configured for IIS Express on **`http://localhost:33850/`**.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)

---

## 🧩 Template 3 – `ASPMVC5FaLayered` (Layered MVC 5 with Tests)

### What it is

A **layered [ASP.NET](https://asp.net/) MVC 5** solution targeting **.NET Framework 4.8**.  
It separates the application into **`X.Core`**, **`X.Infrastructure`**, and **`X.WebUI`**, and includes **three test projects**.

### Solution projects

The solution `ASPMVC5FaLayered.sln` contains:[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaLayered/ASPMVC5FaLayered.sln)

|Project|Path|Role|
|---|---|---|
|**`X.Core`**|`src/X.Core`|Domain contracts: `Constants/`, `Extensions/AppIdentityExtensions/`, `Interfaces/`. Targets `v4.8`.[](https://github.com/KhayyamSoft/KhayyamSoft.Asp.Net/tree/main/templates/ASPMVC5FaLayered/src/X.Core)[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaLayered/src/X.Core/X.Core.csproj)|
|**`X.Infrastructure`**|`src/X.Infrastructure`|Data access (`Data/`), Identity (`Identity/`), Logging (`Logging/`). Targets `v4.8`.[](https://github.com/KhayyamSoft/KhayyamSoft.Asp.Net/tree/main/templates/ASPMVC5FaLayered/src/X.Infrastructure)[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaLayered/src/X.Infrastructure/X.Infrastructure.csproj)|
|**`X.WebUI`**|`src/X.WebUI`|MVC 5 web application. Targets `v4.8`.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaLayered/src/X.WebUI/X.WebUI.csproj)|
|**`UnitTests`**|`tests/UnitTests`|Unit tests. Targets `v4.8`.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaLayered/tests/UnitTests/UnitTests.csproj)|
|**`IntegrationTests`**|`tests/IntegrationTests`|Integration tests.|
|**`FunctionalTests`**|`tests/FunctionalTests`|Functional/end-to-end tests.|

### Key dependencies

- **Entity Framework 6.4.4** — referenced by `X.Infrastructure`.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaLayered/src/X.Infrastructure/X.Infrastructure.csproj)
    
- **Microsoft.AspNet.Identity 2.2.3** — [ASP.NET](https://asp.net/) Identity for user management.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaLayered/src/X.Infrastructure/X.Infrastructure.csproj)
    
- **JWT / IdentityModel** — `System.IdentityModel.Tokens.Jwt` is referenced and was bumped in a later commit.[](https://github.com/KhayyamSoft/KhayyamSoft.Asp.Net/tree/main/templates/ASPMVC5FaLayered/src/X.Infrastructure)
    
- **MVC 5.2.7** — referenced by `X.WebUI`.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaLayered/src/X.WebUI/X.WebUI.csproj)
    

### License

This template includes an **Apache License 2.0** (`templates/ASPMVC5FaLayered/LICENSE`).[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaLayered/LICENSE)  
The other templates do **not** include a license file.

### How to run

1. Open `templates/ASPMVC5FaLayered/ASPMVC5FaLayered.sln` in **Visual Studio 2022**.
    
2. Restore NuGet packages.
    
3. Set **`X.WebUI`** as the startup project.
    
4. Build and press **F5**.
    

> `X.WebUI` is configured for IIS Express on **`http://localhost:19055/`**.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaLayered/src/X.WebUI/X.WebUI.csproj)

---
## 🛠️ Prerequisites (All Templates)

|Requirement|Needed for|
|---|---|
|**Visual Studio 2022** with **[ASP.NET](https://asp.net/) and web development** workload|All templates|
|**.NET 5 SDK**|`ASP5Bootstrap`|
|**.NET Framework 4.5.2 targeting pack**|`ASPMVC5FaBootstrapBoilerplate`|
|**.NET Framework 4.8 targeting pack**|`ASPMVC5FaLayered`|
|**NuGet**|Classic MVC projects (packages are not committed)|
|**SQL Server / LocalDB** (optional)|`ASPMVC5FaLayered` if you enable the EF/Identity data layer|

---

## 🚀 Quick Start

```bash
git clone https://github.com/KhayyamSoft/KhayyamSoft.Asp.Net.git
cd KhayyamSoft.Asp.Net
```

**[ASP.NET](https://asp.net/) Core template:**

```bash
cd templates/ASP5Bootstrap
dotnet run
```

**MVC 5 templates:** open the corresponding `.sln` in Visual Studio, restore NuGet packages, and press **F5**.

---

## 📝 Notes & Caveats

- **Root README was a single line.** This document replaces it with full documentation.
    
- **No license at the repository root.** Only `ASPMVC5FaLayered` contains an **Apache 2.0** license. The other two templates have no license file — contact the repository owner before redistributing them.
    
- **`ASP5Bootstrap` targets .NET 5**, which is **end-of-life**. Retarget to a supported LTS before using it in production.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASP5Bootstrap/ASP5Bootstrap.csproj)
    
- **Classic MVC projects use `packages.config`**, so **NuGet restore is required** before building.[](https://raw.githubusercontent.com/KhayyamSoft/KhayyamSoft.Asp.Net/main/templates/ASPMVC5FaBootstrapBoilerplate/ASPMVC5FaBootstrapBoilerplate.csproj)
    
- **These are starter templates**, not complete applications. They provide project structure, configuration, and (for the boilerplate) styling — you add the business logic.
    
- **The layered template includes tests** (`UnitTests`, `IntegrationTests`, `FunctionalTests`), but the test contents were not individually inspected; treat them as scaffolding to extend.
    
- **`ASPMVC5FaBootstrapBoilerplate`** uses “Fa” in its name to indicate **Farsi/Persian** support; check `Assets/` and `Views/` for RTL styles and localized layouts.
    

---
## 🤝 Contributing

Issues and pull requests are welcome — e.g. retargeting `ASP5Bootstrap` to a supported .NET LTS, adding a root license, or expanding the test coverage in `ASPMVC5FaLayered`.

---
## 📄 License

Feel free to use :)
