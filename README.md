# Sistema Automatizado de Registro Vehicular (BUAP)

---

## 1. Resumen Ejecutivo

Este proyecto propone el desarrollo de un sistema de control de acceso vehicular para las instalaciones de la BUAP. Mediante el uso de visión por computadora y reconocimiento óptico de caracteres (OCR), el sistema automatiza la captura y almacenamiento de placas para todo tipo de vehículos (automóviles, motocicletas y de carga). El objetivo es optimizar el flujo de entrada, eliminar el error humano y centralizar la información de seguridad, reportes y multas en una base de datos estructurada.

### El Problema (Medible y Cuantificable)
Actualmente, el control de acceso en la universidad se realiza de manera manual mediante anotaciones o grupos de WhatsApp. Este método presenta deficiencias cuantificables:
* **Ineficiencia crítica:** El registro manual toma en promedio de 30 a 45 segundos por vehículo. En horas pico, esto genera un cuello de botella que retrasa el ingreso de la comunidad y provoca filas de hasta 30 vehículos.
* **Carencia de integridad de datos:** Al usar plataformas de mensajería, existe un 100% de pérdida de información estructurada. Los datos son inauditable, no se pueden realizar búsquedas eficientes en caso de incidentes y se vulnera la privacidad institucional.
* **Control deficiente:** No existe un seguimiento unificado para vehículos que cometen faltas (exceso de velocidad, estacionamiento indebido), lo que imposibilita la aplicación efectiva del reglamento vial universitario.

### La Solución
Implementar un sistema de registro automatizado basado en cámaras de lectura instaladas en los accesos:
* **Captura Universal y OCR:** La cámara detecta el vehículo, captura la placa y extrae los caracteres alfanuméricos de forma automática en milisegundos.
* **Pre-registro de Invitados:** Portal web donde alumnos o administrativos pueden registrar anticipadamente los datos de un vehículo invitado, permitiendo que la cámara autorice su entrada automática sin detener el tráfico.
* **Sistema de Reportes y Multas:** Módulo que asocia un historial de incidencias a cada matrícula, alertando visualmente al guardia si el vehículo detectado cuenta con multas activas o reportes de seguridad.
* **Almacenamiento Centralizado:** Creación automática de registros con fecha, hora y punto de acceso exacto, sin intervención manual.

### Retorno de Inversión (ROI)
El proyecto justifica su viabilidad a través de métricas claras de eficiencia y ahorro:
* **ROI Operativo:** Reducción del tiempo de registro en un 90% (bajando de 30 segundos a menos de 3 segundos por validación), erradicando las filas en los accesos.
* **ROI Administrativo (Horas-Hombre):** Recuperación estimada de 40 horas semanales por elemento de seguridad en el acceso, reasignando su labor hacia la vigilancia activa.
* **ROI en Seguridad:** Trazabilidad del 100% de los ingresos vehiculares con un historial inmutable, reduciendo drásticamente los tiempos de investigación ante siniestros.
* **ROI Financiero:** Incremento en la recaudación de multas internas gracias al bloqueo y alerta automatizada de vehículos con adeudos o infracciones.

---

## 2. Análisis Costo-Beneficio

La implementación del sistema requiere una inversión inicial que se amortiza rápidamente mediante la eficiencia operativa generada.

* **Costos Directos:** Adquisición de cámaras IP de alta resolución, servidores (locales o nube) para el procesamiento de imágenes e infraestructura de red.
* **Costos Indirectos:** Horas de capacitación para el personal de vigilancia y mantenimiento preventivo periódico de los equipos.
* **Payback Period (Tiempo de Recuperación):** La inversión se recupera a mediano plazo apalancada por la optimización de las horas-hombre del personal de seguridad, la mitigación de riesgos de seguridad (robos o incidentes) y la regularización efectiva de multas.

---

## 3. Evaluación de Riesgos

Se han identificado posibles obstáculos durante la implementación, junto con sus respectivos planes de contingencia:

* **Riesgos Tecnológicos:** Fallas en la lectura OCR debido a lluvia extrema, neblina o placas desgastadas. Se mitigará mediante la inclusión de un módulo de captura manual ultrarrápido en la interfaz del guardia.
* **Riesgos Operativos:** Resistencia al cambio por parte del personal de seguridad o ingreso de vehículos nuevos sin placas. Se mitigará con interfaces altamente intuitivas y la habilitación de accesos mediante escaneo de códigos QR.
* **Riesgos Financieros:** Sobrecostos en el procesamiento en la nube debido al flujo continuo de video. Se mitigará optimizando el código para que el servidor solo procese fotogramas cuando los sensores detecten un vehículo completamente detenido.

---

## 4. En Entornos Ágiles

Para la ejecución de este proyecto hemos seleccionado **Scrum** como marco de trabajo, descartando metodologías tradicionales por las siguientes razones técnicas:

* **Justificación de la Metodología:** Este sistema requiere la integración directa de hardware (cámaras IP) con software (algoritmos OCR y bases de datos). Scrum nos permite trabajar en iteraciones cortas (Sprints de 2 semanas) para probar la precisión de la cámara en campo y hacer ajustes de código inmediatos ante variaciones de luz o clima, algo imposible en un modelo en cascada.
* **Entregas de Valor Constante:** Scrum facilita la entrega del proyecto por módulos funcionales (Sprint 1: Base de datos; Sprint 2: Modelo OCR; Sprint 3: Panel web de multas), permitiendo a los *Stakeholders* validar el progreso de forma tangible.
* **Artefacto Vivo:** Este Caso de Negocio no es estático. Al finalizar cada Sprint Review, el equipo reevaluará los costos, la precisión de la lectura y los riesgos técnicos para asegurar que el ROI se mantenga positivo en todo momento.
