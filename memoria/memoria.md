[TOC]
# Memoria
## Requisitos
- La memoria debe ser:
  - Extremadamente rápida, más rápida que la ejecución de una instrucción para que no detenga a la CPU
  - De gran capacidad
  - Economica
- Ninguna tecnología cumple con todos estos requisitos.
## Jerarquia
- Jerarquia de los tipos de memoria
  - Registros KB
  - Cache MB
  - Memoria principal GB
  - Discos magnéticos GB-TB
- Ordenado de
  - Arriba a abajo según la velocidad y el precio 
  - Abajo a arriba según la capacidad
## Registros
- Ubicados internamente en la CPU
- Su capacidad de almacenamiento es de 32 x 32 bits o 64 x 64 bits depende de la arquitectura de la CPU.
## Cache
### Flujo de la cache
- Un programa necesita leer una palabra de memoria
- Se comprueba si la linea que necesita se encuentra en cache
- **Si se encuentra** la palabra en cache, se obtiene un **acierto de cache**
	- No se envia una petición de la palabra a la memoria principal
	- Por lo general **demora 2 nanosegundos**
- **Si no se encuentra** la palabra en cache, se obtiene un **fallo de cache**
	- Se envia una petición de la palabra a la memoria principal
	- Se inserta el nuevo elemento a la cache
### Niveles de cache
#### L1 o Level 1
- Se ubica dentro de la CPU
- Usualmente alimenta las instrucciones de decodificación del CPU
- Por lo general son de 16KB
- No tiene retraso de velocidad de acceso
#### L2 o Level 2
- Almacena las palabras de datos que se utilizan con frecuencia
- Por lo general son MB
- Tiene un retraso de 1 o 2 ciclos de reloj de velocidad de acceso
- **Modelos**
	- L2 compartida entre los nucleos
		- Utilizado por intel
		- La desventaja: Requiere un controlador de cache complejo 
	- L2 para cada nucleo 
		- Utilizado por AMD
		- Desventaha: Genera inconsistencia de datos
### La memoria principal y la cache
- La **memoria principal** se divide en líneas (line) de cache
- Por lo general las líneas de cache son de 64 bytes
- Ejemplo:
  - **Linea 0**: Con direcciones de 0 a 63
  - **Linea 1**: Con direcciones de 64 a 127
- Las lineas más usadas se ubican en la **cache 1**
## Memoria RAM
- Random Access Memory (Memoria de Acceso Aleatorio), Memoria principal o Memoria de nucleo (antes eran núcleos de ferrita magnetizables).
- Se encarga de satisfacer los **fallos de cache**.
- **Volatil**, es decir, se pierde el contenido cuando se desconecta de la energía.
## Memoria ROM
- Read Only Memory (Memoria de Solo Lectura)
- Se programa de fábrica
- No puede modificarse
- Es rápida y económica
- En algunas máquinas almacena el cargador de arranque (**bootstrap loader**)
## Memoria EEPROM
- Electrically Erasable PROM (PROM Eléctricamente Borrable)
- **No volatil**, es decir, no se pierde el contenido cuando se desconecta de la energía.
- Permite borrar y escribir datos
- Requiere más tiempo para escribir que la RAM.
## Memoria Flash
- **No volatil**, es decir, no se pierde el contenido cuando se desconecta de la energía.
- Permite borrar y escribir datos
- Requiere más tiempo para escribir que la RAM.
- La velocidad está entre el disco magnético y la RAM.
- Si se borra demasiadas veces se desgasta.
## Memoria CMOS
- **Volatil**, es decir, se pierde el contenido cuando se desconecta de la energía.
- Utilizada para almacenar la fecha, hora actual y parametros de configuracion
- Alimentado por una batería que también alimenta al circuito reloj, si falla la batería la computadora empieza a olvidar cosas