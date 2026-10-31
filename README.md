🛒 RetailPro – Sistema de Gestión y Análisis de Ventas
📌 Descripción del proyecto
RetailPro es un proyecto de diseño y desarrollo de una base de datos relacional orientada a la gestión de ventas de una empresa comercializadora de productos tecnológicos.
El objetivo es centralizar y organizar la información de clientes, productos, categorías y operaciones de venta, permitiendo mantener la integridad de los datos y facilitar futuras consultas y análisis comerciales.
El proyecto utiliza SQL para crear la estructura de la base de datos, establecer relaciones entre tablas, insertar registros de ejemplo y realizar consultas para visualizar la información almacenada.
🎯 Objetivos
•	Diseñar una base de datos relacional para gestionar las operaciones comerciales.
•	Organizar la información de clientes, productos y categorías.
•	Registrar las transacciones de venta.
•	Establecer relaciones entre las entidades mediante claves primarias y foráneas.
•	Aplicar restricciones para mantener la integridad de los datos.
•	Realizar consultas SQL para recuperar y analizar información.
Diseñar una estructura de base de datos que reduzca redundancia y evite inconsistencias.
🗄️ Modelo de datos
La base de datos se denomina ventas_tech_db y está compuesta por cuatro tablas principales:
Tabla	Descripción
categorias	Almacena las categorías de productos tecnológicos.
clientes	Contiene los datos personales y de registro de los clientes.
productos	Registra los productos, sus precios, categorías y stock.
ventas	Almacena las operaciones comerciales realizadas.
La tabla ventas es la tabla de hecho y recomendaría realizar un mearge para la tabla categoría
Relaciones entre tablas
•	Cada producto pertenece a una categoría.
•	Cada venta está asociada a un cliente.
•	Cada venta registra el producto comercializado.
•	Las relaciones se implementan mediante claves foráneas (FOREIGN KEY).
Diagrama conceptual
text
CATEGORIAS (1) ───── (N) PRODUCTOS

PRODUCTOS  (1) ───── (N) VENTAS

CLIENTES   (1) ───── (N) VENTAS

🛠️ Tecnologías y herramientas utilizadas
•	SQL: lenguaje utilizado para crear, modificar, consultar y administrar la base de datos.
•	Microsoft SQL Server: motor de base de datos compatible con los tipos de datos y las instrucciones utilizadas en el proyecto.
•	SQL Server Management Studio (SSMS) o Azure Data Studio: herramientas recomendadas para ejecutar y administrar los scripts SQL.
•	GitHub: plataforma utilizada para almacenar, versionar y compartir el código del proyecto.
📂 Estructura del repositorio
text
Ventas_tech_db/
│
├── Ventas_tech_db.sql
│
└── README.md
•	Ventas_tech_db.sql: script principal que contiene la creación de la base de datos, las tablas, las relaciones, la inserción de datos y las consultas de verificación.
•	README.md: documentación general del proyecto e instrucciones de ejecución.
⚙️ Cómo ejecutar el proyecto
1. Requisitos previos
Antes de comenzar, es necesario contar con:
•	Microsoft SQL Server instalado y en funcionamiento.
•	SQL Server Management Studio (SSMS) o Azure Data Studio.
•	Acceso al repositorio de GitHub.
2. Descargar el repositorio
Clonar el repositorio desde una terminal:
bash
git clone https://github.com/ceciliagceres-ctrl/Ventas_tech_db.git
Ingresar a la carpeta:
bash
cd Ventas_tech_db
3. Abrir el script SQL
Abrir SQL Server Management Studio y conectarse a una instancia de SQL Server.
Luego:
1.	Seleccionar File → Open → File.
2.	Buscar el archivo Ventas_tech_db.sql.
3.	Abrir el script en una nueva ventana de consulta.
4. Ejecutar el script
Antes de ejecutarlo, verificar que las instrucciones CREATE TABLE no tengan comas finales antes del cierre de cada definición de tabla.
Una vez realizada esta comprobación:
1.	Ejecutar el script completo con el botón Execute o la tecla F5.
2.	Esperar a que finalice la ejecución.
3.	Verificar que no aparezcan errores en la pestaña Messages.
El script realiza las siguientes operaciones:
•	Creación de la base de datos ventas_tech_db.
•	Selección de la base de datos mediante USE.
•	Eliminación de tablas existentes para permitir recrearlas.
•	Creación de las cuatro tablas principales.
•	Definición de claves primarias y foráneas.
•	Inserción de registros de ejemplo.
•	Ejecución de consultas SELECT para comprobar los datos.
Importante: el script está preparado para SQL Server. Si se ejecuta más de una vez, elimina y vuelve a crear las tablas, por lo que los datos anteriores serán reemplazados.
5. Verificar los resultados
Al finalizar, ejecutar las siguientes consultas para comprobar que los registros se hayan cargado correctamente:
sql
USE ventas_tech_db;

SELECT * FROM categorias;

SELECT * FROM clientes;

SELECT * FROM productos;

SELECT * FROM ventas;
📊 Datos de ejemplo
El proyecto incluye información ficticia para simular las operaciones de una tienda de tecnología.
Entre los datos incorporados se encuentran:
•	Categorías: Computación, Accesorios, Audio y Almacenamiento.
•	Clientes registrados en distintas ciudades de Argentina.
•	Productos como laptops, monitores, auriculares, teclados y dispositivos de almacenamiento.
•	Operaciones de venta realizadas durante marzo de 2024.
Estos registros permiten probar el funcionamiento de las relaciones y realizar consultas sobre las operaciones comerciales.
🚀 Posibles mejoras futuras
Como futuras etapas de desarrollo, RetailPro puede ampliarse incorporando:
•	Consultas SQL avanzadas para analizar ingresos y volúmenes de ventas.
•	Reportes de productos más vendidos.
•	Análisis de ventas por cliente, categoría y período.
•	Control y actualización automática del stock.
•	Procedimientos almacenados y vistas.
•	Indicadores clave de rendimiento (KPIs).
•	Integración con herramientas de visualización de datos como Power BI.
