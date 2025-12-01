<div id="user-content-toc">
  <ul align="center">
    <summary><h1 style="display: inline-block"> Trabajo Practico Final📄✨
 </h1></summary>
    <summary><h1 style="display: inline-block">Gandur-Garcia-Gramajo-equipo-Tr3G :man_technologist: </h1></summary>
  </ul>
</div>
  <ul align="center">

  🐧 Arquitectura y Sistemas Operativos

UTN - FRA -    DIV 313-2

  ---

  # 👥 Integrantes del Equipo
<ul align="left">

  👨‍💼 [Administrador Kevin Gramajo](https://github.com/kevingramajo)

  👩‍💻 [Desarrollador Enzo Garcia](https://github.com/EnzoMatiasGG)

  👷 [Operador Joaquin Gandur](https://github.com/Joaqko0)
<u align="center">
  
  ##  Tecnologías Utilizadas 🧩
<u align="left">

- Vagrant + VirtualBox / QEMU
- Linux Ubuntu Server (Jammy 22.04)
- Git y GitHub
- LVM – Logical Volume Manager
- Docker & Docker Compose
- Nginx, Redis, Postgres
- Prometheus, Loki y Grafana
- Servidor LAMP

<u align="center">
  
## Desarrollo del Trabajo 📝

<u align="left">
  
🔍 0. **Descubrimiento de la IP de la VM**
  
Las IP registradas se encuentran en:

📄 informacion/ip_vm.txt


🏗️ 1. **Configuración Inicial y Repositorio Git**

- Creación del repositorio remoto.
- 
- Clonado del repositorio por cada integrante.
- 
- Configuración de Git en cada VM.


⚙️ 2. **Fastfetch Colaborativo**

Cada alumno generó su salida de fastfetch y la añadió al archivo:

📄 informacion/system_info.txt

**🔐 3. Gestión de Permisos y Usuarios**

Incluye:

- Creación de directorio personal.

- Archivos con permisos privados (600) y públicos (644).

- Creación de usuarios locales.

- Creación del grupo equipotrabajo.

- Directorio colaborativo con permisos (770).

📄 Verificaciones:

permisos/usuarios_[apellido].txt

permisos/verificacion_permisos.txt

**💾 4. Administración de LVM**

- Cada integrante:
- Detectó el disco.
- Creó PV, VG, LV.
- Formateó, montó y configuró fstab.

📄 Verificación completa en:

lvm/lvm-[apellido].txt

Incluye:
- Estado sin montar
- Estado montado
- pvscan / vgscan / lvscan

lvscan

**📁 5. Gestión de Archivos y Directorios**

Se creó la estructura:

<img width="534" height="320" alt="image" src="https://github.com/user-attachments/assets/da9f228b-e68e-41a4-95d0-03fce0ef18f9" />

Operaciones realizadas:

Crear 10 archivos.

Copiar 1–5.

Mover 6–8.

Respaldar 9–10.

Limpiar temporal 9-10.

📄 Verificación:

archivos/verificacion_archivos.txt

**🐳 6. Contenedores y Monitoreo con Docker Compose**

Se configuraron y corrigieron servicios:

- Nginx
- Redis
- Postgres
- Prometheus
- Loki
- Grafana

Se resolvieron errores intencionales del archivo original:

Verificaciones:

- docker ps
- docker-compose ps
- Redes y volúmenes de Docker
- Logs completos

📄 Archivo completo:

contenedores/verificacion_contenedores.txt

**⭐ 7 Bonus: Servidor LAMP**

Se documento:

- Instalación de Apache, MySQL y PHP
- Creación de base de datos
- Archivos index.html, info.php, test_db.php
- Verificación de servicios

📄 Archivos en:

lamp/verificacion_lamp.txt

# 📘 Conclusiones

 El Trabajo Practico en ciertos puntos es sencillo, al principio cuesta acostumbrarse a una interfaz diferente a la habitual, pero te terminas acostumbrando a los comandos y termina siendo lo habitual que se utiliza con el raton y el teclado diariamente en windows, al final resulta facil y agradable moverse por el repositorio con los comandos mas comunes cd / ls / touch / nano / rm /.
  La parte


  
