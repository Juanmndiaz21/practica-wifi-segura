# Informe de Auditoría de Red Wi-Fi Insegura

## Introducción
Este documento detalla el análisis de tráfico realizado sobre una conexión no segura, exponiendo los riesgos de navegar en redes Wi-Fi públicas sin protección y cómo mitigar estas vulnerabilidades.

## Sitio analizado
- **URL:** http://neverssl.com
- **Propósito:** Es un sitio diseñado específicamente para no usar cifrado, ideal para probar la interceptación de tráfico y portales cautivos.

## Evidencia observada
Al analizar la primera solicitud HTTP mediante las herramientas de desarrollador, se obtuvo la siguiente información:
- **URL solicitada:** http://majesticfreshshiningkiss.neverssl.com/online[cite: 3]
- **Método HTTP:** GET[cite: 3]
- **Host:** majesticfreshshiningkiss.neverssl.com[cite: 3]
- **Protocolo:** HTTP
- **User-Agent:** Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/156.0.0.0 Safari/537.36[cite: 3]

## Riesgos encontrados
1. **Protocolo inseguro:** El sitio utiliza HTTP en lugar de HTTPS, lo que significa que la información viaja en texto plano sin cifrar.
2. **Exposición de datos:** Cualquier persona conectada a la misma red Wi-Fi pública puede interceptar el tráfico de red y leer:
   - Las URLs exactas de navegación.
   - El sistema operativo y versión del navegador (User-Agent).
   - Posibles cookies de sesión, contraseñas o datos de formularios si los hubiera.

## Cómo ayuda una VPN
El uso de una Red Privada Virtual (VPN) mitiga estos riesgos mediante:
- **Cifrado:** Aplica criptografía sólida a todos los paquetes de datos que entran y salen del dispositivo.
- **Túnel seguro:** Crea una conexión cifrada entre el dispositivo y el servidor VPN, ocultando el destino final del tráfico a los administradores de la red local.
- **Protección del tráfico:** Un atacante en la red Wi-Fi pública solo interceptará un flujo de datos incomprensible, protegiendo la privacidad y las credenciales del usuario.

## 3 Reglas de Oro para navegar en redes Wi-Fi públicas
1. Nunca ingresar credenciales bancarias ni realizar transacciones financieras sin estar conectado a una VPN de confianza.
2. Verificar siempre que la conexión utilice HTTPS antes de ingresar cualquier dato personal o contraseña.
3. Desactivar la función de conexión automática a redes Wi-Fi abiertas en todos los dispositivos móviles y computadoras portátiles.
