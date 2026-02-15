## 1. Planteamiento de la Situación Problema

#### Contexto

En la ingeniería de software y en la rama de desarrollo de software, las plataformas de e-commerce y servicios de entrega a domicilio en regiones como Antioquia enfrentan retos de múltiples tipos al manejar altos volúmenes de pedidos. 
Más allá de validar inventarios y calcular precios, surge la necesidad de gestionar eficientemente la logística en escenarios reales: 
- Coordinar múltiples pedidos con: 
	- Dependencias geográficas, 
	- Manejar conexiones variables entre zonas (como carreteras con diferentes tiempos de viaje debido a topografía o tráfico)
	- Priorizar entregas basadas en criterios mixtos (urgencia, valor del pedido o proximidad, nivel de suscripcion en la plataforma), 
	- Equilibrar la carga entre varios repartidores para minimizar demoras totales y costos operativos. 
- Nota: Esto puede incluir escenarios donde las rutas no son directas, requiriendo 
	- Cálculos de caminos óptimos a través de redes de zonas interconectadas
	- Ordenamientos dinámicos de secuencias de entrega para maximizar eficiencia.

**Problema planteado:** 

**Objetivo general:**
Diseñar un algoritmo que procese pedidos de clientes en una tienda virtual 

**Objetivos especificos**

**Procesamiento interno:**
- Validar stock
- Calcular precios individuales (incluyendo descuentos, promociones, impuestos y envíos base), 
- Validar pago
- Validar que no se realicen 2 veces el mismo pago (el usuario le dio click dos veces a pagar ya habiendo puesto la tarjeta de credito)

**En lo que respecta a Logistica:**
* Modelar las zonas como una red conectada con distancias variables (no solo directas, sino a través de rutas intermedias).
* Calcular caminos eficientes entre puntos de entrega para minimizar el recorrido total por repartidor, ordenar y agrupar pedidos según prioridades y valores para asignarlos equilibradamente a múltiples repartidores (evitando sobrecargas). 
* Ajustar dinámicamente si hay restricciones como límites de capacidad por vehículo o ventanas de tiempo para entregas. El sistema debe manejar hasta M pedidos y R repartidores, rechazando o reprogramando si no se puede optimizar dentro de límites (ej. tiempo máximo por ruta).

Esto permite módulos independientes para 
- Precios, 
- Modelado de red, 
- Asignación, ordenamiento y optimización de caminos. 
- etc...