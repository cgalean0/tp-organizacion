# tp-organizacion
Participantes:
    - Santiago Miloch - 46768434
    - Nahuel Galeano - 42190957
    - Mikhail Morales - 45701807

Version de CPU Sim utilizada = 4.0.11
Se entregan los archivos:
    - p1 *máquina*
    - ordenar(3) 
    - factorialV2

El principal objetivo del proyecto es dotar al modelo de procesador P1 que estuvimos
desarrollando durante las prácticas de microinstrucciones y de subrutinas con instrucciones
que permitan completar las funcionalidades de la Pila comunes en otras arquitecturas. Esto
permitirá por ejemplo agregar la posibilidad de trabajar con subrutinas que tomen
parámetros de la Pila y que puedan establecer espacios de memoria locales.
Utilizamos p1 como la máquina de nuestro proyecto, que usa una arquitectura de 16 bits, con 4 bit de tamaño de instruccion(opcode), se le agregaron las instrucciones pedidas para el proyecto y nos encontramos con una situación en la que ya no podiamos agregar más instrucciones porque el hardware definido nos limitaba solo a diesiseis instrucciones, debatimos dos opciones; una era agrandar el tamaño de instrucción, lo cual nos flexibilizaría  a la hora de crear más instrucciones, pero esto nos traería el trabajo de modificar todas las intrucciones y microistrucciones ya existentes lo cual iba a ser muy tedioso, y la otra opción, más viable, era eliminar alguna instrucción que no iríamos a usar para ninguno de los dos programas a realizar. Se decidió que eliminar instrucciones que no fueramos a usar era la mejor opción. 
El programa ordenar(3), realiza el orden de dos elementos que el usuario introduzca, el primer input se almacena en el registro A y el segundo en B. Al terminar la ejecución, se almacenará en A el entero menor y en B el entero mayor, y devolverá primer el menor numero y despues el mayor. Este programa utiliza anidamiento de subrutinas de nivel 3.
El programa factorialV2, calcula el factorial de un número positivo mayor a cero que el usuario introduzca mediante el input. Este programa utiliza la pila de recursión mediante la invocación recursiva de la subrutina y da uso de variables locales.  
Ambos programas dan uso de subrutinas con parámetros.
Tanto la máquina como los programas cumplen con lo pedido para realizar el proyecto.
