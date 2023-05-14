
#### If
```c
	int a=1;
	
	printf("if \n\n");
	
	if(a==0){
		printf("es igual 0");
	}else {
		printf("es diferente 0");
	}
```

#### Switch
```c
	printf("\n===== switch case =====\n");
	int a=45;
	
	switch(a)
	
	{
		case 0: printf("a es 0"); break;
		case 1: printf("a es 0"); break;
		case 2: printf("a es 0"); break;
		case 3: printf("a es 0"); break;
		case 4: printf("a es 0"); break;
		default: printf("%i, No es ningún número conocido", a); break;
	}

```

#### While
```c

	int a=99;
	while(a!=0){
		system("clear");
		printf("\nEL valor de a es: %i \n", a);
		printf("\nIngrese un valor\n");
		scanf("%d",&a);
	}
	printf("Saliste..");

```


#### Do While
```c

	int a=10;
	do {
	
		system("clear");
		printf("\nEL valor de a es: %i \n", a);
		printf("\nIngrese un valor\n");
		scanf("%d",&a);
	
	}while (a!=0);
	printf("\nSaliste \n");

```

#### For
```c
	int i=0;
	for(i=0; i<5; i++)
	{
		printf("\nEl valor es %i\n", i);
	}
```
