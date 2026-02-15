##### Proceso de razonamiento - El Por que?
#### Relación con Objetivos de la Tarea

Esta propuesta cumple con los objetivos del avance evaluativo 1 al plantear un problema realista y complejo dentro del área disciplinar de **desarrollo de software**, la propuesta me permite:

- Construir un algoritmo completo con **Entrada**, **Proceso** y **Salida** claramente diferenciados.
- Representarlo en **pseudocódigo** estructurado (cabecera, declaraciones, inicio, instrucciones, fin).
- Ejecutar o esquematizar un **diagrama de flujo** con bucles anidados, decisiones múltiples y subflujos.
- El problema es lo suficientemente rico para desarrollarse en 16 semanas sin llegar a complejidades absolutas, permitiendo iteraciones progresivas (entregas al profesor en cada clase cada semana) y divisiones modulares entre 4 integrantes.

Nota: Esto es un draft muchachos, susceciptible a cambios, el proceso creativo me tomo 1 hora lo mas probable es que lo refinemos y nada esta escrito en piedra. (Nivel de incertidumbre alto)

---
#### División (Propuesta) para 4 integrantes

- **Integrante 1**: Módulo de entrada de datos + validación de stock + cálculo de precios y descuentos (subtotales, descuentos por volumen/global/promociones, IVA).
- **Integrante 2**: Ordenamiento de pedidos (por prioridad y valor) + asignación balanceada a repartidores (criterio de menor carga actual).
- **Integrante 3**: Modelado del grafo de zonas + cálculo de caminos mínimos entre zonas + optimización de ruta por repartidor (secuencia de visitas).
- **Integrante 4**: Verificaciones de límites (capacidad, tiempo máximo), [[Prorrateo de costos]] logísticos, generación de salidas detalladas + elaboración de pseudocódigo final y diagrama de flujo.

#### Escalabilidad (Ejemplo) para 16 semanas

- **Fase 1 (semanas 1–4)**: Algoritmo base de procesamiento de pedidos individuales (precios, descuentos, stock, IVA).
- **Fase 2 (semanas 5–8)**: Ordenamiento dinámico + asignación inteligente a repartidores.
- **Fase 3 (semanas 9–12)**: Implementación del grafo + cálculo de caminos eficientes + estimación de tiempos y costos logísticos.
- **Fase 4 (semanas 13–16)**: Integración completa, pruebas de casos límite, refinamiento de salidas, posible prototipo simple de interfaz (consola o básica gráfica), documentación final y presentación.

Nota: Muchachos, como pueden observar cada fase contempla un modulo, en caso de irse por mi propuesta, debemos refinar/ajustar los alcances por fase para que estemos equilibradamente asignados.
#### Entregables Finales

- Documento Word o PowerPoint estructurado (hojas independientes para: partes del algoritmo, pseudocódigo, descripción del diagrama de flujo).
- Archivo(s) PSEINT (.psc) con pseudocódigo ejecutable y diagrama de flujo.
- Archivo .md o .txt con el Product Backlog final (incluyendo la épica y features conceptuales, para guiar el desarrollo).

---

#### Marco de trabajo para la gestión del proyecto: SCRUM

###### Justificación

Scrum es ideal para este proyecto porque:

- Divide el trabajo en ciclos cortos (Sprints de 1 semana).
- Permite entregar incrementos funcionales frecuentes.
- Facilita adaptarse a cambios o descubrimientos durante las 16 semanas.
	- Ej: Resulta que Emm identificio en la semana 3 que hay una inconsisntencia en el planteamiento del problema, va donde el profe, recibe retroalimenacion, ajusta el alcance, el plantemiento o la descripcion del problema y no se ve afectado el proyecto completo.
- Promueve colaboración diaria, autoorganización y mejora continua en un equipo de 4 personas.
	- Scrum habla de ceremonias, planteo que manejemos 2, dailies y retrospectiva.
		- Daily: Reuniones diarias de 5 minutos para informar el progreso contado que se estuvo haciendo, que se estara haciendo y si tiene algun tipo de problema que no le permite avanzar.
		- Retrospectiva: Reunion al finalizar la iteracion para identificar problemas, oportunidades de mejora y ajustar para la siguiente iteracion.
- Funciona bien en proyectos con requisitos que pueden refinarse progresivamente. ([[VUCA]])

#### A nivel operativo
###### Integración conceptual con BDD y Gherkin (Cucumber)

Dentro de Scrum, usaremos **Behavior-Driven Development (BDD)** para definir requisitos de forma clara y testable desde el inicio:

La taxonomia de los [[Product Backlog Item]] en Agil funciona de la siguiente manera

- **Épica**: Tema grande que engloba todo el proyecto (“Algoritmo de la Optimización Logística de Pedidos”).
- **Features**: Partes grandes y entregables de valor de la épica (ej. “Cálculo de precios y descuentos”, “Optimización de rutas por repartidor”, “Asignación balanceada”, etc.). Cada feature se describe en lenguaje natural y se asocia a uno o más sprints.
	- **Criterios de aceptación**: Condiciones verificables que indican que la feature está terminada. Se escriben en formato **Gherkin** (Given – When – Then) para que sean claros, automatizables y sirvan como base para pruebas.
- **Historias de usuario**: Requisitos pequeños y enfocados en el usuario/rol. Formato estándar: **Como** [rol] **Quiero** [funcionalidad] **Para** [beneficio o razón]
	- **Criterios de aceptación**: Condiciones verificables que indican que la historia está terminada. Se escriben en formato **Gherkin** (Given – When – Then) para que sean claros, automatizables y sirvan como base para pruebas.

### Ejemplos:

#### Ejemplo de Feature

```gherkin
Feature: Optimización de rutas para repartidores
  Como sistema de gestión logística de pedidos
  Quiero calcular la ruta más eficiente para cada repartidor
  Para minimizar el tiempo y costo total de entrega y mejorar la satisfacción del cliente
```
### Ejemplo de User Story (dentro de la Feature)

```gherkin
Como repartidor
Quiero recibir la secuencia óptima de zonas a visitar
Para recorrer la menor distancia posible desde la bodega y regresar
```
### Ejemplo de Criterios de Aceptación (en formato Gherkin)

```gherkin
Scenario: Ruta óptima para un repartidor con 4 zonas asignadas
    Given que el repartidor tiene asignados pedidos en las zonas: 1, 3, 5 y 7
    And el grafo de distancias está definido con conexiones entre zonas
    And la zona de la bodega es la 0
    When se calcula la ruta óptima para ese repartidor
    Then la secuencia de visitas debe empezar en la zona 0 (bodega)
    And debe visitar todas las zonas asignadas (1, 3, 5, 7) exactamente una vez
    And la distancia total recorrida debe ser la mínima posible entre todas las secuencias válidas
    And el sistema debe retornar la distancia total en kilómetros
    And el tiempo estimado debe calcularse como distancia total / velocidad promedio (ej. 30 km/h)
    And si la ruta excede el tiempo máximo permitido (ej. 4 horas), debe marcarse como inválida y sugerir reasignación

Scenario: Ruta con solo una zona asignada
    Given que el repartidor tiene un solo pedido en la zona 2
    And la distancia desde almacén (zona 0) a zona 2 es 12 km
    When se calcula la ruta
    Then la secuencia debe ser: 0 → 2 → 0
    And la distancia total debe ser 24 km (ida y vuelta)
    And el tiempo estimado debe ser aproximadamente 0.8 horas
```