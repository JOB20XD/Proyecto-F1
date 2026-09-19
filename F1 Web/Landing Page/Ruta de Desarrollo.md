### Fase 1: Entorno y Estructura

- [ ] Crear la carpeta `donaciones-f1` y la estructura de subcarpetas (`assets/`, `css/`, `js/`).
    
- [ ] Crear los archivos en blanco (`index.html`, `css/styles.css`, `js/app.js`, `js/payment.js`, `js/webhook.js`).
    
- [ ] Inicializar el repositorio con `git init`.
    
- [ ] Buscar y guardar en `assets/img/` el logo de la comunidad y un fondo relacionado a F1.
    

### Fase 2: Maquetación HTML y Textos

- [ ] Construir la estructura básica HTML5 en `index.html`.
    
- [ ] Insertar los textos definidos en la sección de Copywriting (Header, Párrafos, Footer).
    
- [ ] Crear la estructura del botón de donación con un contenedor vacío (`<div id="paypal-button-container"></div>`) donde se inyectará el modal más adelante.
    
- [ ] Vincular el archivo `styles.css` y los tres archivos de JavaScript al final del `<body>`.
    

### Fase 3: Estilos y Modo Oscuro (UI)

- [ ] Configurar variables CSS para la paleta de colores (Acentos de escudería, blancos/grises para modo claro).
    
- [ ] Establecer el fondo del modo oscuro en negro sólido (`#000000`).
    
- [ ] Programar la lógica en `js/app.js` para que el botón de alternar tema (☀️/🌙) cambie las clases CSS del body.
    
- [ ] Asegurar que el diseño sea responsivo (Mobile First) para que se vea perfecto desde la app móvil de Discord.
    

### Fase 4: Integración de Pagos y Webhooks

- [ ] Crear una cuenta en **PayPal Developer** y obtener el `Client ID`.
    
- [ ] Insertar el script oficial de PayPal en `index.html` y configurar la lógica de apertura del modal en `js/payment.js`.
    
- [ ] Crear un Webhook en el servidor de Discord (Ajustes del servidor > Integraciones > Webhooks) y copiar la URL.
    
- [ ] Escribir la petición `fetch` en `js/webhook.js` para enviar el mensaje automático ("🏁 ¡Bandera a cuadros!...") al canal público cuando `payment.js` confirme la transacción.
    

### Fase 5: Despliegue y Pruebas

- [ ] Realizar una donación de prueba (Sandbox mode) para verificar que el modal no redirige, se cierra correctamente y el mensaje llega a Discord.
    
- [ ] Hacer commit y subir el código al repositorio en GitHub.
    
- [ ] Conectar el repositorio a Vercel o GitHub Pages para publicar la web de forma gratuita.