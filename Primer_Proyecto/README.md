# Primer_Proyecto

Este es un proyecto básico de aplicación web Blazor WebAssembly diseñado para demostrar conceptos fundamentales de Blazor, incluyendo configuración de servicios, gestión de listas y uso de archivos de configuración.

## Descripción

`Primer_Proyecto` es una aplicación de demostración que ilustra los conceptos básicos de Blazor WebAssembly. El proyecto incluye ejemplos de componentes interactivos, un servicio para acceder a configuraciones de API, y una página para gestionar una lista dinámica de elementos. Es ideal para aprender los fundamentos de Blazor y la estructura de un proyecto WebAssembly.

## Características

*   **Blazor WebAssembly:** Ejecución del lado del cliente utilizando WebAssembly.
*   **ApiService:** Servicio singleton para acceder a la configuración de la URL base de la API desde `appsetting.json`.
*   **ListaElementos:** Componente interactivo que permite agregar y visualizar elementos en una lista dinámica.
*   **Configuración:** Uso de archivo `appsetting.json` para almacenar configuraciones como:
    *   URL base de la API (`ApiSettings:BaseUrl`)
    *   Cadenas de conexión
    *   Configuración de logging
    *   Feature flags
*   **Componentes Estándar:** Incluye componentes de ejemplo como `Counter`, `Weather` y `Home`.
*   **OtroContador:** Componente adicional de contador personalizado.

## Requisitos Previos

*   [.NET SDK](https://dotnet.microsoft.com/download) (versión compatible con el proyecto, generalmente .NET 6 o superior).
*   Visual Studio, Visual Studio Code u otro editor compatible con C#.

## Cómo Ejecutar el Proyecto

1.  **Clonar o descargar el repositorio.**
2.  **Navegar al directorio del proyecto:**
    Abrir una terminal y ejecutar:
    ```bash
    cd "Blazor for Front-End Development/Primer_Proyecto"
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

*   `Services/`: Contiene los servicios de la aplicación:
    *   `ApiService.cs`: Servicio para obtener la URL base de la API desde la configuración.
*   `Pages/`: Contiene las páginas y componentes Razor:
    *   `Home.razor`: Página de inicio.
    *   `Counter.razor`: Ejemplo de contador interactivo.
    *   `OtroContador.razor`: Otro ejemplo de contador.
    *   `ListaElementos.razor`: Componente para gestionar una lista dinámica de elementos.
    *   `Weather.razor`: Ejemplo de visualización de datos meteorológicos.
*   `Layout/`: Contiene componentes de diseño compartidos.
*   `wwwroot/`: Archivos estáticos como CSS e imágenes.
*   `appsetting.json`: Archivo de configuración con ajustes de la aplicación.
*   `Program.cs`: Punto de entrada de la aplicación y configuración de servicios.

## Funcionalidades Destacadas

### ApiService

El servicio `ApiService` demuestra cómo:
*   Inyectar `IConfiguration` para acceder a la configuración.
*   Leer valores del archivo `appsetting.json`.
*   Registrar el servicio como singleton en `Program.cs`.

### ListaElementos

El componente `ListaElementos.razor` muestra:
*   Gestión de estado local con una lista de strings.
*   Binding bidireccional con `@bind`.
*   Manejo de eventos con `@onclick`.
*   Validación básica para evitar agregar elementos vacíos.
*   Renderizado dinámico de listas con `@foreach`.

## Configuración

El archivo `appsetting.json` contiene varias configuraciones de ejemplo:
*   **ApiSettings.BaseUrl**: URL base para llamadas a la API.
*   **ConnectionStrings**: Cadenas de conexión a bases de datos.
*   **Logging**: Configuración de niveles de logging.
*   **FeatureFlags**: Flags para habilitar/deshabilitar características.
