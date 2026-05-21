# Sistema de Ventas

## 📋 Requisitos Previos

Antes de comenzar, asegúrate de tener instaladas las siguientes herramientas:

- **XAMPP** (PHP 8.2 o superior)
- **Composer** (Administrador de dependencias para PHP)
- **Git** (Opcional, para clonar el repositorio)

---

## 🚀 Instalación en Entorno Local

Sigue los siguientes pasos para ejecutar el proyecto en tu equipo.

### 1️⃣ Clonar el repositorio

Clona o descarga el proyecto en tu entorno local.

```bash
git clone URL_DEL_REPOSITORIO
```

O descarga el archivo ZIP y extráelo en la carpeta deseada.

---

### 2️⃣ Abrir el proyecto

Abre la carpeta del proyecto con tu editor de código favorito, por ejemplo:

- Visual Studio Code
- PHPStorm
- Sublime Text

---

### 3️⃣ Iniciar XAMPP

Abre **XAMPP Control Panel** e inicia los siguientes servicios:

- Apache
- MySQL

---

### 4️⃣ Verificar dependencias instaladas

Abre una terminal dentro del proyecto y ejecuta:

```bash
php -v
composer -v
```

✅ Ambos comandos deben ejecutarse correctamente sin mostrar errores.

---

### 5️⃣ Instalar dependencias del proyecto

Ejecuta el siguiente comando:

```bash
composer install
```

Este comando descargará e instalará todas las dependencias necesarias del proyecto.

---

### 6️⃣ Configurar variables de entorno

En la raíz del proyecto encontrarás el archivo:

```text
.env.example
```

Duplica el archivo y renómbralo a:

```text
.env
```

Luego configura los datos de tu base de datos:

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=dbsistemaventas
DB_USERNAME=root
DB_PASSWORD=
```

---

### 7️⃣ Generar la clave de la aplicación

Ejecuta:

```bash
php artisan key:generate
```

Este comando generará automáticamente la clave de seguridad de Laravel.

---

### 8️⃣ Crear la base de datos

Ingresa a:

```text
http://localhost/phpmyadmin
```

Crea una nueva base de datos llamada:

```text
dbsistemaventas
```

> Puedes utilizar otro nombre siempre que lo configures correctamente en el archivo `.env`.

---

### 9️⃣ Ejecutar las migraciones

Crea todas las tablas necesarias con:

```bash
php artisan migrate
```

---

### 🔟 Ejecutar los Seeders

Carga los datos iniciales del sistema (incluyendo el usuario administrador):

```bash
php artisan db:seed
```

> Las credenciales del usuario administrador pueden consultarse en:
>
> ```text
> database/seeders/UserSeeder.php
> ```

---

### 1️⃣1️⃣ Crear enlace simbólico para almacenamiento

Ejecuta:

```bash
php artisan storage:link
```

Esto permitirá acceder a los archivos almacenados desde la carpeta pública.

---

### 1️⃣2️⃣ Ejecutar colas de trabajo (Opcional)

Si el sistema utiliza trabajos en segundo plano, ejecuta:

```bash
php artisan queue:listen
```

---

### 1️⃣3️⃣ Iniciar el servidor local

Levanta la aplicación ejecutando:

```bash
php artisan serve
```

Laravel mostrará una URL similar a:

```text
http://127.0.0.1:8000
```

Abre esa dirección en tu navegador para acceder al sistema.

---

## ✅ Instalación Completa

Si todos los pasos se ejecutaron correctamente, el sistema estará listo para su uso en tu entorno local.

### Comandos principales

```bash
composer install
php artisan key:generate
php artisan migrate
php artisan db:seed
php artisan storage:link
php artisan serve
```

---

## 🛠 Tecnologías Utilizadas

- Laravel
- PHP 8.2+
- MySQL
- Bootstrap
- Composer
- XAMPP

---

## 📄 Licencia

Este proyecto es de uso académico y/o empresarial según las políticas definidas por sus autores.