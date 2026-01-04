# Rutinas_Entrenamiento

Este es un proyecto de aplicación web Blazor WebAssembly diseñado para gestionar rutinas de entrenamiento físico, permitiendo agregar, eliminar y visualizar rutinas de ejercicio.

## Descripción

`Rutinas_Entrenamiento` es una aplicación de demostración que ilustra cómo crear un sistema de gestión de rutinas de entrenamiento utilizando Blazor WebAssembly. La aplicación permite a los usuarios agregar nuevas rutinas de ejercicio, eliminar rutinas existentes por nombre, visualizar una lista de todas las rutinas disponibles, y consultar los detalles de rutinas específicas. Utiliza un servicio singleton para la gestión de datos en memoria.

## Características

*   **Blazor WebAssembly:** Ejecución del lado del cliente utilizando WebAssembly.
*   **Modelo de Rutina:** Clase `Rutinas` con propiedades:
    *   `Id`: Identificador único de la rutina.
    *   `Nombre`: Nombre de la rutina de ejercicio.
    *   `Descripcion`: Descripción de la rutina.
    *   `Duracion`: Duración de la rutina en minutos.
*   **RutinaService:** Servicio singleton para gestionar rutinas con las siguientes funcionalidades:
    *   Almacenamiento de rutinas en memoria.
    *   Agregar nuevas rutinas con generación automática de IDs.
    *   Eliminar rutinas por nombre (búsqueda case-insensitive).
    *   Obtener rutinas por ID.
    *   Rutinas de ejemplo precargadas (Sentadilla, Curl de Barra).
*   **Páginas de Gestión:**
    *   `Home.razor`: Página principal que muestra la lista de rutinas disponibles.
    *   `AñadirRutina.razor`: Formulario para agregar nuevas rutinas de entrenamiento.
    *   `QuitarRutina.razor`: Formulario para eliminar rutinas por nombre.
    *   `DetallesEntrenamiento.razor`: Página de detalles de una rutina específica.
*   **Componentes Estándar:** Incluye componentes de ejemplo como `Counter` y `Weather`.

## Requisitos Previos

*   [.NET SDK](https://dotnet.microsoft.com/download) (versión compatible con el proyecto, generalmente .NET 6 o superior).
*   Visual Studio, Visual Studio Code u otro editor compatible con C#.

## Cómo Ejecutar el Proyecto

1.  **Clonar o descargar el repositorio.**
2.  **Navegar al directorio del proyecto:**
    Abrir una terminal y ejecutar:
    ```bash
    cd "Blazor for Front-End Development/Rutinas_Entrenamiento/Rutinas_Entrenamiento"
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

*   `Rutinas.cs`: Modelo de datos para representar una rutina de entrenamiento con `Id`, `Nombre`, `Descripcion` y `Duracion`.
*   `Services/`: Contiene los servicios de la aplicación:
    *   `RutinaService.cs`: Servicio para gestionar rutinas con métodos `AñadirRutina()`, `QuitarRutina()` y `ObtenerRutina()`.
*   `Pages/`: Contiene las páginas y componentes Razor:
    *   `Home.razor`: Página principal que muestra la lista de rutinas disponibles.
    *   `AñadirRutina.razor`: Formulario para crear y agregar nuevas rutinas.
    *   `QuitarRutina.razor`: Formulario para eliminar rutinas por nombre.
    *   `DetallesEntrenamiento.razor`: Página para visualizar los detalles de una rutina específica.
    *   `Counter.razor`, `Weather.razor`: Componentes de ejemplo adicionales.
*   `Layout/`: Contiene componentes de diseño compartidos.
*   `wwwroot/`: Archivos estáticos como CSS e imágenes.
*   `Program.cs`: Punto de entrada de la aplicación y configuración de servicios.

## Funcionalidades Destacadas

### RutinaService

El servicio `RutinaService` demuestra:
*   Gestión de estado en memoria con una lista de rutinas.
*   Generación automática de IDs utilizando `Max(r => r.Id) + 1`.
*   Métodos CRUD completos:
    *   `AñadirRutina()`: Agregar nuevas rutinas.
    *   `QuitarRutina()`: Eliminar rutinas por nombre (case-insensitive).
    *   `ObtenerRutina()`: Recuperar rutinas por ID.
*   Registro como servicio singleton en `Program.cs` para compartir datos entre componentes.

### Eliminación de Rutinas

La funcionalidad de eliminación (`QuitarRutina.razor`) incluye:
*   Búsqueda de rutinas por nombre sin distinción entre mayúsculas y minúsculas.
*   Validación para verificar que la rutina existe antes de eliminarla.
*   Feedback al usuario sobre el resultado de la operación.

## Datos de Ejemplo

La aplicación viene precargada con dos rutinas de ejemplo:
*   **Sentadilla**: Rutina para piernas (30 minutos).
*   **Curl de Barra**: Rutina para brazos (45 minutos).
