# Arquitectura propuesta del sistema de riego

**Estado:** diseño para maqueta y pruebas. El proyecto todavía no documenta mediciones de autonomía, ahorro de agua ni una instalación en campo.

## Componentes y responsabilidades

| Componente | Función | Comunicación y energía |
| --- | --- | --- |
| Módulo central (ESP32-S3) | Mide su propia zona, recibe lecturas de módulos dependientes y reúne el estado de las zonas. | Se comunica localmente con los módulos asociados y por Wi-Fi con la web. Batería y recarga solar previstas. |
| Módulo dependiente (ESP32-C3) | Mide la humedad del suelo de una zona adicional. | Envía lecturas a la central asociada. Batería y recarga solar previstas para cada unidad. |
| Plataforma web | Muestra estado e historial separados por zona; permite solicitar riego. | Intercambia datos y órdenes a través de la central. |
| Controlador de riego (ESP independiente) | Recibe la orden de la zona asignada y acciona una bomba. | En la maqueta se probará un controlador con una bomba. Su alimentación se definirá según la bomba elegida. |

La lectura prevista es aproximadamente cada cinco minutos, sujeta a pruebas de energía y alcance. La central también funciona como punto de medición, de modo que una central y un módulo dependiente representan dos zonas medidas.

## Flujo previsto

1. La central y los módulos dependientes miden la humedad de sus zonas.
2. Los dependientes transmiten sus lecturas a la central. La central envía los datos por Wi-Fi a la web.
3. La persona consulta el historial por zona y solicita riego cuando corresponda.
4. La orden se dirige al controlador de la zona; este activa la bomba asociada.
5. La maqueta demostrará una bomba y un controlador. Ampliar a varias zonas requerirá probar la asociación de cada controlador y su suministro de agua.

## Pruebas pendientes

- Calibrar los sensores por tipo de suelo y comparar las lecturas.
- Comprobar alcance y fiabilidad de la comunicación local y la conexión Wi-Fi de la central.
- Medir consumo, duración de batería y recarga solar de la central y de cada dependiente para sustentar la autonomía.
- Verificar que una orden para una zona solo active el controlador y la bomba correspondientes.
- Definir comportamiento seguro ante pérdida de conexión o falta de agua antes de operar fuera de la maqueta.

El nombre comercial del proyecto está pendiente.
