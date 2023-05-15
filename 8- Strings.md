Los strings o cadenas de carácteres no son nada menos que arreglos de carácteres.
Hay varias formas de declararlos e inicializarlos.

La mas sencilla y cómoda es sin definir el tamaño previamente, para ello utilizamos comillas dobles ==" "==, de esta forma el tamaño del dato se asigna
automáticamente.
``` c

	char nombre[]="pepe";

```

Una mas detallada es definir caracter por caracter en el array, y previamente estableciendo el tamaño del  arreglo.
``` c
	
	char apellido2[6]={'p','e','r','e','z'\0'};

```
El último carácter que vemos es el que indica que finalizó la cadena y es imprescindible, en el primer ejemplo, este caracter esta implícito.


La una menos común es definir posición por posición.
``` c

	nombre[0]='p';
	nombre[1]='e';
	nombre[2]='p';
	nombre[3]='e';

```


Y otra es utilizar la función strcpy(char[], valor)
``` c
	
	strcpy(nombre, "pepe");

```

----


### Función %s en printf() ==Importante==

>SI te preguntas por que al pasarle a printf() una cadena es necesario un **puntero** a la cadena o es necesario pasarle la dirección de memoria del
  primer caracter de la cadena de caracteres aquí esta la aplicación.

>Al ser una cadena de caracteres un array y por tanto sus posiciones en memoria contiguas al pasarle la primer dirección de memoria la función 
   %s del printf(), lo que hace es iterar en la memoria a partir de esa dirección hasta que llega al caracter =='\0'== de esta forma recorre la cadena completa.

#### En el siguiente ejemplo programamos el funcionamiento de %s

``` c
	void function leerCadena(char *cadena);
	
	int main(){
		
		char cadena[]="buenosdias"
		char *pCadena=&cadena;

		leerCadena(pCadena);    
		return 0;
	}
	
	void function leerCadena(char *cadena){
		while((*cadena) != '\0'){
			printf("%c", *(cadena++));
		}

	}
	

```
