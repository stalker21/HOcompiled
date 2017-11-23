1. Escriban que esperan de cada uno de los pasos.
2. ¿Qué agregó el preprocesador?
3. Identificar en las rutinas de assembler las funciones.
4. Explicar qué quieren decir los símbolos que se crean en el objeto.
5. ¿En qué se diferencian los símbolos del objeto y del ejecutable?

2. El preprocesador agregó el contenido completo del archivo calculator.h
3. Al compilar en assembler aparecen las instrucciones  push, call, leave, ret y mov, entre otras. Mov mueve el contenido de los operandos. "push" sirve para introducir los argumentos de la función al stack o espacio de memoria antes de llamar a la función con "call". En este caso, las funciones que se llaman son main, add_numbers y printf. Para terminar la función se utiliza "leave" seguido de "ret" con un argumento extra para indicar la cantidad de bytes que se utilizaron en el stack (para el caso de add_numbers, por ejemplo, los argumentos serían 7 y 8 bytes).  
4. Los símbolos que se crean en el objeto son descriptores de registro y de posición (representados por letras en minúscula y mayúscula), los cuales son utilizados por el compilador para consultar la disponibilidad en el registro y la ubicación en memoria de los valores del código.  
