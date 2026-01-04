# TaskManagerApp

Este es un proyecto de aplicación web Blazor WebAssembly diseñado para demostrar la comunicación entre componentes padre e hijo mediante parámetros y eventos.

## Descripción

`TaskManagerApp` es una aplicación de demostración que ilustra los conceptos fundamentales de comunicación entre componentes en Blazor. El proyecto muestra cómo un componente padre (`ParentTaskManager`) puede pasar datos a componentes hijos (`ChildTaskDisplay`) y cómo los componentes hijos pueden notificar eventos de vuelta al padre mediante `EventCallback`. Es ideal para aprender patrones de comunicación entre componentes en Blazor.

## Características

*   **Blazor WebAssembly:** Ejecución del lado del cliente utilizando WebAssembly.
*   **Comunicación Padre-Hijo:** Demostración de paso de datos del padre al hijo mediante parámetros `[Parameter]`.
*   **Comunicación Hijo-Padre:** Uso de `EventCallback<T>` para notificar eventos del hijo al padre.
*   **Componentes:**
    *   `ParentTaskManager.razor`: Componente padre que gestiona una lista de tareas.
    *   `ChildTaskDisplay.razor`: Componente hijo que muestra una tarea individual y permite marcarla como completada.
*   **Renderizado Dinámico:** Uso de `@foreach` para renderizar múltiples instancias del componente hijo.
*   **Gestión de Estado:** Actualización de la interfaz mediante `StateHasChanged()`.
*   **Componentes Estándar:** Incluye componentes de ejemplo como `Counter` y `Home`.

## Requisitos Previos

*   [.NET SDK](https://dotnet.microsoft.com/download) (versión compatible con el proyecto, generalmente .NET 6 o superior).
*   Visual Studio, Visual Studio Code u otro editor compatible con C#.

## Cómo Ejecutar el Proyecto

1.  **Clonar o descargar el repositorio.**
2.  **Navegar al directorio del proyecto:**
    Abrir una terminal y ejecutar:
    ```bash
    cd "Blazor for Front-End Development/TaskManagerApp"
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
6.  **Navegar a la página de tareas:**
    Accede a `/parent-task-manager` para ver el administrador de tareas.

## Estructura del Proyecto

*   `Pages/`: Contiene las páginas y componentes Razor:
    *   `ParentTaskManager.razor`: Componente padre que gestiona la lista de tareas y maneja eventos de los componentes hijos.
    *   `ChildTaskDisplay.razor`: Componente hijo que muestra una tarea individual con un botón para marcarla como completada.
    *   `Counter.razor`, `Home.razor`: Componentes de ejemplo adicionales.
*   `Layout/`: Contiene componentes de diseño compartidos.
*   `wwwroot/`: Archivos estáticos como CSS e imágenes.
*   `Program.cs`: Punto de entrada de la aplicación y configuración de servicios.

## Funcionalidades Destacadas

### Comunicación Padre → Hijo

El componente `ParentTaskManager` pasa datos al componente `ChildTaskDisplay` mediante el parámetro `TaskName`:

```razor
<ChildTaskDisplay TaskName="@task" OnTaskCompleted="HandleTaskCompleted"/>
```

El componente hijo recibe el dato mediante:

```csharp
[Parameter]
public string TaskName { get; set; } = "Tarea sin nombre";
```

### Comunicación Hijo → Padre

El componente `ChildTaskDisplay` notifica al padre cuando una tarea se completa mediante `EventCallback`:

```csharp
[Parameter]
public EventCallback<string> OnTaskCompleted { get; set; }

private async Task MarkAsCompleted()
{
    await OnTaskCompleted.InvokeAsync(TaskName);
}
```

El componente padre maneja el evento:

```csharp
private void HandleTaskCompleted(string completedTask)
{
    TaskList.Remove(completedTask);
    StateHasChanged();
}
```

### Flujo de Eventos

1. Usuario hace clic en "Marcar como Completada"
2. Se ejecuta `MarkAsCompleted()` en el componente hijo
3. Se invoca `OnTaskCompleted.InvokeAsync()` notificando al padre
4. Se ejecuta `HandleTaskCompleted()` en el componente padre
5. Se elimina la tarea de `TaskList`
6. Se llama a `StateHasChanged()` para actualizar la UI
7. Blazor re-renderiza automáticamente la interfaz

## Conceptos Clave Demostrados

*   **Parámetros de Componente**: Uso de `[Parameter]` para recibir datos del padre.
*   **EventCallback**: Mecanismo para comunicación de eventos del hijo al padre.
*   **Renderizado Dinámico**: Generación de múltiples componentes mediante `@foreach`.
*   **Gestión de Estado**: Actualización manual de la UI con `StateHasChanged()`.
*   **Binding de Eventos**: Uso de `@onclick` para manejar eventos de usuario.
