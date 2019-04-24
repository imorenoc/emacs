Emacs
=====


Comandos generales
------------------



**Instalar paquetes**

    M-x package-list

i para seleccionar, x para instalar, u para deseleccionar


	**Teclas para desplazarse** 


	You can move by words.

	C-f : move forward a character
	C-b : move backward a character

	M-f : move forward a word
	M-b : move backward a word

	C-a : move to the beginning of a line
	C-e : move to the end of a line

	M-a : move to beginning of a sentence
	M-e : move to the end do a sentences

	Two other important cursor motion are M-< (META Less-than), which moves to the beginning of the whole text, and M-> (META Greater-than), which moves to the end pf the whole text.

	C-u 8 C-f , moves forward eigh characters.
	C-u 5 C-n
	C-u 6 C-p



**Ingresar un columna** 

    M-x cua-mode
    Seleccionas la columna a modificar
	C-RET


**Insertar un archivo en otro**

 Si deseas insertar un archivo dentro de otro, simplemente abre un archivo muevete a donde deseas posicionar la información del otro y presiona

	C-x i

Indentar toda una seccion

    C-u x i

### Revisar ortografía ###

M-$

    Revisa y corrige la palabra actual (ispell-word)

M-x ispell

    Revisa y corrige todas las palabras en el buffer

M-x ispell-region

    Revisa y corrige en una región

M-x flyspell-mode

    Habilita el modo de corrección al escribir, resaltando las palabras erroneas.


### INSERTING AND DELETING


Remember that most Emacs commands can be given a epet count; this includestext characters. Repeting a text character inserts it several times.

>> C-u 8 * to insert ********

	<DEL>  	      Delete the caracter just before the cursor
	C-d    	      Delete the next character after the cursor

	M-<DEL>	      Kill the word immeduately before the cursor
	M-d	      Kill the next word after the cursor

	C-k	      Kill from the cursor position to end of line
	M-k	      Kill to the end of the corrent sentence

You can also kill a segment of text with one uniform method.
	C-<SPC>	     Then move the cursor to the other end of the text
	C-w	     Finally, type C-w
This kill all the text between the two pasitions.

Reinserting killed text es called "yanking". You can yank the killed text either at the same place where it was killed, or at some ither place in the text you are editing, or even in a different file.


### BUFFERS

	C-x C-b		List buffers

	Type C-x 1 to get rid of the buffer list.

	C-x b	   Switch buffer
	C-x C-c	   Quit emacs

    C-x k    delete a buffer

	C-z	is the command to exit Emacs *remporarily*





R (ESS)
-------

PARA iniciar ESS en emacs podemos utilizar `M-x R`, o también se inicializa cuando ejecutamos con `C-Enter` que ejecuta linea por línea el scrip.

	M-x R
    C-Enter
	C-c C-l		Para leer el archivo (*source()*) simplemente
	C-c`		Si ocurre un erro en el codigo puedes investigar mediante


Para comentar una región primero seleccionamos la región y usamos el momando `M-x comment-region`, para descomentar una región, nuevamente primero la seleccionamos, y usamos `C-u M-x comment-region`.

	M-x comment-region
	C-u M-x comment-region

LaTeX
-----

Para comentar una región, con AUCTex, seleccionamos el texto y utilizamos el comando `C-c ;`. Para marcar como comentario todo un parrafo `C-c %` o `C-c '`. Para eliminar las marcas de comentario, seleccionamos una región, utilizamos `C-u C-c ;` o `C-c :`. Para eliminar comentario `C-c "`

	C-c ;
    C-c % | C-c '
    C-u C-c | C-c :
    C-c "
    C-c C-m | C-c RET

### Modo matemático ###

Para activar el modo matemático (AUC TeX)

C-c ~

Para ingresar una letra griega

$`b -> $\beta
$`g -> $\gamma


###  RefTeX
Here is a summary of the available key bindings.

C-c =      reftex-toc
C-c -      reftex-toc-recenter
C-c (      reftex-label
C-c )      reftex-reference
C-c [      reftex-citation
C-c &      reftex-view-crossref
S-mouse-2  reftex-mouse-view-crossref
C-c /      reftex-index-selection-or-word
C-c \      reftex-index-phrase-selection-or-word
C-c |      reftex-index-visit-phrases-buffer
C-c <      reftex-index
C-c >      reftex-display-index





### eshell

Para ejecutar el shell
	
	M-x eshell
	
Si deseas ejecutar un segundo shell

	C-u M-x eshell



###Cosas practicas

### Trabajando con columnas
Una de las cosas mas tediosas es trabajar columnas, copiar, eliminar o sustituir. Con emacs primero seleccionamos la columna que nos interesa (C-tap), posicionandonos en el inicio y final y después podemos utilizar los siguientes comandos

	kill-rectangle			Ctrl-x r k
	replace-rectangle		Ctrl-x r t
	yank-rectange			Ctrl-x r y
	rectangle-number-lines	Ctrl-x r N

### Alinear Texto
Para alinear texto, e.g.

	x = 32
	y= 23
	z  =13
utilizamos el comando  `align-regexp` e indicamos `=`

	x = 32
	y = 23
	z = 13


Herramientas de emacs
---------------------

    M-x calendar

(+ 2 2)
(this is a quoted list)


