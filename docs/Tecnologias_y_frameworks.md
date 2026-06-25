## 🛠️ Stack Tecnológico

El proyecto emplea tecnologías nativas y herramientas de alto rendimiento para garantizar un funcionamiento fluido, rápido y capaz de operar sin conexión a internet en los puntos de acceso universitario.

| Tecnología / Framework | Descripción | Justificación en el Proyecto |
| :--- | :--- | :--- |
| **Android Studio** | Entorno de Desarrollo Integrado (IDE) oficial de Google para el ecosistema Android. | Proporciona las herramientas de compilación y emulación necesarias para generar rápidamente el archivo instalable (`.apk`). |
| **Java** | Lenguaje de programación nativo, fuertemente tipado y orientado a objetos. | Permite aplicar lógicas complejas de estructuras de datos y garantiza solidez en la manipulación del ciclo de vida de la cámara. |
| **XML & Material Design** | Lenguaje de marcado nativo combinado con la librería de componentes preconstruidos de Google. | Facilita el diseño de pantallas limpias, alertas de estado claras y botones accesibles, asegurando una experiencia de usuario estandarizada. |
| **Google ML Kit (Text Recognition API)** | Motor de OCR impulsado por Machine Learning que opera directamente en el dispositivo (*on-device*). | Extrae el texto de las placas en milisegundos. Al funcionar de manera offline, evita que el sistema dependa de conexiones de red inestables. |
| **Realm (MongoDB)** | Base de datos móvil NoSQL orientada a objetos. | Permite almacenar los historiales de acceso y perfiles de usuarios de forma ultrarrápida, eliminando las consultas SQL complejas y reduciendo el código de persistencia. |
| **RegEx (Expresiones Regulares)** | Secuencias de caracteres que conforman un patrón de búsqueda para validación. | Limpia la lectura en crudo del OCR, evitando "basura visual" y garantizando que solo ingresen formatos válidos de placa vehicular al sistema. |
| **Java I/O (Input/Output)** | Librerías nativas para la manipulación y escritura de archivos en el sistema de almacenamiento. | Empaqueta todo el historial guardado en Realm en un archivo plano estructurado (`.csv`), permitiendo entregar reportes administrativos sin necesidad de un servidor. |
