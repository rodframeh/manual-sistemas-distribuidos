[TOC]
# Sistemas operativos
- Permite la **administración** de los recursos
	- Se tienen las siguientes premisas:
	  - Los recursos: procesador, memoria y dispositivos de entrada y salida
	  - Los programas **compiten** por utilizar los recursos
	- El sistema operativo **asigna de forma ordenada y controlada los recursos a los programas**. Para realizar esto debe:
		- Llevar un registro de qué programa están utilizando qué recursos
		- Otorgar peticiones de recursos
		- Contabilizar el uso de los recursos
		- Mediar las peticiones en conflicto
	- El sistema operativo hace que los programas compartan recursos según:
		- El **tiempo**: Los programas toman turnos para utilizar los recursos, ej: CPU o impresora
		- El **espacio**: Los programas toman parte del recurso, ej: RAM y disco duro
	- Por lo tanto el sistema operativo impone orden al caos.
- Permite la **abstracción** de los recursos
  - Se tienen las siguientes premisas:
    - Cada recurso tiene un conjunto de instrucciones diferentes y complejas
      - Cada recurso tiene un conjunto de componentes internos (chips, motores, ...)
      - Las instrucciones de un recurso pueden **variar** según la marca, el modelo y la tecnología de sus componentes
      - Por lo tanto un mismo recurso puede tener diferentes o similares conjuntos de instrucciones.
    - Los programadores de aplicaciones y sus aplicaciones requieren utilizar estos recursos.
  - El sistema operativo **abstrae o simplifica estas complejas y diferentes instrucciones en operaciones más simples**
    - Una simple operación de un recurso puede invocar a varias instrucciones complejas
    - Con la abstracción reduce la complejidad de la interacción con los recursos
- Se almacenan en un lugar diferente al común de los programas.
- Son grandes, complejos y de larga duración, por eso es complicado reemplazarlos.
## Partes
- Shell
- La GUI no forma parte del sistema operativo
## Modos de operación
- La mayoría de sistemas operativos tiene los modos operación kernel y usuario
### Modo kernel
- También llamado modo supervisor
- El modo kernel permite ejecutar cualquier instrucción en todo el hardware de la máquina.
- Las instrucciones que afectan control de la máquina, la entrada o salida están permitidas solo para el modo kernel.
- El sistema operativo se ejecuta en modo kernel.
### Modo usuario
- Permite la ejecución de un subconjunto de instrucciones del modo kernel.
- El software del modo usuario es más fácil de cambiar que el del modo kernel.
- La GUI y el shell son el nivel más bajo del modo usuario.