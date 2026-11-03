# Informe de Auditoría de Red Wi-Fi Insegura

**Asignatura:** Ciberseguridad
**Alumno:** Juan Manuel Diaz
**Comisión:** 105720

## Introducción
En esta práctica hice un análisis de tráfico de una conexión no segura para ver exactamente qué información queda expuesta cuando navegamos en una red Wi-Fi pública sin protección. La idea es entender los riesgos reales y ver cómo solucionarlos.

## Sitio analizado
- **URL:** http://neverssl.com
- **¿Por qué este sitio?:** Es una página web diseñada a propósito sin cifrado, lo que la hace perfecta para hacer pruebas de red y ver cómo viajan los datos en texto plano.

## Evidencia observada
Al revisar la primera solicitud desde la pestaña Network de las herramientas de desarrollador, capturé los siguientes datos:
- **URL solicitada:** http://majesticfreshshiningkiss.neverssl.com/online
- **Método HTTP:** GET
- **Host:** majesticfreshshiningkiss.neverssl.com
- **Protocolo:** HTTP
- **User-Agent:** Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/156.0.0.0 Safari/537.36

## Riesgos encontrados
Si alguien estuviera espiando la red (por ejemplo, en un café o aeropuerto), esto es lo que podría pasar:
1. **Todo viaja en texto plano:** Como el sitio usa HTTP normal, la información no va cifrada.
2. **Exposición total:** Cualquier persona conectada a la misma red usando un programa para capturar paquetes podría ver exactamente qué páginas estoy visitando.
3. **Huella del dispositivo:** A través del *User-Agent*, el atacante ya sabe qué sistema operativo uso y qué navegador tengo. Esto le sirve para buscar vulnerabilidades específicas de mi equipo. Si hubiera enviado una contraseña o una cookie, también la habría visto sin esfuerzo.

## ¿Cómo nos ayuda una VPN?
Si hubiera puesto una VPN antes de hacer esto, la historia sería muy distinta:
- **Cifrado real:** Todo el tráfico saldría de mi computadora ya encriptado.
- **Túnel invisible:** El atacante en la red pública solo vería que estoy conectado a un servidor VPN, pero no tendría idea de que estoy visitando "neverssl.com" ni qué estoy haciendo ahí.
- **Privacidad garantizada:** Toda esa evidencia sería solo una sopa de letras indescifrable para quien intente espiar.

## Mis 3 Reglas para redes Wi-Fi públicas
1. Si estoy en el Wi-Fi de un aeropuerto, plaza o café, nunca entro al banco ni pago nada a menos que tenga mi VPN encendida.
2. Siempre reviso que aparezca (HTTPS) en la barra de direcciones antes de escribir un usuario o contraseña en cualquier lado.
3. Tengo desactivada la opción del celular y la computadora que se conecta automáticamente a cualquier red abierta que encuentre por la calle.
