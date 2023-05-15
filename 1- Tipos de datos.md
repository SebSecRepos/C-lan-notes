
```c
	char c; // un caracter
	char nombre[] = "sebastián";    //muchos caracteres se define como un array de caracteres
	short s;                       //String de pocos carácteres
	int i;                        // entero >0, <0, 0
	unsigned int ui;              //entero >0
	long l;                       // entero de mayor tamaño
	float f;                     // decimal finito
	double d; //
	long double ld; //
	int array [ 20 ]; //
	int *ptr = array; //
	FILE  
```

El tamaño de los tipos de dato cambiará si la ejecución de **gcc** es
- m32
- m64

```bash
	gcc -m64 ./index.c -o archivofinal
```
	