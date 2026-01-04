# FeedbackApp

Este es un proyecto de aplicación web Blazor WebAssembly diseñado para recopilar y gestionar comentarios de usuarios mediante formularios con validación.

## Descripción

`FeedbackApp` es una aplicación de demostración que ilustra cómo crear un sistema de recopilación de feedback utilizando Blazor WebAssembly. La aplicación permite a los usuarios enviar comentarios a través de un formulario validado y visualizar todos los comentarios enviados en una lista. Utiliza validación de datos con Data Annotations y gestión de estado mediante un servicio singleton.

## Características

*   **Blazor WebAssembly:** Ejecución del lado del cliente utilizando WebAssembly.
*   **Formulario de Feedback:** Componente `FeedbackForm.razor` con campos para nombre, email y comentarios.
*   **Validación de Formularios:** Validación del lado del cliente usando Data Annotations:
    *   Campo `Name` requerido.
    *   Campo `Email` con validación de formato de correo electrónico.
    *   Campo `Comment` con límite de 500 caracteres.
*   **Servicio de Feedback:** `FeedbackService` implementado como singleton para almacenar y recuperar comentarios.
*   **Lista de Feedback:** Componente `FeedbackList.razor` para visualizar todos los comentarios enviados.
*   **Modelo de Datos:** Clase `Feedback` con propiedades validadas.

## Requisitos Previos

*   [.NET SDK](https://dotnet.microsoft.com/download) (versión compatible con el proyecto, generalmente .NET 6 o superior).
*   Visual Studio, Visual Studio Code u otro editor compatible con C#.

## Cómo Ejecutar el Proyecto

1.  **Clonar o descargar el repositorio.**
2.  **Navegar al directorio del proyecto:**
    Abrir una terminal y ejecutar:
    ```bash
    cd "Blazor for Front-End Development/FeedbackApp/FeedbackApp"
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

*   `Models/`: Contiene los modelos de datos:
    *   `Feedback.cs`: Modelo con propiedades `Name`, `Email` y `Comment`, incluyendo atributos de validación.
*   `Services/`: Contiene los servicios de la aplicación:
    *   `FeedbackService.cs`: Servicio singleton para gestionar la lista de comentarios con métodos `AddFeedback()` y `GetFeedback()`.
*   `Pages/`: Contiene las páginas y componentes Razor:
    *   `FeedbackForm.razor`: Formulario para enviar comentarios (página principal `/`).
    *   `FeedbackList.razor`: Lista de todos los comentarios enviados.
    *   `Counter.razor`, `Weather.razor`, `Home.razor`: Componentes de ejemplo adicionales.
*   `Layout/`: Contiene componentes de diseño compartidos.
*   `wwwroot/`: Archivos estáticos como CSS e imágenes.
*   `Program.cs`: Punto de entrada de la aplicación y configuración de servicios.

## Funcionalidades Destacadas

### Validación de Formularios

El modelo `Feedback` utiliza Data Annotations para validar los datos:
*   `[Required]`: Campo obligatorio para el nombre.
*   `[EmailAddress]`: Validación de formato de email.
*   `[StringLength(500)]`: Límite de caracteres para comentarios.

### Gestión de Estado

El `FeedbackService` se registra como singleton en `Program.cs`, lo que permite compartir la lista de comentarios entre diferentes componentes durante la sesión de la aplicación.
