# BlazorServerApp

Este es un proyecto de aplicación web Blazor Server diseñado para demostrar conceptos de renderizado del lado del servidor, comunicación en tiempo real con SignalR y gestión de estado.

## Descripción

`BlazorServerApp` es una aplicación de demostración que ilustra el uso de Blazor Server, donde la lógica de la aplicación se ejecuta en el servidor y las actualizaciones de la interfaz de usuario se envían al cliente a través de una conexión SignalR. El proyecto incluye ejemplos de chat en tiempo real, gestión de estado y componentes interactivos.

## Características

*   **Blazor Server:** Renderizado del lado del servidor con actualizaciones en tiempo real mediante SignalR.
*   **SignalR Chat:** Implementación de un chat en tiempo real usando SignalR (`SignalRChat.razor` y `NotificationHub.cs`).
*   **Componentes Interactivos:** Incluye componentes como `Counter`, `Weather`, y `StateManagement`.
*   **Gestión de Estado:** Ejemplo de gestión de estado en componentes Blazor Server.
*   **Modo de Renderizado Interactivo:** Uso de `@rendermode InteractiveServer` para componentes con interactividad del lado del servidor.

## Requisitos Previos

*   [.NET SDK](https://dotnet.microsoft.com/download) (versión compatible con el proyecto, generalmente .NET 6 o superior).
*   Visual Studio, Visual Studio Code u otro editor compatible con C#.

## Cómo Ejecutar el Proyecto

1.  **Clonar o descargar el repositorio.**
2.  **Navegar al directorio del proyecto:**
    Abrir una terminal y ejecutar:
    ```bash
    cd "Blazor for Front-End Development/BlazorServerApp/BlazorServerApp"
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

*   `Components/Pages/`: Contiene las páginas y componentes Razor de la aplicación:
    *   `Home.razor`: Página de inicio.
    *   `Counter.razor`: Ejemplo de contador interactivo.
    *   `Weather.razor`: Ejemplo de visualización de datos meteorológicos.
    *   `SignalRChat.razor`: Implementación de chat en tiempo real con SignalR.
    *   `StateManagement.razor`: Ejemplo de gestión de estado.
    *   `Error.razor`: Página de error.
*   `Components/Layout/`: Contiene componentes de diseño compartidos (como `MainLayout` y `NavMenu`).
*   `Hubs/`: Contiene los hubs de SignalR:
    *   `NotificationHub.cs`: Hub para la comunicación en tiempo real del chat.
*   `wwwroot/`: Archivos estáticos como CSS, JavaScript e imágenes.
*   `Program.cs`: Punto de entrada de la aplicación y configuración de servicios (incluyendo SignalR).

## Funcionalidades Destacadas

### SignalR Chat

El componente `SignalRChat.razor` demuestra cómo implementar un chat en tiempo real:
*   Conexión al hub SignalR (`NotificationHub`).
*   Envío y recepción de mensajes en tiempo real.
*   Indicador de estado de conexión.
*   Gestión del ciclo de vida de la conexión con `IAsyncDisposable`.
