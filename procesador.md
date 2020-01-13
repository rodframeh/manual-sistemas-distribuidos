[TOC]
# Procesador
## Instrucciones de la CPU
- Ejemplo de instrucciones de una CPU
	- Sumar de dos operadores
	- Cargar de memoria a un registro
	- Almacenar de registro a memoria
## Velocidad de la CPU
- La ley del cofundador de Intel, Gordon Moore específica que el número de transistores se duplica cada 18 meses.
## Ciclo de la CPU
- El ciclo básico para una CPU contiene las siguientes fases:
	- **Obtener** la primera instrucción de memoria
	- **Decodificarla** para obtener su tipo y operandos
	- **Ejecutarla**
	- Repetir hasta terminar el programa.
## Unidades de ejecución separadas
- Cuando para cada fase del ciclo se tiene una **unidad de ejecución separada**, se puede:
	- Tener **paralelismo** de instrucciones al ejecutar más de una instrucción a la vez en una única CPU.
	- Tener un **buffer de contención** donde se depositan las instrucciones decodificadas para luego ser ejecutadas por alguna unidad de ejecución libre
	- Tener ejecuciones realizadas en **desorden y no de forma secuencial**
	- Tener una **arquitectura pipeline**.
## Registros
- **Ejecutar una instrucción es más rápido que obtener la instrucción de memoria**, por eso todas las CPUs contienen ciertos registros en su interior que contienen variables clave y resultados temporales.
- Ejemplos de registros:
	- Contador del programa
	- Apuntador del stack
	- PSW Palabra de Estado del Programa
## CPU compartida en el tiempo
- Para compartir la CPU el sistema operativo debe detener el programa de ejecución para reiniciar otro y guarda todos sus registros para restaurarlos cuando el programa continúe su ejecución.
## Instrucción `trap`
- Para utilizar servicios del sistema operativo, un programa usuario debe hacer una llamada al sistema operativo, con la instrucción `trap` (son producidos por el hardware y advierten una situación excepcional) cambia del modo usuario al modo kernel, cuando se ha completado la acción (probablemente la solución de un problema) el control vuelve al programa de usuario.
## Cache
- Mientras la cache tenga un mayor tamaño de almacenamiento, el rendimiento de la CPU incrementará. Pero esto también tienen un límite, cuando el rendimiento comienza a decrecer. 
## Multihilamiento
- El multihilamiento (multithreading) o hiperhilamiento (hiperthreading) permite que la CPU contenga el estado de los dos hilos de ejecución distintos y luego alterné entre uno y otro, 
- El tiempo de alternar entre hilos está en una escala de nanosegundos.
- Cada hilo aparece en el sistema operativo como una CPU separada.
## Multiprocesador
- Las CPUs con más de un procesador tiene más de un minichip con su propia CPU independiente.