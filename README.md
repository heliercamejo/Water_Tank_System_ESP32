# Water Tank System
Este proyecto consiste en el planteamiento, investigación y control del nivel de agua en un sistema tanque cisterna y posterior desarrollo de una solución de software. Concretamente como grupo de trabajo 
junto a dos compañeros de universidad, Helier Camejo y Esteban Acevedo todos estudiantes de Ingeniería en Automática, desarrollamos una maqueta del sistema la cual consiste en dos botellas de agua de 5lts
que representan una el tanque elevado y otra el tanque cisterna, este proyecto se desarrollo a favor de un Taller llevado a cabo en la asignatura de Control de Procesos, se mejoro para proyecto final de 
la asignatura de Programa de Desarrollo Hardware y como se siguio la mejora se presento en la Jornada Cientifica a nivel de Facultad y nivel de Universidad.

## Definición del problema
Cuba pierde un 22 por ciento del agua potable distribuida a las viviendas a causa del deterioro de las redes domésticas, según datos del Instituto Nacional de Recursos Hidráulicos (INRH). 
El mal estado de los herrajes hidrosanitarios y los derrames que se generan desde los tanques elevados y las cisternas son los principales causantes de las pérdidas del agua en el interior de las casas, 
[indicó la presidenta del INRH](URL "[Título del enlace](http://www.cubadebate.cu/noticias/2018/03/22/cuba-pierde-millones-de-dolares-al-ano-por-fugas-de-agua-en-las-casas/)http://www.cubadebate.cu/noticias/2018/03/22/cuba-pierde-millones-de-dolares-al-ano-por-fugas-de-agua-en-las-casas/").

## Solucion planteada
Mediante el uso de sensores de presion diferncial MXP10DP, ESP32 y Raspberry Pi 3 o superior se propone generar una infraestructura a nivel local con la cual medir el nivel de agua de los tanques elevado y cisterna, de la siguiente manera:  

Utilizando un sensor MX10DP por cada tanque se busca medir el nivel de agua, esto con el fin de monitorear el gasto de agua, considerar el encendido y apagado del motor, además de regular el flujo de agua de salida del tanque elevado, analizando la información entregada por los sensores a la placa ESP32.

La parte final y no menos importante es el uso de la Raspberry PI, esta actuará como servidor local que se encargar la procesar la información recibida de todas las placas ESP32 la cual será enviada a un servidor local utilizando Apache donde está alojada el resto de la infraestructura, la cual será mencionada más adelante en este post. Es importante el uso de la Raspberry PI, ya que nos permite, a bajo coste energético y monetarios tener un servidor local con capacidades de expansión o mejor dicho, escalabilidad y la posibilidad de expandirse según el cliente lo necesite, ya sea, agregando una Raspberry PI adicional al clúster o removiendo las sobrantes según sea necesario.
