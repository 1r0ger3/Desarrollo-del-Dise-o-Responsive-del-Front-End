# Funifelt AI Chat

## Descripción del Proyecto

Funifelt AI Chat es una plataforma de chat de inteligencia artificial diseñada específicamente para el aprendizaje de idiomas. Este sistema permite a los usuarios interactuar con un asistente virtual multilingüe capaz de responder en español, inglés, francés e italiano, ofreciendo una experiencia conversacional amigable e interactiva que facilita la práctica y aprendizaje de idiomas.

## Características Principales

- **Soporte Multilingüe**: Interacción fluida en español, inglés, francés e italiano.
- **Detección Automática de Idioma**: Identifica el idioma utilizado por el usuario.
- **Interfaz Amigable**: Diseño intuitivo y atractivo con colores de la marca Funifelt.
- **Comunicación en Tiempo Real**: Implementada con Socket.IO para respuestas instantáneas.
- **Personalización del Contexto**: Prompts específicos para cada idioma.
- **Diseño Responsivo**: Funciona perfectamente en dispositivos móviles y de escritorio.
- **Comandos Rápidos**: Cambio sencillo entre idiomas mediante comandos específicos.

## Tecnologías Utilizadas

- **Backend**:
  - Node.js
  - Express.js
  - Socket.IO
  - OpenAI API (GPT-4)

- **Frontend**:
  - HTML5
  - CSS3
  - JavaScript (Vanilla)
  - Socket.IO Cliente

## Requisitos Previos

- Node.js (v14.0.0 o superior)
- npm (v6.0.0 o superior)
- Clave API de OpenAI

## Estructura del Proyecto

```
funifelt-ai-chat/
│
├── public/
│   ├── index.html      # Interfaz de usuario principal
│   ├── css/            # Estilos de la aplicación (opcional)
│   ├── js/             # Scripts del cliente (opcional)
│   └── assets/         # Imágenes y recursos adicionales
│
├── server.js           # Archivo principal del servidor
├── package.json        # Configuración del proyecto y dependencias
├── .env                # Variables de entorno (API keys, configuración)
└── README.md           # Documentación del proyecto
```

## Instalación

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/funifelt/funifelt-ai-chat.git
   cd funifelt-ai-chat
   ```

2. Instalar dependencias:
   ```bash
   npm install
   ```

3. Configurar las variables de entorno:
   - Crear un archivo `.env` en la raíz del proyecto
   - Añadir la clave API de OpenAI:
     ```
     OPENAI_API_KEY=tu_clave_api_aquí
     PORT=3000
     ```

4. Iniciar el servidor:
   ```bash
   npm start
   ```

5. Acceder a la aplicación:
   - Abrir un navegador web
   - Navegar a `http://localhost:3000`

## Configuración

### Idiomas Soportados

El sistema está configurado para soportar los siguientes idiomas:
- Español (es)
- Inglés (en)
- Francés (fr)
- Italiano (it)

### Personalización del Modelo de IA

El archivo `server.js` contiene configuraciones para el comportamiento del chat en cada idioma. Puedes modificar los siguientes parámetros según tus necesidades:

1. **Prompts del Sistema**: Ubicados en la función `getSystemPrompt()`, estos determinan la personalidad y comportamiento del asistente en cada idioma.

2. **Modelo de OpenAI**: Por defecto se utiliza GPT-4, pero puedes cambiarlo a otro modelo según tus necesidades de rendimiento y costo:
   ```javascript
   model: "gpt-4" // Cambiar a "gpt-3.5-turbo" u otro modelo compatible
   ```

3. **Parámetros de Generación**:
   ```javascript
   max_tokens: 500 // Ajustar según la extensión deseada de las respuestas
   ```

### Personalización de la Interfaz

El archivo `index.html` contiene todo el código de la interfaz de usuario. Puedes personalizar:

1. **Colores de Marca**: Modificar las variables CSS en la sección `:root` para adaptar los colores a la marca Funifelt.

2. **Textos y Etiquetas**: Cambiar los textos de la interfaz según las necesidades específicas.

3. **Comportamiento de la Detección de Idioma**: Modificar la función `detectLanguage()` para mejorar la precisión de la detección automática.

## Uso

### Comandos de Cambio de Idioma

El chat responde a los siguientes comandos para cambiar de idioma:
- `/español` o `/spanish`: Cambia al español
- `/inglés` o `/english`: Cambia al inglés
- `/francés` o `/french`: Cambia al francés
- `/italiano` o `/italian`: Cambia al italiano

### API y Endpoints

El servidor expone los siguientes endpoints:

- **GET /** - Sirve la interfaz principal del chat
- **WebSocket** - Maneja la comunicación en tiempo real del chat

### Eventos Socket.IO

- **user-message**: Enviado por el cliente al servidor con el mensaje del usuario
- **bot-message**: Enviado por el servidor al cliente con la respuesta del asistente

## Consideraciones para Producción

### Seguridad

- Implementar autenticación de usuarios
- Configurar límites de tasa (rate limiting)
- Almacenar las claves API de forma segura
- Configurar HTTPS para conexiones seguras

### Escalabilidad

- Considerar una arquitectura de microservicios para componentes independientes
- Implementar un balanceador de carga para manejar múltiples instancias
- Utilizar una base de datos para almacenar historiales de conversación

### Optimización de Costos

- Implementar caché para respuestas comunes
- Monitorear y limitar el uso de tokens de la API de OpenAI
- Considerar modelos más económicos para preguntas simples

## Funcionalidades Avanzadas (Desarrollo Futuro)

- **Ejercicios Personalizados**: Generar ejercicios basados en el nivel y necesidades del usuario
- **Corrección Gramatical**: Identificar y corregir errores gramaticales en los mensajes del usuario
- **Análisis de Progreso**: Seguimiento del aprendizaje y áreas de mejora
- **Expansión de Idiomas**: Añadir soporte para más idiomas
- **Integración con Audio**: Capacidad de pronunciación y reconocimiento de voz


## Contacto

Para más información o soporte, contactar a:
- Telefono: +57 3053493168 (CO)
+31 6 87623593  (NL)
- Sitio web:[ [sitio web de Funifelt]](https://www.funifelt.com)

---

2024

by FUNIFELT ©

All rights reserved 
