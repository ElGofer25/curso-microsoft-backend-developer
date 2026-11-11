# Módulo 1

## Por qué usar C# en back-end

El **back-end** es la parte de una aplicación que se ejecuta en un servidor:
procesa peticiones, aplica reglas de negocio y accede a los datos. **C#** es un
lenguaje de programación de Microsoft que se ejecuta sobre **.NET**, la
plataforma que incluye el *runtime* (el programa que ejecuta tu código) y un
conjunto de bibliotecas listas para usar.

### Razones principales

- **Integración con .NET y ASP.NET Core.** ASP.NET Core es el framework de .NET
  para crear aplicaciones web y APIs. Al ser de la misma plataforma, incluye de
  fábrica herramientas comunes como autenticación y manejo de peticiones HTTP.
- **Multiplataforma.** .NET funciona en Windows, macOS y Linux, así que el mismo
  servicio puede desarrollarse en tu equipo y desplegarse en cualquier servidor
  o servicio en la nube. (Antes se llamaba ".NET Core"; hoy se le llama
  simplemente ".NET".)
- **Tipado estático y orientación a objetos.** En C# cada variable tiene un tipo
  fijo (número, texto, etc.) y el compilador revisa que se use bien *antes* de
  ejecutar el programa. Así se detectan
  errores al compilar y no cuando la aplicación ya está en uso. La orientación a
  objetos organiza el código en clases, lo que facilita mantenerlo.
- **Ecosistema amplio.** Existen muchas bibliotecas, herramientas y una gran
  comunidad, por lo que es fácil encontrar documentación y soluciones.

### Ejemplo: el compilador detecta el error

```csharp
int edad = 25;          // `edad` solo puede guardar números enteros

// edad = "veinte";     // Error de compilación: no se puede convertir
                        // 'string' a 'int'. El programa ni siquiera arranca.

Console.WriteLine(edad); // Muestra: 25
```

## Introducción a GitHub

### Git y GitHub no son lo mismo

- **Git** es un sistema de **control de versiones**: guarda el historial de cambios
  de tu código para que puedas ver qué cambió, cuándo y volver a una versión
  anterior. Funciona en tu computadora, incluso sin internet.
- **GitHub** es un servicio en internet que aloja repositorios Git y añade
  herramientas para colaborar.

Un **repositorio** es la carpeta de un proyecto junto con todo su historial.

### Qué ofrece GitHub

- **Colaboración.** Varias personas trabajan en el mismo proyecto sin pisarse:
  cada una propone sus cambios en una rama (*branch*) y los envía mediante un
  **pull request**, una solicitud para incorporarlos al proyecto principal.
  Antes de aceptarlos, otros pueden revisarlos y comentarlos (*code review*).
  Los **issues** sirven para registrar errores, tareas o ideas.
- **Integración.** Se conecta con editores como Visual Studio Code y con
  servicios en la nube, lo que permite automatizar pruebas y despliegues.
- **Código abierto (*open source*).** Aloja millones de proyectos públicos que
  puedes consultar, usar o a los que puedes contribuir.

### Flujo básico con Git

```bash
git init                         # Crea un repositorio en la carpeta actual
git add .                        # Prepara todos los cambios para guardarlos
git commit -m "Primer commit"    # Guarda una versión (commit) con un mensaje
git remote add origin <URL>      # Vincula el repositorio con el de GitHub (solo la primera vez)
git push -u origin main          # Envía los commits a GitHub
```

Cada `commit` es un punto del historial al que puedes volver. `git push` es lo
que sube ese historial a GitHub para compartirlo.
