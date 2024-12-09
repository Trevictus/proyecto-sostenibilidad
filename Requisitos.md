## Raspberry Pi
- Cualquier modelo puede valer aunque cada modelo tiene unas características diferentes.
  - Consumo de Raspberry Pi Zero: entre 100mA y 150mA.
  - Pi 4: entre 600mA hasta 1A.
- Necesitará una fuente de alimentación ecológica, en este caso utilizaremos un panel solar.
- Se puede conectar a una batería recargable para que pueda operar sin necesidad de panel solar.
- Para el SO hay varias opciones, aunque pensamos que la más correcta por su bajo consumo sería una sin GUI
  - Raspberry Pi OS: Más pesado que los otros dos al incluir, entre otras, una GUI.
  - RaspBian Lite: Versión ligera y sin GUI de la Raspberry PI OS. Suele usarse para servidores. Impacto mínimo en recursos.
  - DietPi: Optimizado especificamente para dispositivos de bajo consumo, sin GUI por defecto. Más pequeño que Raspbian Lite
- Opciones a tener en cuenta para reducir aún mas el consumo de de energía de la Raspberry Pi:
  - Deshabilitar HDMI, puertos USB que no se usen o LEDS.

## HTTP/2 para el servidor.
- HTTP/2 es una versión más eficiente de HTTP que permite la multiplexación de múltiples solicitudes sobre una sola conexión TCP, 
reduciendo la latencia y mejorando el rendimiento del servidor. Esto puede llevar a un menor uso de recursos y, por ende, a una menor huella de carbono si se implementa correctamente.

### Instalación del Servidor Web:
Primero, hay que instalar un servidor web como Apache en la Raspberry Pi.

### Instalación de SSL/TLS:
Utilizamos Let's Encrypt para obtener certificados SSL gratuitos. Configuramos SSL/TLS, ya que HTTP/2 requiere una conexión segura. 

### Configuración de HTTP/2 para Apache:
- sudo a2enmod http2
- sudo systemctl restart apache2

Luego, habilitar HTTP/2 en la configuración de tu sitio.

Verificamos que HTTP/2 está funcionando utilizando herramientas como curl con el parámetro --http2, o verificando en el navegador con herramientas de desarrollo.
