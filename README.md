# Sistema Automatizado de Registro Vehicular (BUAP)

---

## 1. Resumen Ejecutivo

Este proyecto propone el desarrollo de una aplicación móvil integral para el control de acceso vehicular en las instalaciones de la BUAP. Mediante el uso de visión por computadora y reconocimiento óptico de caracteres (OCR) integrado en los dispositivos móviles del personal de seguridad, el sistema automatiza la captura de placas directamente con la cámara del teléfono celular. El objetivo es optimizar el flujo de entrada, eliminar el error humano, identificar plenamente a los miembros de la comunidad y centralizar la información de seguridad, reportes y multas en una base de datos estructurada.

### El Problema
Actualmente, el control de acceso en la universidad se realiza de manera manual. El personal de seguridad utiliza sus teléfonos personales para anotar las placas y enviar los registros a través de grupos de WhatsApp. Este método presenta deficiencias cuantificables:
* **Ineficiencia crítica:** Escribir cada placa manualmente en el teclado del celular toma en promedio de 30 a 45 segundos por vehículo. En horas pico, esto genera un cuello de botella que retrasa el ingreso de la comunidad y provoca filas de hasta 30 vehículos.
* **Carencia de integridad y anonimato de los datos:** Al usar plataformas de mensajería, existe un 100% de pérdida de información estructurada. No es posible saber al instante a quién pertenece el vehículo que ingresa, los datos son inauditables y se vulnera la privacidad institucional.
* **Control deficiente:** No existe una forma rápida para que el guardia verifique si el conductor es un estudiante activo, un trabajador o si el vehículo tiene reportes pendientes o multas acumuladas dentro del campus.

### La Solución
Implementar una aplicación móvil de registro automatizado para uso del personal de seguridad en los puntos de acceso, diseñada para todo tipo de vehículos (automóviles, motocicletas y de carga):
* **Captura Móvil y OCR:** El guardia apunta la cámara de su dispositivo móvil hacia la placa; la app captura la imagen y extrae los caracteres alfanuméricos de forma automática en milisegundos.
* **Despliegue de Perfil Completo:** Al procesar la placa, la aplicación muestra inmediatamente en la pantalla del celular toda la información del usuario vinculado: Nombre completo, Matrícula, Tipo de usuario (Estudiante, Docente o Administrativo), Carrera o Dependencia a la que pertenece, y un historial detallado de multas o reportes vigentes.
* **Pre-registro de Invitados:** Portal web donde alumnos o administrativos pueden registrar anticipadamente los datos de un vehículo invitado, permitiendo que la app del guardia lo reconozca y autorice su entrada de forma inmediata.
* **Almacenamiento Centralizado:** Creación automática de registros de acceso con fecha, hora, punto de entrada y los datos del guardia que realizó la validación.

### Retorno de Inversión (ROI)
El proyecto justifica su viabilidad a través de métricas claras de eficiencia y aprovechamiento de recursos:
* **ROI Operativo:** Reducción del tiempo de registro en un 90% (bajando de 30 segundos de digitación manual a menos de 3 segundos por escaneo fotográfico), erradicando las filas en los accesos.
* **ROI Administrativo (Horas-Hombre):** Recuperación estimada de 40 horas semanales por elemento de seguridad en el acceso, reasignando su labor hacia la vigilancia activa en lugar de la captura de texto.
* **ROI en Seguridad:** Identificación y trazabilidad del 100% de los ingresos vehiculares con un historial inmutable y conocimiento exacto de la identidad del conductor (nombre y carrera/dependencia) al momento de cruzar el acceso.
* **ROI Financiero:** Incremento en la recaudación de multas internas al contar con un sistema que notifica visualmente al guardia sobre adeudos pendientes en el instante preciso del ingreso.

---

## 2. Análisis Costo-Beneficio

La naturaleza móvil del proyecto optimiza significativamente los costos de infraestructura física, facilitando una adopción ágil.

* **Costos Directos:** Desarrollo del software móvil, infraestructura de servidores o servicios en la nube para el backend y la base de datos centralizada, junto con la adquisición de dispositivos móviles institucionales (en caso de ser requeridos).
* **Costos Indirectos:** Tiempo de capacitación para que los guardias se familiaricen con la interfaz de la aplicación y el consumo de datos móviles para la sincronización con el servidor.
* **Payback Period (Tiempo de Recuperación):** Al no requerir la costosa instalación de cámaras fijas ni cableado estructurado en cada acceso, la inversión inicial es baja y se recupera a corto plazo mediante la optimización de horas-hombre y la detección inmediata de infracciones no pagadas.

---

## 3. Evaluación de Riesgos

Se han identificado posibles obstáculos durante la implementación móvil, junto con sus respectivos planes de contingencia:

* **Riesgos Tecnológicos:** Variaciones en la calidad de la lectura OCR debido al pulso del guardia, condiciones de luz cambiantes (noche/día) o falta de enfoque de la cámara móvil. Se mitigará mediante el desarrollo de un algoritmo de estabilización de imagen dentro de la app y un botón de captura manual de respaldo ultrarrápido.
* **Riesgos Operativos:** Resistencia al cambio por parte del personal de seguridad acostumbrado a WhatsApp, o descarga prematura de las baterías de los teléfonos durante turnos largos. Se mitigará diseñando una interfaz móvil minimalista de un solo toque y proveyendo estaciones de carga rápida o baterías externas en las casetas de vigilancia.
* **Riesgos de Conectividad:** Zonas de los accesos campus con baja cobertura de red celular o Wi-Fi. Se mitigará implementando una base de datos local temporal en la app (modo offline) que permita seguir escaneando placas y sincronice los datos de manera automática al recuperar la señal.

---

## 4. En Entornos Ágiles

Para la ejecución de este proyecto hemos seleccionado **Scrum** como marco de trabajo, descartando metodologías tradicionales por las siguientes razones técnicas:

* **Justificación de la Metodología:** El desarrollo de aplicaciones móviles requiere pruebas constantes en diversos modelos de teléfonos y condiciones reales de luz en los accesos de la universidad. Scrum nos permite trabajar en iteraciones cortas (Sprints de 2 semanas) para liberar versiones de prueba de la app, evaluar el rendimiento del OCR directamente en los celulares de los guardias y corregir errores de usabilidad de inmediato.
* **Entregas de Valor Constante:** Scrum facilita la entrega del proyecto por módulos funcionales utilizables desde el celular (Sprint 1: Interfaz base y lectura de placas; Sprint 2: Conexión a la base de datos y despliegue de perfiles de estudiantes/carreras; Sprint 3: Módulo de multas y pre-registro web).
* **Artefacto Vivo:** Este Caso de Negocio no es estático. Al finalizar cada Sprint Review, el equipo evaluará el desempeño de la aplicación móvil en campo y actualizará los costos y riesgos técnicos para garantizar la viabilidad del proyecto.
