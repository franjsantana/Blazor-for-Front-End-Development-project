# RecipeManagerApp

Este es un proyecto de aplicación web Blazor WebAssembly diseñado para gestionar recetas de cocina, permitiendo agregar, visualizar y consultar recetas.

## Descripción

`RecipeManagerApp` es una aplicación de demostración que ilustra cómo crear un sistema de gestión de recetas utilizando Blazor WebAssembly. La aplicación permite a los usuarios agregar nuevas recetas, visualizar una lista de todas las recetas disponibles, y consultar los detalles de recetas específicas. Utiliza un servicio singleton para la gestión de datos en memoria.

## Características

*   **Blazor WebAssembly:** Ejecución del lado del cliente utilizando WebAssembly.
*   **Modelo de Receta:** Clase `Recipe` con propiedades `Id`, `Name` y `Description`.
*   **RecipeService:** Servicio singleton para gestionar recetas con las siguientes funcionalidades:
    *   Almacenamiento de recetas en memoria.
    *   Agregar nuevas recetas con generación automática de IDs.
    *   Obtener recetas por ID.
    *   Recetas de ejemplo precargadas (Spaghetti Bolognese, Chicken Curry).
*   **Páginas de Gestión:**
    *   `Home.razor`: Página principal que muestra la lista de recetas.
    *   `AddRecipe.razor`: Formulario para agregar nuevas recetas.
    *   `RecipeDetails.razor`: Página de detalles de una receta específica.
*   **Componentes Estándar:** Incluye componentes de ejemplo como `Counter` y `Weather`.

## Requisitos Previos

*   [.NET SDK](https://dotnet.microsoft.com/download) (versión compatible con el proyecto, generalmente .NET 6 o superior).
*   Visual Studio, Visual Studio Code u otro editor compatible con C#.

## Cómo Ejecutar el Proyecto

1.  **Clonar o descargar el repositorio.**
2.  **Navegar al directorio del proyecto:**
    Abrir una terminal y ejecutar:
    ```bash
    cd "Blazor for Front-End Development/RecipeManagerApp/RecipeManagerApp"
    ```
3.  **Restaurar dependencias:**
    ```bash
    dotnet restore
    ```
4.  **Ejecutar la aplicación:**
    ```bash
    dotnet run
    ```
    O si utilizas `dotnet watch` para recarga en caliente:
    ```bash
    dotnet watch run
    ```
5.  **Abrir en el navegador:**
    La terminal mostrará la URL local (por ejemplo, `http://localhost:5000` o `https://localhost:7000`). Abre esa dirección en tu navegador web.

## Estructura del Proyecto

*   `Recipe.cs`: Modelo de datos para representar una receta con `Id`, `Name` y `Description`.
*   `Services/`: Contiene los servicios de la aplicación:
    *   `RecipeService.cs`: Servicio para gestionar recetas con métodos `AddRecipe()` y `GetRecipe()`.
*   `Pages/`: Contiene las páginas y componentes Razor:
    *   `Home.razor`: Página principal que muestra la lista de recetas disponibles.
    *   `AddRecipe.razor`: Formulario para crear y agregar nuevas recetas.
    *   `RecipeDetails.razor`: Página para visualizar los detalles de una receta específica.
    *   `Counter.razor`, `Weather.razor`: Componentes de ejemplo adicionales.
*   `Layout/`: Contiene componentes de diseño compartidos.
*   `wwwroot/`: Archivos estáticos como CSS e imágenes.
*   `Program.cs`: Punto de entrada de la aplicación y configuración de servicios.

## Funcionalidades Destacadas

### RecipeService

El servicio `RecipeService` demuestra:
*   Gestión de estado en memoria con una lista de recetas.
*   Generación automática de IDs utilizando `Max(r => r.Id) + 1`.
*   Métodos para agregar y recuperar recetas.
*   Registro como servicio singleton en `Program.cs` para compartir datos entre componentes.

### Navegación entre Páginas

La aplicación muestra:
*   Navegación desde la lista de recetas (`Home.razor`) a los detalles de cada receta (`RecipeDetails.razor`).
*   Uso de parámetros de ruta para pasar el ID de la receta.
*   Formulario de creación de recetas con navegación de regreso a la página principal.

## Datos de Ejemplo

La aplicación viene precargada con dos recetas de ejemplo:
*   **Spaghetti Bolognese**: A classic Italian pasta dish with rich meat sauce.
*   **Chicken Curry**: A flavorful curry dish with tender chicken pieces.
