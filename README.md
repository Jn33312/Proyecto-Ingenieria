# Sistema Automatizado de Registro Vehicular para Motocicletas (BUAP)

## Resumen Ejecutivo

Este proyecto propone el desarrollo de un sistema de control de acceso vehicular enfocado en motocicletas para las instalaciones de la BUAP. Mediante el uso de visión por computadora y reconocimiento óptico de caracteres (OCR), el sistema automatiza la captura y almacenamiento de placas, optimizando el flujo de entrada, eliminando el error humano y centralizando la información de seguridad en una base de datos estructurada.

### El Problema
Actualmente, el control de acceso de motocicletas en la universidad se realiza de manera manual. El personal de seguridad utiliza sus teléfonos personales para anotar las placas y enviar los registros a través de grupos de WhatsApp. Este método presenta múltiples deficiencias:
* **Ineficiencia y cuellos de botella:** Escribir cada placa manualmente toma tiempo, lo que genera tráfico en las entradas durante las horas pico.
* **Falta de integridad de datos:** Los registros en WhatsApp no están estructurados, son susceptibles a errores de dedo (tipográficos) y son extremadamente difíciles de auditar o buscar en caso de un incidente de seguridad.
* **Vulnerabilidad de la información:** Los datos de acceso se almacenan en dispositivos móviles personales y plataformas de mensajería de terceros, lo que representa un riesgo para la privacidad y el control institucional.

### La Solución
Implementar un sistema de registro automatizado que funcione a través de una cámara instalada en el punto de acceso. 
1. **Captura:** Al momento en que una motocicleta se detiene en la entrada, la cámara captura una imagen de la placa.
2. **Procesamiento:** El sistema procesa la imagen, extrae los caracteres alfanuméricos de la placa de forma automática.
3. **Almacenamiento:** El registro se guarda instantáneamente en una base de datos centralizada con la fecha, hora y punto de acceso exacto, sin requerir intervención manual del guardia.

### Retorno de Inversión (ROI)
Al tratarse de un proyecto institucional de seguridad y logística, el ROI se mide principalmente en eficiencia operativa, mitigación de riesgos y ahorro de horas-hombre:

* **ROI Operativo (Tiempo):** Reducción del tiempo de registro por vehículo de un promedio de 20-30 segundos (método manual) a menos de 3 segundos (método automatizado). Esto elimina las filas en los accesos.
* **ROI en Seguridad (Mitigación de Riesgos):** Creación de un historial de acceso inmutable y consultable en milisegundos. En caso de robo o incidente, la universidad puede identificar exactamente qué vehículos estaban en el campus, reduciendo la vulnerabilidad y posibles costos asociados a incidentes de seguridad.
* **Optimización de Recursos Humanos:** El personal de seguridad deja de realizar tareas administrativas repetitivas de captura de datos, permitiéndoles enfocarse en la vigilancia activa y el control del entorno.
