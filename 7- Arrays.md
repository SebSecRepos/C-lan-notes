
Para saber el valor de un array debe multiplicarse el valor del tipo de dato ==sizeof(dato)== por el largo del array

## Array de enteros

```c
		int vector[5]; //peso = 25bytes
		vector[0]=1;
		vector[1]=2;
		vector[2]=3;
		vector[3]=4;
		vector[4]=5;
		
		int i=0;
		for(i=0;i<5;i++){
			printf("vector[%d] = %d\n",i, vector[i]);
		}
```

## Array de char o cadena 

``` c
		int vector[5]; 
		vector[0]=1;
		vector[1]=2;
		vector[2]=3;
		vector[3]=4;
		vector[4]=5;
		
		int i=0;
		for(i=0;i<5;i++){
			printf("vector[%d] = %d\n",i, vector[i]);
		}
```

---

## Arrays y punteros

Cuando apuntamos un puntero a un array, este apunta a la dirección de memoria del elemento de la primera posición del array
``` c
	char vector[5]="holam";
	char pVector=&vector;   ---> Apunta al la dirección de memoria de 'h'
```

Al estar las posiciones de memoria en forma contigua, se puede iterar por los elementos del array incrementando las posiciones de memoria
sin ningún incoveniente

``` c
	int i=0;
	for(i=0; i<5; i++){
		prinf("Vector[%d]= %c ",i,(*vector));
		vector++;
	}
```
En este ejemplo modificamos la dirección de memoria a la que apunta el puntero, incrementandolo en cada iteración.