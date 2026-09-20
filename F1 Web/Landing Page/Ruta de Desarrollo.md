### Fase 1: Entorno y Estructura

- [x] Crear la carpeta `donaciones-f1` y la estructura de subcarpetas (`assets/`, `css/`, `js/`).
    
- [x] Crear los archivos en blanco (`index.html`, `css/styles.css`, `js/app.js`, `js/payment.js`, `js/webhook.js`).
    
- [x] Inicializar el repositorio con `git init`.
    
- [x] Buscar y guardar en `assets/img/` el logo de la comunidad y un fondo relacionado a F1.
    

### Fase 2: Maquetación HTML y Textos

- [x] Construir la estructura básica HTML5 en `index.html`.
    
- [x] Insertar los textos definidos en la sección de Copywriting (Header, Párrafos, Footer).
    
- [x] Crear la estructura del botón de donación con un contenedor vacío (`<div id="paypal-button-container"></div>`) donde se inyectará el modal más adelante.
    
- [x] Vincular el archivo `styles.css` y los tres archivos de JavaScript al final del `<body>`.
    

### Fase 3: Estilos y Modo Oscuro (UI)

- [x] Configurar variables CSS para la paleta de colores (Acentos de escudería, blancos/grises para modo claro).
    
- [x] Establecer el fondo del modo oscuro en negro sólido (`#000000`).
    
- [x] Programar la lógica en `js/app.js` para que el botón de alternar tema (☀️/🌙) cambie las clases CSS del body.
    
- [x] Asegurar que el diseño sea responsivo (Mobile First) para que se vea perfecto desde la app móvil de Discord.
    

### Fase 4: Integración de Pagos y Webhooks

- [x] Crear una cuenta en **PayPal Developer** y obtener el `Client ID`.
    
- [x] Insertar el script oficial de PayPal en `index.html` y configurar la lógica de apertura del modal en `js/payment.js`.
    
- [x] Crear un Webhook en el servidor de Discord (Ajustes del servidor > Integraciones > Webhooks) y copiar la URL.
    
- [x] Escribir la petición `fetch` en `js/webhook.js` para enviar el mensaje automático ("🏁 ¡Bandera a cuadros!...") al canal público cuando `payment.js` confirme la transacción.
    

### Fase 5: Despliegue y Pruebas

- [x] Realizar una donación de prueba (Sandbox mode) para verificar que el modal no redirige, se cierra correctamente y el mensaje llega a Discord.
    
- [x] Hacer commit y subir el código al repositorio en GitHub.
    
- [x] Conectar el repositorio a Vercel o GitHub Pages para publicar la web de forma gratuita.



