# Primer Parcial - API REST de Gestión de Clientes

## Descripción del proyecto
Este proyecto es una API REST desarrollada para administrar los clientes de una empresa, permitiendo realizar operaciones CRUD (Crear, Leer, Actualizar y Eliminar). La solución está estructurada en capas separando responsabilidades (Controllers, Services, Repositories, Models y Data) y aplica los principios de Inyección de Dependencias y persistencia de datos mediante Entity Framework Core.

## Tecnologías utilizadas
- Visual Basic .NET
- ASP.NET Core Web API
- Entity Framework Core
- Microsoft SQL Server

## Descripción de los endpoints
La API expone los siguientes endpoints bajo la ruta principal `/api/clientes`:

* **`GET /api/clientes`** : Devuelve una lista con todos los clientes registrados en la base de datos.
* **`GET /api/clientes/{id}`** : Obtiene los detalles de un cliente específico según su ID.
* **`POST /api/clientes`** : Registra un nuevo cliente en el sistema. Requiere un objeto JSON con los datos del cliente (Nombre, Apellido, Email, Telefono).
* **`PUT /api/clientes/{id}`** : Modifica los datos de un cliente existente. Requiere el ID en la URL y los datos actualizados en el cuerpo de la petición.
* **`DELETE /api/clientes/{id}`** : Elimina un cliente de la base de datos utilizando su ID.

## Instrucciones necesarias para ejecutar el proyecto
1. **Clonar el repositorio:** Descarga o clona este repositorio en tu máquina local.
2. **Preparar la Base de Datos:** Abre SQL Server Management Studio (SSMS) y ejecuta el script `script_db.sql` incluido en el repositorio para crear la base de datos `EmpresaDB` y la tabla `Clientes`.
3. **Configurar la conexión:** Abre el archivo `appsettings.json` en Visual Studio y verifica que la cadena de conexión (`DefaultConnection`) apunte a tu instancia local de SQL Server (por ejemplo, `localhost\SQLEXPRESS`).
4. **Ejecutar el proyecto:** Abre la solución en Visual Studio 2022 y presiona `F5` (o el botón de Iniciar depuración).
5. **Probar la API:** Puedes probar los endpoints utilizando un navegador web para las peticiones GET (accediendo a `https://localhost:<puerto>/api/clientes`) o utilizar herramientas como Postman para probar el flujo CRUD completo (POST, PUT y DELETE).
