# Guía de Instalación y Configuración en Raspberry Pi (Con APACHE)

## Requisitos previos

- Raspberry Pi con Raspbian OS (o Raspberry Pi OS) instalado.
- Conexión a internet.
- Acceso a la terminal (ya sea de manera local o mediante SSH).

## Primeros pasos (Instalación y configuración con Apache)

### 1. Habilitar SSH en la Raspberry Pi (si aún no está habilitado)

Para acceder de forma remota a tu Raspberry Pi, necesitas habilitar SSH. Sigue estos pasos:

1. Ejecuta `sudo raspi-config`.
2. Dirígete a "Advanced Options" > "SSH" y habilítalo.

### 2. Actualizar los paquetes del sistema

Es importante mantener el sistema actualizado. Abre la terminal y ejecuta:

```bash
sudo apt-get update && sudo apt-get upgrade -y
```

### 3. Instalar APACHE

```bash
sudo apt-get install apache2 -y
```

### 4. Crear un archivo index.html (sudo nano /var/www/html/index.html).

```bash
sudo nano /var/www/html/index.html
```

### 5. Obtener la IP de la Raspberry Pi

Para encontrar la dirección IP de la Raspberry Pi, ejecutamos `ifconfig`.
La IP está bajo la sección `inet` (generalmente en la interfaz `eth0` o `wlan0` dependiendo de si estamos conectados por cable o Wi-Fi).

La IP estará bajo la sección inet (generalmente en la interfaz eth0 o wlan0 dependiendo de si estás conectado por cable o Wi-Fi).

### 6. Verificar el servidor desde otro dispositivo

```
http://<IP-de-la-RaspberryPi>/
```

### 7. Conectar mediante SSH + FTP

Para conectarte remotamente a la Raspberry Pi desde otro ordenador, podemos usar una herramienta como Putty (Windows) o simplemente la terminal en Linux o macOS con el siguiente comando:

```bash
ssh pi@<IP-de-tu-RaspberryPi>
```

### 8. Subir y actualizar la página web automáticamente utilizando Git
1. Utilizar git en la raspberry
2. Crear script bash que automatice los pulls cuando se inicie la raspberry y cada x tiempo.


## Errores
1. Reset de PWD (por si cambiaron la pwd):
    sudo -i command + Enter.
    passwd -e username.
2. Si hay problemas de fingerprint a la hora de conectar por SSH, borramos el server del archivo según el enlace proporionado por terminal.
