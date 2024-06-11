SISTEMA WEB PARA EL CONTROL ESCOLAR DE LA UNIVERSIDAD AUTÓNOMA COMUNAL DE OAXACA
Clonar el repositorio
git clone https://github.com/Fepsali-Perez/SISTEMA-UACO.git

Instalar dependencias para el backend
cd backend_uaco
composer install

Instalar dependencias para el frontend
cd frontend_uaco
npm install


Configurar el archivo .env para la conexión con la base de datos. Copia .env.example a .env:
cp .env.example .env

Configuracion inicial de la base de datos.
Abre MySQL Workbench o tu herramienta preferida de administración de bases de datos.
Crear una base de datos. Ejemplo:
CREATE DATABASE uaco;

Abre el archivo .env y configura las siguientes líneas para reflejar tu configuración de base de datos
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nombre_de_la_base_de_datos
DB_USERNAME=nombre_de_usuario 
DB_PASSWORD=contraseña
Asegúrate de reemplazar nombre_de_la_base_de_datos, nombre_de_usuario, y contraseña con la información de tu base de datos.

Ejecutar las migraciones para crear las tablas en la base de datos:
php artisan migrate

Ejecutar el servidor de desarrollo para el backend
cd backend_uaco
php artisan serve

Ejecutar el servidor de desarrollo para el frontend
cd frontend_uaco
npm run dev
