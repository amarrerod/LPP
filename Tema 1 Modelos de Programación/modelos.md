

#Tema 1: Modelos de Programación.


###¿Por qué hay tantos lenguajes de programación?
Hay tantos lenguajes de programación debido principalmente a 3 motivos:

- 	El avance de la ciencia de la computación
- 	Nuevas necesidades y propósitos específicos
- 	Poder expresivo de los lenguajes

###¿Qué hace que un lenguaje de programación tenga éxito?

-	Fácil de aprender
-	Fácil de implementar
-	Estandarizado
-	Código libre
-	Buenos compiladores
-	Ayudas económicas

###¿Qué es una modelo o paradigma de programación?
Un modelo o paradigma de programación es una abstracción de un sistema de cómputo.
Los más importantes son el paradigma ***imperativo y el paradigma declarativo***.

-	El *paradigma imperativo* se caracteriza porque es de más bajo nivel, más cercano a la máquina y donde la programación se realiza especificando todas y cada una de las instrucciones que se tienen que ejecutar en la máquina obtener la solución del problema. En este paradigma podemos encontrar los siguientes lenguajes de programación:

			-	Von Neumann: FORTAN, C
			-	Scripting: Perl, Ruby, Phyton
			-	O.O: C++, Java
				
-	El *paradigma declarativo* se caracteriza por ser de más alto nivel, nos abstraemos más de la máquina en la que se ejecutará el programa, y programamos diciendo lo que queremos resolver pero a nivel de usuario. Nos podemos encontrar los lenguajes:

			- Funcionales: FP, ML, Haskell, Miranda, Lisp
			- Lógicos: Prolog, Datalog
		


----------
###Lenguaje de Programación
Un lenguaje de programación es un conjunto de caracteres y unas reglas para combinar estos caracteres que especifican el funcionamiento que va a tener cuando se ejecute en una computadora. Los lenguajes de programación son independientes de la máquina en la que se ejecutan y se caracterizan por su sintaxis y su semántica. Donde, 
la sintaxis define la estructura que tienen que seguir las sentencias para ser válidas para un lenguaje de programación y la semántica nos permite conocer el significado de dichas sentencias. Estos dos aspectos son controlados por el compilador. Además, un único lenguaje de programación puede dar soporte a varios modelos de programación.

-	**Compilador:** Es un programa que traduce un programa fuente a un programa equivalente, denominado programa objetivo, que es el que se ejecutará en una computador.
	-	*Un intérprete* es un traductor que no genera programa objetivo, lo que hace es analizar y ejecutar sentencia a sentencia el programa fuente. Una traducción en simultáneo.

####Pasos que sigue el compilador#####
Un compilador se puede dividir en dos partes, *Front-End* y *Back-End*. El *Front-End* es siempre el mismo para un lenguaje de programación concreto y el *Back-End* es específico para la arquitectura de la máquina en la que se va a ejecutar ese lenguaje de programación. Por lo tanto si queremos implementar un compilador podemos reutilizar el *Front-End* para el lenguaje con el que vamos a trabajar e implementar únicamente el *Back-End* específico para la arquitectura de la máquina en la que queremos que se ejecute ese lenguaje de programación.

**Front-End (Tiempo de Compilación):** Se divide en fase de análisis y  fase de síntesis:

-	Fase de análisis
	-	Analizador Léxico: Se encarga de eliminar comentarios, espacios en blanco e identificar los tokens.
	-	Analizador Sintáctico: Agrupa los tokens en función de las reglas del lenguaje.
	-	Analizador Semántico: Significado de las sentencias, hace una análisis de ámbito y de tipo.
-	Fase de Síntesis
	-	Generación de código intermedio: tercetas, cuartetas, p-código.

**Back-End (Tiempo de Ejecución):**

-	Generación de código
-	Optimización del código
-	Ensamblador
-	Linker