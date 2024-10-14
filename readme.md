# Sistema de Gestión de Reservas

## Integrantes

Cristhian Conforme
Johnn Valencia
Wilfrido Herrera

## Historia de Usuario Principal

Título: Gestión de Reservas en el Restaurante "La Buena Mesa"
Como un empleado del restaurante "La Buena Mesa",
Quiero poder registrar y gestionar las reservas de clientes de manera sencilla y organizada,
Para evitar problemas de doble reserva y mejorar la distribución de mesas.
Criterios de Aceptación:
Registrar reserva: El sistema debe permitir registrar reservas con el nombre del cliente, número de teléfono, cantidad de personas, y seleccionar la fecha y hora de la reserva.
Asignación automática de mesa(s): Según el número de personas, el sistema debe sugerir la mejor combinación de mesas disponibles.
Ver disponibilidad: El empleado puede consultar qué mesas están libres u ocupadas por fecha y hora.
Modificar o cancelar reserva: Las reservas pueden ser modificadas o canceladas según sea necesario.
Control de reglas de negocio:
Horario de atención: Martes a Domingo de 12:00 a 22:00.
Duración por reserva: 2 horas.
Mínimo 2 horas de anticipación para hacer reservas.
Máximo de 12 personas por reserva combinando mesas.

## Documentación de Decisiones de Diseño

1. Descripción del Problema
El restaurante "La Buena Mesa" requiere un sistema para gestionar reservas, ya que el manejo manual actual genera problemas como dobles reservas y falta de organización. Se necesita una solución que permita registrar reservas, asignar mesas, y gestionar la disponibilidad de las mismas.
2. Opciones Consideradas
Opción 1:
Crear un sistema de gestión de reservas utilizando una base de datos relacional (MySQL) y un entorno frontend sencillo con HTML, CSS y JavaScript.
Ventajas: Base de datos robusta que permite realizar consultas complejas, fácil integración con múltiples tecnologías.
Desventajas: Mayor tiempo de configuración inicial y requerimientos de mantenimiento.
3. Decisión Tomada
Se decidió usar una base de datos relacional (MySQL) para gestionar las reservas y las mesas, ya que permite un manejo adecuado de las consultas para verificar la disponibilidad de mesas y evitar dobles reservas. Además, facilita el escalado del sistema en el futuro si el restaurante decide crecer o integrar funcionalidades más avanzadas.
Frontend: Se optó por crear una interfaz sencilla utilizando HTML, CSS, y JavaScript con el propósito de que los empleados del restaurante puedan gestionar las reservas sin complicaciones. Se agregará un wireframe para definir cómo será la pantalla principal.
4. Justificación Técnica
La base de datos relacional fue elegida debido a que permite la integridad referencial, la consulta rápida sobre la disponibilidad de mesas, y evita problemas de concurrencia, algo fundamental cuando varias personas del restaurante podrían estar manejando las reservas al mismo tiempo. Además, garantiza una buena escalabilidad si en el futuro se agregan nuevas funcionalidades como autenticación o un sistema de pagos.
5. Impacto en el Proyecto
La elección de usar una base de datos relacional y un frontend con tecnologías web básicas impactará en la duración del proyecto, pero se considera necesario para obtener un sistema más robusto.
Se podrá integrar fácilmente un pipeline de CI/CD para verificar los cambios en el código y la documentación, facilitando el mantenimiento a largo plazo.
6. Revisiones Futuras
Autenticación: En una futura versión, se podría agregar autenticación para restringir el acceso a empleados del restaurante.
Sistema de pagos: El sistema actual no contempla pagos, pero en una iteración futura, podría integrarse un sistema de pagos en línea.
Optimización del asignador de mesas: A futuro, el algoritmo para asignar mesas podría mejorarse con inteligencia artificial o lógica más avanzada para maximizar la ocupación del restaurante.
