#  Laboratorio #2 – Implementación de Login en Laravel

##  Desarrollo Web VII

**Universidad Tecnológica de Panamá**
**Facultad de Ingeniería de Sistemas Computacionales**

---

##  Objetivo del Laboratorio

Implementar un sistema de autenticación (login y registro) utilizando **Laravel**, aplicando la arquitectura Modelo-Vista-Controlador (MVC).

---

## 🔧 Requisitos Previos

Para la ejecución del laboratorio se utilizó el siguiente entorno:

* PHP 8.3
* Composer (última versión)
* Laravel Installer
* WampServer (Apache + MySQL)
* Servidor Web: Apache
* Base de datos: MySQL
* Editor de código: Visual Studio Code
* Node.js y NPM
* Sistema Operativo: Windows 10

---

## ⚙️ Instalación y Comandos Utilizados

```bash
composer create-project laravel/laravel pruebaregistrolaravel
cd pruebaregistrolaravel

composer require laravel/ui
php artisan ui bootstrap --auth

npm install
npm run dev

php artisan migrate
php artisan serve
```

---

##  Arquitectura MVC en Laravel

Laravel utiliza el patrón MVC:

* **Modelo (Modelos):** Representan la estructura de la base de datos
   `app/Models`

* **Vista (Views):** Interfaz de usuario (Blade)
  `resources/views`

* **Controlador (Controllers):** Lógica de la aplicación
   `app/Http/Controllers`

* **Rutas:** Definen la navegación del sistema
   `routes/web.php`

---

##  Base de Datos

Se utilizó MySQL mediante WAMP.

### 📄 Configuración del archivo `.env`

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=pruebaregistrolaravel
DB_USERNAME=root
DB_PASSWORD=
```

###  Migraciones

```bash
php artisan migrate
```

Se generaron tablas como:

* users
* password_resets
* failed_jobs

---

##  Resultado del Laboratorio

Se implementó correctamente el sistema de autenticación:

* Registro de usuario
* Inicio de sesión
![image alt](https://github.com/Gabriel2025k/documentacion1/blob/494be486065dd273d01b87e3a5e99721c7fd0bf2/login.png.png)
![image alt](https://github.com/Gabriel2025k/documentacion1/blob/c419c07bcb7af3b6ffda1eae26bff64b4421dfcf/loginsucc.png.png)
![image alt](https://github.com/Gabriel2025k/documentacion1/blob/7b12dfc7eb549fbc58162eac902cd7109db9f22d/registro.png.png)



```md
![Login](ruta_imagen_login)
![Registro](ruta_imagen_registro)
```

---

##  Dificultades y Soluciones

Durante el desarrollo del laboratorio se presentaron los siguientes problemas:

### 1. Error de versión de PHP

Se requería PHP 8.2 o superior
✔ Solución: Configurar correctamente el PATH con PHP 8.3 de WAMP

---

### 2. Error con Laravel Installer

✔ Solución: Actualizar PHP y usar Composer correctamente

---

### 3. Error "Schema not found"

✔ Solución:

```php
use Illuminate\Support\Facades\Schema;
Schema::defaultStringLength(191);
```

---

### 4. Error de base de datos

✔ Solución:

* Crear la base en phpMyAdmin
* Configurar `.env`

---

### 5. Error "No application encryption key has been specified"

✔ Solución:

```bash
php artisan key:generate
```

---

### 6. Error con npm

✔ Solución:

* Instalar Node.js
* Agregar al PATH

---

##  Referencias

* https://laravel.com/docs
* https://getcomposer.org
* https://nodejs.org

---

##  Fecha de Ejecución

Abril 2026

---

##  Información del Estudiante

Este laboratorio ha sido desarrollado por:

Nombre: TU NOMBRE
Correo: TU CORREO
Curso: Desarrollo Web VII
Instructor: Irina Fong

---
