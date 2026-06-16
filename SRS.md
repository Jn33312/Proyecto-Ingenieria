# Análisis de Perfiles y Requerimientos (UX Aristotélica)

### 1. Perfil: Conductores
Estudiantes o docentes de la BUAP que ingresan con motocicleta.

* **Ethos 
  * **Privacidad de datos:** El sistema deja de usar WhatsApp. Las fotografías y cadenas de texto de las placas viajan encriptadas mediante una petición HTTP (API) directamente a un servidor de la universidad. No se guardan copias locales en la galería del vigilante.
  * **Optimización del tiempo:** El sistema procesa la validación en menos de 3 segundos. El conductor solo detiene la moto frente a la cámara del vigilante, sin interactuar con la app, y avanza en cuanto el vigilante recibe la alerta visual en verde.
  * **Fácil de usar:** Para el registro inicial, el conductor interactúa con una interfaz web o móvil mínima que solo le exige tres campos: Matrícula BUAP, Contraseña y Placa de la moto.
* **Pathos 
  * **Mala organización de datos:** Se elimina la pérdida de registros. Al estar en una base de datos relacional, el ID del conductor está estrictamente vinculado al de su motocicleta, evitando rechazos de acceso por "errores de dedo" en búsquedas manuales.
  * **Falta de seguridad:** El sistema genera un *Log* (bitácora) inmutable. Cada vez que la placa es detectada, se guarda un registro exacto (Timestamp, Placa, ID de la puerta de acceso), garantizando la trazabilidad en caso de robo o incidente en el campus.
* **Logos
  * **Registrarse:** Ejecución de una consulta (Query) tipo `INSERT` en la base de datos donde se crea el perfil del conductor (Matrícula BUAP) y se asocia como llave foránea (Foreign Key) a la tabla de vehículos.
  * **Buen ingreso de información:** Implementación de expresiones regulares (Regex) en el formulario de registro para obligar al usuario a ingresar la placa en un formato válido (ej. obligar mayúsculas, restringir caracteres especiales y longitud exacta), evitando que entre "basura" a la base de datos.

---

### 2. Perfil: Vigilantes
Personal encargado de operar la aplicación móvil desarrollada (ej. en Java) en las casetas de acceso.

* **Ethos 
  * **Optimización de tiempo:** El vigilante confía en que el módulo de Reconocimiento Óptico de Caracteres (OCR) integrado en la app extraerá el texto de la imagen de manera automática, eximiéndolo de teclear cada número.
  * **Fácil de usar:** La interfaz de la app consta de una vista de cámara en pantalla completa y un recuadro de estado que cambia de color. Cero navegación compleja.
  * **Soporte:** Si la placa está sucia o despintada y el OCR falla, la interfaz despliega un campo de texto `Input` manual (Override) para que el vigilante no se quede bloqueado y pueda forzar la consulta a la base de datos.
* **Pathos
  * **Mala organización de datos:** El vigilante ya no tiene que hacer "scroll" infinito en un chat de WhatsApp para buscar si una moto ya salió o entró; la app hace la consulta asíncrona por él.
  * **Renovación del sistema:** Transición de usar una app de mensajería informal a un archivo `.apk` institucional diseñado específicamente para control de accesos.
  * **Optimización del tiempo:** Al automatizar la lectura, se evita el cuello de botella físico y la presión de las largas filas de motos en la entrada durante los horarios de mayor afluencia.
* **Logos 
  * **Registrarse:** La app móvil requiere un `Login` al inicio del turno para generar un Token de sesión. Así, cada registro de entrada se asocia al ID del vigilante en turno.
  * **Captura de placa / Matrícula:** La cámara del móvil toma un *frame* (foto), lo pasa por la librería de visión artificial, recorta el área de la placa y convierte los píxeles en un dato tipo `String`.
  * **Validación de información:** La app envía el `String` de la placa al servidor mediante un método `GET`. El servidor verifica el estado de la placa (`status: activa`) y devuelve una respuesta booleana (`True/False`) para pintar la pantalla del vigilante de verde o rojo.

---

### 3. Perfil: Admin
Usuarios con privilegios administrativos (Dirección de Seguridad, Equipo de Desarrollo: Manuel, Jovan, Erika Audrey, Yonathan).

* **Ethos 
  * **Sistema bien organizado:** Arquitectura basada en una base de datos normalizada que separa claramente las tablas de Usuarios, Vehículos y Accesos, permitiendo escalabilidad a futuro (ej. agregar autos además de motos).
* **Pathos 
  * **Solvencia económica:** Al ser un proyecto desarrollado e implementado internamente por alumnos de la BUAP, la universidad evita el pago de costosas suscripciones (SaaS) a empresas privadas de software de telemetría.
* **Logos 
  * **Seguimiento de actualizaciones:** El sistema cuenta con un panel administrativo (Dashboard) que permite ejecutar operaciones CRUD (Crear, Leer, Actualizar, Borrar) para dar de baja a alumnos que egresan, actualizar placas y exportar el registro total de entradas y salidas en formatos tabulares (CSV/Excel).
