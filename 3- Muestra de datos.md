Como vimos anteriormente, al mostrar los datos con un *==prinf()==* o leer uno por consola con *==scanf()==*, hay que tener en cuenta que dato va a ser

Si es un string %s
```c
	char strg[]="hola";
	
	printf("%s",strg );
```

Si es un char %c
```c
	char car='h';
	
	printf("%c",car );
```

Si es un número se recomiendo %ld  (Long decimal)  o  %d (decimal) 
```c
	double num=2000;
	
	printf("%d",num );
```

Si es una dirección de memoria debe ser %p   (Referencia a puntero)
```c
	double num=2000;
	double *pnum=&num;
	
	printf("%p",pnum);
```