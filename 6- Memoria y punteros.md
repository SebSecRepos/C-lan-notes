
Cada elemento en C ocupa espacio en memoria y por cada espacio en memoria correspondiente a 1 byte, es una dirección de memoria.
Por ejemplo un char ocupa 1 byte y un int ocupa 4 bytes en sistemas de 64 bits.


>Para acceder al valor de memoria de un elemento, se utiliza el operador & seguido del elemento.


Un puntero es una variable que apunta a la dirección de memoria de otro elemento, pero que a su vez ocupa también un espacio en memoria.
```c
	int num=20;
	
	int *pnum=&num;  //Apunta a la dirección de memoria de num
```

Esto a veces confunde, debido a que los elementos como un int, ocupan mas de un espacio en memoria, en el caso del int ocupa 4 espacios, osea
4 bytes, entonces ¿A dónde apunta el puntero?


Como quizás se te haya ocurrido si, apunta al primer espacio en memoria, y con eso es suficiente ya que los siguientes 3 bytes del int son contiguos
en la memoria, por tanto si por ejemplo hacemos:
```c
	printf("%p", pnum++);  //Vamos a ver la dirección de memoria del segundo byte ya que con el ++ avanzó una posición contigua
```
---


### ¿A que valores accede el puntero?

Los punteros  tienen por tanto acceso a 3 valores:

- Su propia dirección de memoria (Utilizamos el operador &). 
```c
	printf("%p", &pnum);  ---->  0x14EF4ET3
```


- La dirección de memoria a la que apuntan, osea la dirección en memoria de num
```c
	printf("%p", pnum);   ----->  0x23EF4ET3
```


- Y por último el contenido de num (Utílizamos el operador \*)
```c
	printf("%p", pnum);   -----> 20
```

----


>Como bien vimos el puntero se declara con un tipo de dato, por tanto si se cambia, debe apuntar a datos que sean del mismo tipo

### Modificación de punteros y de objetos mediante punteros

Si queremos cambiar a que objeto apunta el puntero:
```c
	int num1=20;
	int num2=30;
	
	int *pnum=&num1;   //----> Apuntando a num1 

	pnum=&num2;        //----> Apuntando a num2
```

Si queremos modificar el valor de un elemento a travez de su puntero:
```c
	int num1=20;
	
	int *pnum=&num1;   //----> Apuntando a num1 
	*pnum=23;          //cambiamos el valor de num1 a travez del puntero
```