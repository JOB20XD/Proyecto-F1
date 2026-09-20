# Landing Page de Donaciones F1
## 1. Objetivo del Proyecto

Crear una página web propia y sin comisiones de terceros para recibir donaciones de la comunidad.

**Justificación pública:** Los fondos recaudados se reinvertirán en distintos porcentajes a la mejora y mantenimiento de los distintos productos que ofrecemos a la comunidad, más específicamente para:

- Mejorar la infraestructura del servidor de Discord y costear las versiones premium de los bots de moderación y utilidades.
    
- Mejorar la calidad del servicio de streaming, invirtiendo en herramientas para no depender de señales de terceros y ofrecer la mejor experiencia durante las transmisiones.

_(Nota interna: Un pequeño porcentaje de utilidad quedará para el equipo de desarrollo del proyecto)._

## 2. Estilo Visual y UI/UX

- **Temática:** Motorsport / Fórmula 1.
    
- **Modo de visualización:** Implementación de un botón (toggle) para alternar entre Modo Claro y Modo Oscuro (con un fondo totalmente negro para el modo oscuro).
    
- **Paleta de Colores:**
    
    - Fondo: Dinámico (Blanco/Gris claro en modo claro; Negro sólido/Gris fibra de Carbono en modo oscuro).
        
    - Acentos: Múltiples colores Representativos de las diferentes escuderías para diferentes Secciones y botones.
        
- **Tipografía:** Itálica para los títulos, moderna y deportiva.
## 3. [[Estructura]] de la Página (Secciones)

1. **Head:** Logo de la comunidad, título llamativo y botón de cambio Claro/Oscuro.
    
2. **Mensaje Principal:** Explicación sobre el uso de las donaciones.
    
3. **Recompensas:** _(Definidas más adelante)._
    
4. **Módulo de Pago:** Botones claros para donar.
    
5. **Footer:** Agradecimientos y enlaces de vuelta al servidor de discord y a los canales de transmisión.

## 4. Requisitos Técnicos (Tech Stack)

- **Frontend:** HTML5, CSS3, JavaScript.
    
- **Pagos:** Sistema determinado para PayPal
    
- **Notificaciones:** Una webhook para enviar un mensaje automático a un canal de discord con cada donación.

## 5. [[Copywriting]]

### Opción A: Enfoque a día de carrera

- **Título Principal (H1):** 🏎️ Impulsa nuestra Escudería
    
- **Subtítulo (H2):** Ayúdanos a mejorar el rendimiento del servidor y las transmisiones.
    
- **Párrafo Principal:** Mantener la pista en óptimas condiciones para los miembros requiere mejoras constantes. Tus aportes se destinan directamente a la telemetría del servidor: costeamos las versiones premium de nuestros bots de moderación y mejoramos la infraestructura de streaming. Queremos depender menos de señales externas y ofrecerte la mejor calidad de transmisión en cada Gran Premio.
    
- **Texto de Botones (CTA):**
	- "Apoyo Personalizado"
		
	- "Apoyo Rookie (Donar $3)"
	    
    - "Hacer un Pit Stop (Donar $5)"
        
    - "Mejorar el Monoplaza (Donar $10)"
        

### Opción B: Enfoque más técnico y directo

- **Título Principal (H1):** 🛠️ Telemetría y Mejoras del Servidor
    
- **Subtítulo (H2):** Invierte en el desarrollo y la calidad de nuestra comunidad.
    
- **Párrafo Principal:** Nuestro servidor y las transmisiones en directo están en constante evolución. Las donaciones nos permiten actualizar nuestro paquete aerodinámico: pagamos el alojamiento de bots de alto rendimiento para Discord y adquirimos herramientas de streaming independientes. El objetivo es ofrecer transmisiones fluidas, en alta calidad y sin depender de terceros durante las clasificaciones y carreras.
    
- **Texto de Botones (CTA):**
	- "Apoyo persinalizado"
		
	- "Apoyo Rookie (Donar $3)"
	    
    - "Aportar Combustible ($5)"
        
    - "Financiar Mejoras ($10)"
        

### Textos de Interfaz (Micro-copy)

- **Toggle Claro/Oscuro:** Modo Nocturno / Modo Día (iconos ☀️ / 🌙).
    
- **Footer:** Creado por la comunidad, para la comunidad. Síguenos en la pista: [Iconos de Twitch, Kick, Discord].
    
- **Mensaje Post-donación:** 🏁 ¡Bandera a cuadros! Tu aporte ha sido procesado con éxito. El equipo de mecánicos te lo agradece. Nos vemos en la pista.
## 6. Flujo de Pagos y Seguridad (UX)

**Estrategia:** In-page Modal

- **Método de integración:**
    
    - Se utilizarán los **Smart Payment Buttons de PayPal**. Estos botones se insertan mediante un script en el `index.html` y al hacer clic, abren una ventana emergente segura de PayPal en la misma página.
        
- **Seguridad:** Nivel PCI-DSS delegado. La página no almacena ni procesa datos de tarjetas ni cuentas. El script oficial de PayPal maneja el 100% de la transacción encriptada.
    
- **Flujo de interacción:**
    
    1. El usuario selecciona un monto o el tier de donación.
        
    2. Hace clic en el botón de donar.
        
    3. Se oscurece el fondo y aparece el modal de pago.
        
    4. Al confirmar, el modal se cierra solo.
        
    5. La página web detecta el éxito de la transacción (vía promesas en JavaScript) y muestra el mensaje de agradecimiento en pantalla.
        
    6. Se dispara el Webhook hacia el canal de Discord.

## 7. Estructura de Carpetas y Archivos
~~~
donaciones-f1/
│
├── index.html             # Estructura principal y copywriting
├── README.md              # Documentación técnica para el repositorio de GitHub
│
├── assets/                # Archivos multimedia
│   ├── img/               # Fondos, logo de la comunidad, imágenes de la escudería
│   └── icons/             # Iconos de Discord, Twitch, Kick y el toggle
│
├── css/                   # Estilos visuales
│   └── styles.css         # Configuración del modo oscuro/claro y ajustes de diseño
│
└── js/                    # Lógica del frontend separada en módulos
    ├── app.js             # Lógica de la interfaz
    ├── payment.js         # Configuración del modal emergente de PayPal
    └── webhook.js         # Lógica para enviar la notificación automática al servidor
~~~
## 8. [[Ruta de Desarrollo]]
### Fase 1: Entorno y Estructura

- Crear la carpeta `donaciones-f1` y la estructura de subcarpetas (`assets/`, `css/`, `js/`).
    
- Crear los archivos en blanco (`index.html`, `css/styles.css`, `js/app.js`, `js/payment.js`, `js/webhook.js`).
    
- Inicializar el repositorio con `git init`.
    
- Buscar y guardar en `assets/img/` el logo de la comunidad y un fondo relacionado a F1.
    

### Fase 2: Maquetación HTML y Textos

- Construir la estructura básica HTML5 en `index.html`.
    
- Insertar los textos definidos en la sección de Copywriting (Header, Párrafos, Footer).
    
- Crear la estructura del botón de donación con un contenedor vacío (`<div id="paypal-button-container"></div>`) donde se inyectará el modal más adelante.
    
- Vincular el archivo `styles.css` y los tres archivos de JavaScript al final del `<body>`.
    

### Fase 3: Estilos y Modo Oscuro (UI)

- Configurar variables CSS para la paleta de colores (Acentos de escudería, blancos/grises para modo claro).
    
- Establecer el fondo del modo oscuro en negro sólido (`#000000`).
    
- Programar la lógica en `js/app.js` para que el botón de alternar tema (☀️/🌙) cambie las clases CSS del body.
    
- Asegurar que el diseño sea responsivo (Mobile First) para que se vea perfecto desde la app móvil de Discord.
    

### Fase 4: Integración de Pagos y Webhooks

- Crear una cuenta en **PayPal Developer** y obtener el `Client ID`.
    
- Insertar el script oficial de PayPal en `index.html` y configurar la lógica de apertura del modal en `js/payment.js`.
    
- Crear un Webhook en el servidor de Discord (Ajustes del servidor > Integraciones > Webhooks) y copiar la URL.
    
- Escribir la petición `fetch` en `js/webhook.js` para enviar el mensaje automático ("🏁 ¡Bandera a cuadros!...") al canal público cuando `payment.js` confirme la transacción.
    

### Fase 5: Despliegue y Pruebas

- Realizar una donación de prueba (Sandbox mode) para verificar que el modal no redirige, se cierra correctamente y el mensaje llega a Discord.
    
- Hacer commit y subir el código al repositorio en GitHub.
    
- Conectar el repositorio a Vercel o GitHub Pages para publicar la web de forma gratuita.