# Símbolos 
 
El archivo `visibility.c` tiene muchos tipos de símbolos. En
este trabajo sólo tienen que compilar el objeto `visibility.o` 
e identificar los símbolos, ejecutando:

```
make object
```
Tipeamos -nm visibility.o para ver la lista de símbolos y aparece lo siguiente:

0000000000000000 t add_abs

                 U _GLOBAL_OFFSET_TABLE_ 

000000000000002a T main

                 U printf

0000000000000000 r val1

0000000000000004 R val2

0000000000000000 d val3

0000000000000004 D val4

Los símbolos U_GLOBAL_OFFSET_TABLE y U printf aparecen referenciados en el objeto 

pero son indefinidos (Undefined, o tipo U) o no tienen valor.

t add_abs es un símbolo de texto y remite a una función (local)

T main es un símbolo de texto y remite a una función (global)

r val1 es de sólo lectura y remite a un objeto (local)  

R val2 es de sólo lectura y remite a un objeto (global)

d val3 es un símbolo de datos y remite a un objeto (local)

D val4 es un símbolo de datos y remite a un objeto (global)
