Son operadores que permiten cambiar los valores de los elementos sobre si mismos

- Operador de incremento     *==*++
- Operador de decremento    *==*--
- Operador de producto         *==* \*=numero
- Operador de suma               *==* +=numero
- Operador de resta               *==* \-=numero

----

## Orden de modificación

El orden en que se modifica un elemento determina como lo interpreta la estructura de control
```c
	int num = 0;          
    if ( num++ != 0 )    ----- > False
```

En este caso ==*num*==  se incrementa, pero al estar el incremento a su derecha el if primero interpreta a *==num==*  y luego lo incrementa, por tanto
num no es diferente de 0 para el if

En el caso opuesto si es diferente de 0
```c
	int num = 0;          
    if ( ++num != 0 )    ----- > True
```