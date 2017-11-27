1. Escriban que esperan de cada uno de los pasos.
2. ¿Qué agregó el preprocesador?
3. Identificar en las rutinas de assembler las funciones.
4. Explicar qué quieren decir los símbolos que se crean en el objeto.
5. ¿En qué se diferencian los símbolos del objeto y del ejecutable?


1. En la etapa de preprocesado, espero que pegue al código el contenido del archivo calculator.h. En la primer etapa de compilación espero que el código preprocesado sea traducido a instrucciones específicas de assembler, lo cual incluye el llamado a las funciones del programa, instrucciones de memoria, etc. En la segunda etapa de compilación, espero que el compilador genere archivos objeto en código máquina, para luego poder linkearlos en la última etapa de compilación.  
2. El preprocesador agregó el contenido completo del archivo calculator.h
3. Al compilar en assembler aparecen las instrucciones  push, call, leave, ret y mov, entre otras. Mov mueve el contenido de los operandos. "push" sirve para introducir los argumentos de la función al stack o espacio de memoria antes de llamar a la función con "call". En este caso, las funciones que se llaman son main, add_numbers y printf. Para terminar la función se utiliza "leave" seguido de "ret" con un argumento extra para indicar la cantidad de bytes que se utilizaron en el stack (para el caso de add_numbers, por ejemplo, los argumentos serían 7 y 8 bytes).

4. Los símbolos que se crean en el objeto son descriptores de registro y de posición (representados por letras en minúscula y mayúscula), los cuales son utilizados por el compilador para consultar la disponibilidad en el registro y la ubicación en memoria de los valores del código. 
Si tipeamos nm calculator.o en el terminal, nos muestra la tabla de símbolos del objeto: 

000000000000003e T add_numbers
                 U _GLOBAL_OFFSET_TABLE_
0000000000000000 T main
                 U printf


