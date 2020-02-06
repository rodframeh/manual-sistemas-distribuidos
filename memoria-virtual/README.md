# Memoria virtual
- Memoria fisica: Memoria RAM
- MMU: Unidad  de  Administración  de  Memoria,  Memory  Management Unit

- Es un esquema que hace posible la ejecución de programas más grandes que la memoria física.
- Permite expandir la capacidad de la memoria física, al juntar la memoria física y parte del disco duro.
- Utiliza  la  memoria  principal  como  un  tipo  de  cache,  donde  almacena  las  partes  que  se ejecutan  con  más  frecuencia. 
- Este esquema  requiere  la  reasignación  de  direcciones  de  memoria,  para  convertir  la dirección  que  el  programa  género  en  la  dirección  física  de  la  RAM.  Esta  asignación  se realiza  mediante  la  MMU  que  forma  parte  de  la  CPU. 
- En un sistema  de  multiprogramación  al  cambiar  de  contexto  (context  switch)  o programa  la  MMU  y  la  cache,  puede  que  vacíen  todos  los  bloque  modificados  de  la cache  y  modificar  los  registros  de  asignación  en  la  MMU,  esto  reduce  el  rendimiento.