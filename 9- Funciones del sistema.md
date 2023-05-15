Primero vamos a ver funciones propias del sistema, que nos serán útiles para crear nuestros programas, para hacer uso de ellas hay que
importar librerías del sistema operativo.


### strcpy()
Una que vimos anteriormente se llama ==strcpy()== de la librería #string  lo que hace es asignar valor a una variable de tipo cadena de caracteres,
recibe la cadena de caracteres, y luego el valor.

----



### sizeof( ==elemento== )
Sizeof() nos devuelve el peso en bytes de un elemento

------


### strlen( ==array== )
Strlen() nos devuelve la longitud en cantidad de elementos de un array.

------



# Funciones de manejo de archivos


Funciones para leer y editar archivos: ==fopen()==, ==fwrite()==, etc de la librería stdio.h

### fopen():

- Primer parámetro:          "url del archivo"
- Segundo parámetro:     
> =="r"==   ----> Solo para lectura de archivos existentes
> =="w"==   ----> Solo para escritura de archivos existentes o no
> =="a"==   ----> Solo para escritura añadiendo el contenido al final 
> =="rb"==   ----> Solo para lectura de archivos binarios que ya existan
> =="wb"==   ----> Solo para escritura de archivos binarios existentes o no
> =="ab"==   ----> Solo para escritura de archivos binarios existentes o no, agrega el contenido al final

----

### fwrite():

Fwrite requiere varios parámetros pero el mas importante es que halla un puntero a un archivo abierto por fopen()

- Primer parámetro:         Cadena de caracteres
- Segundo parámetro:     El tamaño  de cada elemento de la cadena  ( sizeof() )
- Tercer parámetro:         La longitud del texto ( strlen() )
- Cuarto parámetro:         El puntero al archivo que abrimos con fopen()

``` c

	FILE * miFile=fopen("./texto.txt", "a");

	if ( myfile !=0 ){

		char texto[]="holamundo";
		frwite(texto, sizeof(texto[0], strlen(texto), mifile));
		fclose(mifile);   //fclose cierra el archivo
	} 

```

### fseek():

Cuando manejamos un archivo, siempre utilizamos un puntero de esta forma nos desplazamos en la posición en memoria que ocupa dicho archivo,
esto nos permite entre otras cosas ver si tamaño.
fseek() nos permite realizar esta maniobras.

##### Parámetros
- Primer parámetro      ------->   El puntero al archivo abierto con fopen()
- Segundo parámetro  ------->   Una variable de tipo **long**, que especifica hacia que lado se recorre el archivo, si es positivo o negativo cambia de dirección
- Tercer parámetro     -------->   Hay 3 opciones 
								-   `SEEK_SET` (0): El desplazamiento se calcula desde el principio del archivo.
								-   `SEEK_CUR` (1): El desplazamiento se calcula desde la posición actual del puntero.
								-   `SEEK_END` (2): El desplazamiento se calcula desde el final del archivo.