# AgentsArch

Repositorio de arquitecturas de agentes.

## 🧩 Proyecto: Sistema de Procesamiento Distribuido (Supervisor–Worker–Agent)

### 📖 Descripción General

En una empresa de comercio electrónico, se implementa una arquitectura Supervisor–Worker para optimizar el procesamiento de pedidos. El Supervisor es un servicio central que monitorea una cola de mensajes donde llegan los pedidos desde la tienda en línea. Cada vez que detecta un nuevo pedido, lo distribuye a uno o varios Workers disponibles.

Los Workers son procesos independientes que ejecutan tareas específicas: validación del pago, verificación de inventario, cálculo de costos de envío y actualización del estado del pedido. Si un Worker falla o tarda demasiado en completar su tarea, el Supervisor lo detecta mediante métricas de tiempo y estado, reasigna la tarea a otro Worker y registra el incidente para análisis posterior.

Esta arquitectura permite escalar horizontalmente agregando más Workers según la carga de pedidos, garantiza tolerancia a fallos y mantiene la trazabilidad completa de cada operación, logrando un sistema más eficiente, resiliente y fácil de mantener.
