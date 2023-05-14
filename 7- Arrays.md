
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

```c
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