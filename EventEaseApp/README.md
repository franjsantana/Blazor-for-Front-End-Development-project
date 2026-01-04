# EventEaseApp

EventEaseApp es una aplicación moderna de gestión de eventos construida con **Blazor WebAssembly** y **.NET 9**. Permite a los usuarios explorar eventos, registrarse y gestionar su asistencia de manera eficiente.

## Características

- **Listado de Eventos**: Visualización optimizada de eventos utilizando virtualización para un alto rendimiento.
- **Registro de Eventos**: Formulario de registro sencillo e intuitivo para los asistentes.
- **Seguimiento de Asistencia**: Sistema para registrar y monitorear la asistencia a los eventos.
- **Gestión de Sesiones**: Manejo de estado de sesión de usuario para una experiencia personalizada.

## Tecnologías Utilizadas

- **.NET 9.0**: La última versión del framework de desarrollo de Microsoft.
- **Blazor WebAssembly**: Para construir interfaces web interactivas del lado del cliente con C#.
- **Bootstrap**: Para un diseño responsivo y moderno.

## Comenzando

Sigue estos pasos para configurar y ejecutar el proyecto localmente.

### Prerrequisitos

- [.NET 9.0 SDK](https://dotnet.microsoft.com/download/dotnet/9.0)

### Instalación

1. Clona el repositorio:
   ```bash
   git clone <URL_DEL_REPOSITORIO>
   ```
2. Navega al directorio del proyecto:
   ```bash
   cd EventEaseApp
   ```
3. Restaura las dependencias:
   ```bash
   dotnet restore
   ```

### Ejecución

Para iniciar la aplicación en modo de desarrollo:

```bash
cd EventEaseApp
dotnet watch
```

La aplicación estará disponible típicamente en `http://localhost:5000` o `https://localhost:5001` (consulta la salida de la consola para la URL exacta).

## Estructura del Proyecto

- **Pages**: Contiene las páginas Razor (vistas) de la aplicación (`Events.razor`, `EventRegister.razor`, etc.).
- **Components**: Componentes reutilizables de la interfaz de usuario.
- **Services**: Lógica de negocio y servicios (`AttendanceService`, `UserSessionState`).
- **Models**: Definiciones de datos y modelos (`Event`, `Registration`).
- **wwwroot**: Archivos estáticos (CSS, imágenes, JS).

---
Desarrollado con ❤️ usando Blazor.
