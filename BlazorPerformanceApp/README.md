# BlazorPerformanceApp

Este es un proyecto de aplicación web Blazor WebAssembly diseñado para demostrar conceptos de componentes y rendimiento en Blazor.

## Descripción

`BlazorPerformanceApp` es una aplicación de demostración que ilustra el uso de componentes Razor, incluyendo un componente híbrido (`HybridComponent.razor`) que muestra cómo renderizar una lista de datos simulados. El proyecto sirve como ejemplo básico para entender la estructura y el funcionamiento de una aplicación Blazor del lado del cliente (WebAssembly).

## Características

*   **Blazor WebAssembly:** Ejecución del lado del cliente utilizando WebAssembly.
*   **Componentes Razor:** Uso de componentes reutilizables como `Counter`, `Home`, `Weather` y `HybridComponent`.
*   **HybridComponent:** Un componente personalizado que demuestra la carga y renderizado de una lista de datos (`Data`) simulada.
*   **Inyección de Dependencias:** Configuración básica de servicios en `Program.cs`, incluyendo `HttpClient`.

## Requisitos Previos

*   [.NET SDK](https://dotnet.microsoft.com/download) (versión compatible con el proyecto, generalmente .NET 6 o superior).
*   Visual Studio, Visual Studio Code u otro editor compatible con C#.

## Cómo Ejecutar el Proyecto

1.  **Clonar o descargar el repositorio.**
2.  **Navegar al directorio del proyecto:**
    Abrir una terminal y ejecutar:
    ```bash
    cd "Blazor for Front-End Development/BlazorPerformanceApp/BlazorPerformanceApp"
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

*   `Pages/`: Contiene las páginas y componentes Razor de la aplicación (`Home`, `Counter`, `Weather`, `HybridComponent`).
*   `Shared/`: (Si existe) Contiene componentes compartidos como el diseño principal (`MainLayout`) y el menú de navegación (`NavMenu`).
*   `wwwroot/`: Archivos estáticos como CSS, imágenes y el archivo `index.html`.
*   `Program.cs`: Punto de entrada de la aplicación y configuración de servicios.
