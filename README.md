# Blazor for Front-End Development

Este repositorio contiene una colección de proyectos de demostración desarrollados con **Blazor WebAssembly** y **Blazor Server**, diseñados para ilustrar conceptos fundamentales y avanzados del desarrollo front-end con Blazor.

## Descripción

Esta colección de proyectos sirve como recurso educativo para aprender Blazor, cubriendo desde conceptos básicos como componentes y binding de datos, hasta temas más avanzados como comunicación en tiempo real con SignalR, gestión de estado, validación de formularios, y comunicación entre componentes.

## Proyectos Incluidos

### 1. [BlazorPerformanceApp](./BlazorPerformanceApp)
Aplicación de demostración que ilustra conceptos de componentes y rendimiento en Blazor WebAssembly.

**Características principales:**
- Componentes Razor reutilizables
- Componente híbrido (`HybridComponent`) con renderizado de listas
- Inyección de dependencias básica

### 2. [BlazorServerApp](./BlazorServerApp)
Aplicación Blazor Server que demuestra renderizado del lado del servidor y comunicación en tiempo real.

**Características principales:**
- Blazor Server con SignalR
- Chat en tiempo real (`SignalRChat`)
- Gestión de estado en componentes Server
- Modo de renderizado interactivo

### 3. [EventEaseApp](./EventEaseApp)
*Aplicación para gestión de eventos (README pendiente)*

### 4. [FeedbackApp](./FeedbackApp)
Sistema de recopilación de comentarios con validación de formularios.

**Características principales:**
- Formularios con validación usando Data Annotations
- Servicio singleton para gestión de datos
- Validación de email y límites de caracteres
- Lista de comentarios enviados

### 5. [Primer_Proyecto](./Primer_Proyecto)
Proyecto básico que introduce conceptos fundamentales de Blazor WebAssembly.

**Características principales:**
- Servicio `ApiService` para configuración
- Componente `ListaElementos` para gestión de listas dinámicas
- Uso de archivos de configuración (`appsetting.json`)
- Binding bidireccional y manejo de eventos

### 6. [RecipeManagerApp](./RecipeManagerApp)
Sistema de gestión de recetas de cocina con operaciones CRUD.

**Características principales:**
- Modelo de datos `Recipe`
- Servicio singleton `RecipeService`
- Páginas para agregar, listar y ver detalles de recetas
- Generación automática de IDs
- Navegación entre páginas con parámetros de ruta

### 7. [Rutinas_Entrenamiento](./Rutinas_Entrenamiento)
Aplicación para gestionar rutinas de entrenamiento físico.

**Características principales:**
- CRUD completo de rutinas
- Eliminación por nombre (case-insensitive)
- Modelo con propiedades: Id, Nombre, Descripción, Duración
- Servicio `RutinaService` para gestión en memoria

### 8. [TaskManagerApp](./TaskManagerApp)
Demostración de comunicación entre componentes padre-hijo.

**Características principales:**
- Comunicación padre → hijo mediante `[Parameter]`
- Comunicación hijo → padre mediante `EventCallback<T>`
- Renderizado dinámico con `@foreach`
- Gestión de estado con `StateHasChanged()`
- Patrón de eventos completo

## Tecnologías Utilizadas

*   **Blazor WebAssembly**: Framework para ejecutar aplicaciones .NET en el navegador mediante WebAssembly.
*   **Blazor Server**: Framework para aplicaciones con renderizado del lado del servidor y actualizaciones en tiempo real.
*   **SignalR**: Biblioteca para comunicación en tiempo real.
*   **ASP.NET Core**: Framework web de Microsoft.
*   **C#**: Lenguaje de programación principal.
*   **Razor**: Sintaxis para componentes de interfaz de usuario.

## Requisitos Previos

Para ejecutar cualquiera de estos proyectos necesitas:

*   [.NET SDK](https://dotnet.microsoft.com/download) (versión 6.0 o superior)
*   Visual Studio 2022, Visual Studio Code, o cualquier editor compatible con C#
*   Navegador web moderno (Chrome, Firefox, Edge, Safari)

## Cómo Usar Este Repositorio

1.  **Clonar el repositorio:**
    ```bash
    git clone <url-del-repositorio>
    cd "Blazor for Front-End Development"
    ```

2.  **Navegar a un proyecto específico:**
    ```bash
    cd <nombre-del-proyecto>
    ```

3.  **Leer el README del proyecto:**
    Cada proyecto tiene su propio README.md con instrucciones detalladas.

4.  **Ejecutar el proyecto:**
    ```bash
    dotnet restore
    dotnet run
    ```

## Conceptos Clave Cubiertos

*   ✅ **Componentes Razor**: Creación y reutilización de componentes
*   ✅ **Data Binding**: Binding unidireccional y bidireccional
*   ✅ **Validación de Formularios**: Data Annotations y validación del lado del cliente
*   ✅ **Inyección de Dependencias**: Registro y uso de servicios
*   ✅ **Gestión de Estado**: Servicios singleton y scoped
*   ✅ **Comunicación entre Componentes**: Parámetros y EventCallback
*   ✅ **SignalR**: Comunicación en tiempo real
*   ✅ **Navegación**: Routing y parámetros de ruta
*   ✅ **Renderizado Dinámico**: Listas y condicionales
*   ✅ **Configuración**: Uso de archivos de configuración

## Estructura del Repositorio

```
Blazor for Front-End Development/
├── .gitignore
├── README.md (este archivo)
├── Blazor for Front-End Development.sln
├── BlazorPerformanceApp/
│   └── README.md
├── BlazorServerApp/
│   └── README.md
├── EventEaseApp/
│   └── README.md
├── FeedbackApp/
│   └── README.md
├── Primer_Proyecto/
│   └── README.md
├── RecipeManagerApp/
│   └── README.md
├── Rutinas_Entrenamiento/
│   └── README.md
└── TaskManagerApp/
    └── README.md
```

## Recursos Adicionales

*   [Documentación oficial de Blazor](https://docs.microsoft.com/aspnet/core/blazor/)
*   [Blazor University](https://blazor-university.com/)
*   [Awesome Blazor](https://github.com/AdrienTorris/awesome-blazor)

## Licencia

Este repositorio es de uso educativo y está disponible para aprendizaje y referencia.
