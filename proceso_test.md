# Pasos a seguir (en el SO default por ahora)

## Primeros pasos (con APACHE por ahora)
*IMPORTANTE* sudo raspi-config + Advanced options + SSH

1. Primero y fundamental, update de paquetes con 'apt-get update' y 'apt-get upgrade'.
2. Instalar APACHE (sudo apt-get install apache2).
3. Creamos un index.html (sudo nano /var/www/html/index.html).
4. Averiguamos IP de la Raspberry con ifconfig.
5. Verificamos que la web funciona desde otro ordenador (http://IP/index.html).

## Conectar mediante SSH + FTP

1. Descargamos Putty o conectamos mediante consola de ubuntu por ssh.
2. Instalamos FileZilla en nuestro master.
3. Hacemos uso de SFTP mediante IP + USER + PWD + PORT 22.
4. Navegamos a directorio var www html y subimos fichero (si fallo de permisos: chown -R www-data:www-data /var/www/html + usermod -g www-data pi + chmod -R 770 /var/www)

## Maybe sin FTP para menos consumo y automatización

1. Utilizar git en la raspberry
2. Crear script bash que automatice los pulls cuando se inicie la raspberry y cada x tiempo.

## Errores
1. Reset de PWD (por si cambiaron la pwd):
    sudo -i command + Enter.
    passwd -e username.
