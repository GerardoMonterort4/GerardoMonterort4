# 🐾 Mascotas Perdidas — Política de Respaldo y Automatización

Documentación correspondiente al proyecto desarrollado en la asignatura **Programación** del grupo **Informática TA3**.

---

## 🎓 Información académica

- **Universidad:** Universidad del Trabajo del Uruguay
- **Instituto:** Instituto Tecnológico de Informática
- **Asignatura:** Programación  
- **Tutor:** Profesor Damián Pajares  
- **Autor:** Alumno Gerardo Montero  
- **Grupo:** Informática TA3

---

## 🛡️ Política de respaldo de base de datos

### 📍 Entornos utilizados

- Ubuntu 22.04 LTS (WSL)
- MariaDB / MySQL
- XAMPP en Windows
- phpMyAdmin

### 🔁 Procedimiento básico con `mysqldump`

#### 🔹 En Ubuntu:
```bash
mysqldump -u gerardo -p mydb2 > ~/backups/mydb2.sql

##🔹 En Windows (XAMPP):
cd C:\xampp\mysql\bin
.\mysqldump.exe -u root -p mydb2 > "C:\Users\Gerardo\backups\mydb2.sql"


### 📂 Restauración desde phpMyAdmin
- Acceder a http://localhost/phpmyadmin
- Crear la base mydb2 o Mysqlhito3
- Ir a pestaña Importar y subir el .sql

---

### 🧪 Script Bash de respaldo
Archivo: respaldo.sh
#!/bin/bash
echo "hola"
echo "mundo"
echo "Se ejecuta un script en bash a la base de datos mydb2"
echo "Fin del script"


Permisos y ejecución:
chmod +x respaldo.sh
./respaldo.sh

---

## 📦 Registro de sistema y reinstalación
rpm -qa | sort > pkgs.txt
cat pkgs.txt >> respaldo.sh
sudo dnf reinstall $pkgs

---

## 🗜️ Compresión y transferencia
Comprimir:
tar -cvzf directorioTA3.tar.gz directorioTA3


Transferir remoto con scp:
scp -P 3306 /local2/mydb2/usuario.sql gerardo@SERVER-K3Q7H7D:/Download/


## ⏱️ Automatización con crontab
Agregado en crontab -e:
* * * * * cd ~/Escritorio && ./script.sh

Script de ejemplo:
#!/bin/bash
mv mover.txt ~/mydb2/


Ver cron activo:
crontab -l

## 🌐 Visualización en HTML (Chrome)
Archivo chrome.html:
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>PROGRAMACION MOSTRAR UN CHROME</title>
  <link rel="stylesheet" href="css/style.css">
</head>
<body>
  <header>
    <nav>
      <h1 class="logo">GMC</h1>
      <ul>
        <li><a href="index.html" class="current">Home</a></li>
        <li><a href="product.html">Product</a></li>
        <li><a href="about.html">About</a></li>
        <li><a href="contact.html">Contact</a></li>
      </ul>
    </nav>
    <h2>MOSTRAR UN CHROME</h2>
    <img src="img/product-1.jpg" alt="">
    <img src="img/product-3.jpg" alt="">
  </header>
  <footer>
    <a href="https://twitter.com/gmontero">Follow @gmontero</a>
  </footer>
</body>
</html>

---

## 📘 Observaciones finales
Este archivo README.md resume la política de respaldo, automatización,
gestión de paquetes, compresión, visualización HTML y documentación del sistema utilizada en el proyecto,
integrando scripting, base de datos y procesos remotos.

🔗 Repositorio del proyecto en GitHub




