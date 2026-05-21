## Dependencias

Antes de comenzar, asegúrate de tener instaladas las siguientes herramientas:
* **XAMPP** (con versión de PHP 8.2 o superior).
* **Composer** (Gestor de dependencias de PHP).

---

## Cómo instalar en Local

Sigue estos pasos para configurar y ejecutar el proyecto en tu máquina local:

1. **Clonar el repositorio:** Clona o descarga el repositorio a una carpeta en tu entorno local.
2. **Abrir el editor:** Abre el repositorio en tu editor de código favorito (por ejemplo, Visual Studio Code).
3. **Iniciar servicios:** Ejecuta la aplicación XAMPP e inicia los módulos de **Apache** y **MySQL**.
4. **Verificar dependencias:** Abre una nueva terminal en tu editor y comprueba que tienes instaladas las dependencias correctamente ejecutando:
   ```bash
   php -v
   composer -v
(Ambos comandos deberán ejecutarse correctamente sin mostrar errores).

Instalar dependencias del proyecto: Ejecuta el siguiente comando para instalar todas las librerías necesarias de Composer:

Bash
composer install
Configurar el entorno: En el directorio raíz encontrarás el archivo .env.example. Duplícalo y renómbralo como .env. Modifica este nuevo archivo con la configuración de tu base de datos para que quede así:

Fragmento de código
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=dbsistemaventas
DB_USERNAME=root
DB_PASSWORD=
Generar la clave de la aplicación: Ejecuta el comando para crear la Key de seguridad de Laravel:

Bash
php artisan key:generate
Crear la base de datos: Ingresa a tu administrador de phpMyAdmin (generalmente en http://localhost/phpmyadmin) y crea una nueva base de datos. El nombre es opcional, pero por defecto debes nombrarla dbsistemaventas.

Correr las migraciones: Crea las tablas en tu base de datos ejecutando:

Bash
php artisan migrate
Ejecutar los seeders: Esto creará la información por defecto, incluido un usuario administrador. (Puedes revisar las credenciales en el archivo database/seeders/UserSeeder):

Bash
php artisan db:seed
Crear enlace simbólico: Ejecuta este comando para enlazar la carpeta pública con el almacenamiento:

Bash
php artisan storage:link
Ejecutar los trabajos en segundo plano (Opcional - Modo Desarrollo): Si el sistema maneja colas de trabajos, ejecuta:

Bash
php artisan queue:listen
Iniciar el servidor local: En una nueva terminal, levanta el proyecto ejecutando:

Bash
php artisan serve