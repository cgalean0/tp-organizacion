
# Procesador P1 v3
El principal objetivo del proyecto es dotar al modelo de procesador P1 que estuvimos desarrollando durante las prácticas de microinstrucciones y de subrutinas con instrucciones que permitan completar las funcionalidades de la pila (*Stack*) comunes en otras arquitecturas. Esto permitirá por ejemplo agregar la posibilidad de trabajar con subrutinas que tomen parámetros de la Pila y que puedan establecer espacios de memoria locales. 
## Integrantes:
- Santiago Miloch - 46768434 
- Nahuel Galeano - 42190957 
- Mikhail Morales - 45701807

---
## Características
El Software utilizado para la creación de este procesador fue  `CpuSim 4.0.11`.
Todos los archivos necesario en cuanto a el procesador y los pogramas se encuentran en esta carpeta

### Programa 1 - Ordenar Números (ordenar(3))
---
Realiza el orden de dos elementos que el usuario introduzca, el primer input se almacena en el registro A y el segundo en B. Al terminar la ejecución, se almacenará en A el entero menor y en B el entero mayor, y devolverá primer el menor numero y despues el mayor. Este programa utiliza anidamiento de subrutinas de nivel 3.
Ejemplo:
```java
// Pasados como parámetros
7
3
// El programa devuelve
3
7
```


---
### Programa 2 - Calcular Factorial (FactorialV2)
---
Calcula el factorial de un número positivo mayor  o igual a cero que el usuario introduzca mediante el input. Este programa utiliza la pila de recursión mediante la invocación recursiva de la subrutina y da uso de variables locales.  

```java
// Si pasamos 3 como parámetro el programa devuelve
6
```

---
## Mas información sobre la construcción

Utilizamos **p1** como la máquina de nuestro proyecto, que usa una arquitectura de 16 bits, con 4 bit de tamaño de instruccion(opcode), se le agregaron las instrucciones pedidas para el proyecto `LoadStack, SaveStack` además de las otras que ya habíamos realizado durante las prácticas y nos encontramos con una situación en la que ya no podiamos agregar más instrucciones porque el hardware definido nos limitaba solo a 16 instrucciones, debatimos dos opciones; 
> Una era agrandar el tamaño de instrucción, lo cual nos flexibilizaría a la hora de crear más instrucciones, pero esto nos traería el trabajo de modificar todas las intrucciones y microinstrucciones ya existentes lo cual iba a ser muy tedioso.
> La otra opción, más viable, era eliminar alguna instrucción que no iríamos a usar para ninguno de los dos programas a realizar. 

Se decidió que eliminar instrucciones que no fueramos a usar era la mejor opción, fue entonces que optamos por reemplazar las intrucciones:
- `Load`
- `Save`
- `Sub`

Por las siguientes intrucciones:
- `SubR`
- `Mul`
- `JG`

Las cuales ahora permiten hacer multiplicaciones entre regitros, restar entre registros y hacer saltos condicionales cuando el registro A sea mayor o igual a cero.

 Tanto la máquina como los programas cumplen con lo pedido para realizar el proyecto.
