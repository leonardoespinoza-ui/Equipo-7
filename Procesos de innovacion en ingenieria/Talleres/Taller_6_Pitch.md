# Taller 6: pitch del sistema de riego sectorizado

> **Estado:** guion y apoyo visual listos para grabar. El enlace del video queda pendiente hasta que el equipo lo grabe y lo suba a YouTube como **No listado**.

**Diapositivas:** [Pitch_Taller_6.pptx](../Presentaciones%20de%20Proyecto/Pitch_Taller_6.pptx)  
**Video del pitch (YouTube, No listado):** PENDIENTE_DE_ENLACE

**Duración prevista:** 4 min 35 s a 4 min 50 s, con transiciones breves.  
**Participación:** puede exponer una persona o repartirse entre integrantes del equipo.  
**Apoyo visual:** seis diapositivas, una por bloque temático. El guion cubre los ocho pasos solicitados.

## Arquitectura que se presenta

- **Módulo central (ESP32-S3):** mide la humedad de su propia zona, recibe los datos de módulos dependientes cercanos y se conecta por Wi-Fi a la plataforma web. Cuenta con alimentación autónoma y recarga solar en el diseño propuesto.
- **Módulos dependientes (ESP32-C3):** miden la humedad de otras zonas, se asocian al módulo central y le envían sus lecturas. Cada unidad cuenta con batería y recarga solar en el diseño propuesto.
- **Controlador de riego (otro ESP):** recibe la orden para su zona y activa la bomba correspondiente. En la maqueta se mostrará un controlador y una bomba como simulación del riego.
- **Plataforma web:** muestra el estado y el historial de cada zona y permite enviar órdenes de riego. La comunicación local entre módulos y el funcionamiento continuo con energía solar son objetivos del prototipo que deben verificarse en las pruebas.

## Guion para la grabación

### Diapositiva 1 · Historia y problema (0:00–0:48)

**1. Historia.** «Imaginemos a la persona encargada de cuidar las áreas verdes de un parque de San Martín de Porres. Ve algunas plantas secas y otras zonas todavía húmedas, pero solo dispone de un horario general de riego. Si riega todo por igual, no sabe qué sector necesita realmente agua.»

**2. Problema.** «Ese es el problema que abordamos: el riego uniforme toma la misma decisión para zonas con condiciones distintas. Se necesita conocer la humedad del suelo en cada sector antes de decidir cuándo regar.»

### Diapositivas 2 y 3 · Solución (0:48–1:55)

**3. Solución.** «Proponemos un sistema modular de medición y control del riego. El módulo central mide su zona y recibe las lecturas de módulos dependientes instalados en otras zonas. Estos módulos se recargan con energía solar y trabajan con batería. La central se conecta al Wi-Fi y envía los datos a una web, donde se ve el estado y el historial por zona.»

«El riego tiene un controlador separado: otro ESP recibe la orden dirigida a una zona y activa su bomba. En nuestra maqueta representaremos el proceso con un controlador y una bomba. Así podemos mostrar la cadena completa: medir, consultar y activar el riego de la zona que corresponda.»

### Diapositiva 4 · Modelo y estrategia (1:55–2:53)

**4. Modelo de negocio.** «La propuesta se ofrecería por módulos. Una instalación comienza con la central y los elementos de una zona, y puede añadir módulos dependientes y controladores según la cantidad de sectores. El precio final se definirá después de comprobar costos y funcionamiento; todavía no afirmamos un ahorro de agua medido.»

**5. Estrategia.** «Empezaríamos con un piloto pequeño en un área verde de San Martín de Porres. Compararíamos lecturas entre zonas, revisaríamos la comunicación con la central y observaríamos la respuesta del controlador. Con esas pruebas ajustaríamos el sistema antes de proponerlo a responsables de parques, instituciones y otros espacios con varias zonas de riego.»

### Diapositiva 5 · Avance y equipo (2:53–3:51)

**6. Tracción o avance.** «Estamos en etapa de propuesta y prototipo. Ya definimos una arquitectura con una central, módulos de medición asociados, una plataforma web y un controlador de bomba para la maqueta. Aún debemos medir la duración real de la batería, comprobar la recarga solar, la comunicación entre módulos y el riego por zonas. Por eso no presentamos resultados de ahorro ni despliegues reales.»

**7. Equipo.** «Somos el Equipo 07 de la Universidad Peruana Cayetano Heredia. Repartimos el trabajo entre investigación, diseño del prototipo, programación y documentación. Esa combinación nos permitirá construir la maqueta, registrar las pruebas y corregir lo que falle.»

### Diapositiva 6 · Pedido y cierre (3:51–4:40)

**8. Pedido.** «Buscamos validar esta prueba de concepto con la asesoría del curso y recibir retroalimentación de quienes gestionan áreas verdes. Pedimos acceso a un espacio pequeño para comparar zonas de suelo y evaluar si el control sectorizado resulta útil en una situación real.»

«La siguiente meta es demostrar que la central puede recoger los datos de sus módulos, mostrarlos en la web y activar mediante el controlador la bomba de la zona indicada. Muchas gracias.»

## Apoyo visual: seis diapositivas

1. **Una misma área, necesidades distintas:** vista de dos sectores con humedad diferente y una pregunta sobre el riego uniforme.
2. **Cómo funciona:** central que también mide; módulos dependientes asociados; web conectada a la central; controlador y bomba separados.
3. **Qué recibe cada zona:** ejemplo visual de historial y orden de riego, marcado como *ilustrativo, sin datos medidos*.
4. **Modelo y piloto:** incorporación gradual de módulos y tres comprobaciones del piloto.
5. **Avance y equipo:** arquitectura definida, pruebas pendientes y funciones del Equipo 07.
6. **Pedido:** espacio pequeño para validar la prueba de concepto y recibir comentarios.

## Antes de entregar

1. Ensayar con cronómetro y recortar el guion si la lectura pasa de cinco minutos.
2. Grabar el video con al menos un integrante y una diapositiva visible.
3. Subirlo a YouTube como **No listado**.
4. Sustituir `PENDIENTE_DE_ENLACE` por la URL real en este archivo.
5. Compartir esa URL en Discord antes de las 23:59 del día previo al siguiente taller.

**Nota:** el nombre comercial sigue sin definirse. En el pitch se usan «módulo central», «módulos dependientes» y «controlador de riego».
