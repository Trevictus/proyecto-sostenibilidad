## Raspberry Pi
- Cualquier modelo puede valer aunque cada modelo tiene unas características diferentes.
- Necesitará una fuente de alimentación ecológica, en este caso utilizaremos un panel solar.
- Se puede conectar a una batería recargable para que opere sin necesidad de panel solar.

## HTTP/2 para el servidor.
- HTTP/2 es una versión más eficiente de HTTP que permite la multiplexación de múltiples solicitudes sobre una sola conexión TCP, 
reduciendo la latencia y mejorando el rendimiento del servidor. Esto puede llevar a un menor uso de recursos y, por ende, a una menor huella de carbono si se implementa correctamente.

### Instalación del Servidor Web:
Primero, hay que instalar un servidor web como Apache en la Raspberry Pi.

### Instalación de SSL/TLS:
Utilizamos Let's Encrypt para obtener certificados SSL gratuitos. Configuramos SSL/TLS, ya que HTTP/2 requiere una conexión segura. 

### Configuración de HTTP/2 para Apache:
sudo a2enmod http2
sudo systemctl restart apache2

Luego, habilitar HTTP/2 en la configuración de tu sitio.

Verificamos que HTTP/2 está funcionando utilizando herramientas como curl con el parámetro --http2, o verificando en el navegador con herramientas de desarrollo.
