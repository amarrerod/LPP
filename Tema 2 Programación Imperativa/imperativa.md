
#Paradigma de Programación Imperativo
Se programa dando órdenes a la máquina.
> In computer science, imperative programming is a programming paradigm that uses statements that change a program's state. In much the same way that the imperative mood in natural languages expresses commands, an imperative program consists of commands for the computer to perform. Imperative programming focuses on describing how a program operates - Wikipedia
> 



**ASM  → Programación Procedural  → Programación Estructurada  → Programación Orientada a Objetos**

Esta evolución se ha conseguido a base de abstracción y encapsulamiento. Los lenguajes de programación dividen la memoria de la máquina en dos partes:

-	Memoria de programa
-	Memoria de datos:
	-	Zona estática (Static)
	-	Zona de pila (Stack)
	-	Montículo (Heap)

##Registro de Activación (Stack Frame)##
Un registro de activación *Stack Frame* es una estructura dinámica que almacena información sobre las subrutinas activas en una computadora. Se compone de:

- Valor a devolver
- Parámetros
- Zona de control
- Variables locales
- Variables temporales

![Stack Frame](https://abrickshort.files.wordpress.com/2006/11/stackframe.jpg)

##Programación Procedural

Es el paradigma de programación dentro de la programación imperativa que se caracteriza porque se basa en un número muy bajo de expresiones repetidas, agrupándolas bajo un mismo procedimiento o función para invocarlo cada vez que sea necesaria su ejecución.

    static int a=10, b=20, c;
	int suma(a,b){
		return a+b;	
	}

	int main(){
		c = suma(a,b);
	}

##Programación Estructurada
Es el paradigma de programación dentro de la programación imperativa que se caracteriza porque se basa en el uso de subrutinas y en el *Teorema Fundamental de la Estructura*. Se pueden producir efectos laterales.
El *Teorema Fundamental de la Estructura* dice que siempre se va a poder escribir un programa sin hacer uso de sentencias *go to*, y que ese programa tendrá:

- Sentencias secuenciales
- Sentencias condicionales
- Sentencias repetitivas

Y que el uso de la sentencia *go to* se considera perjudicial porque el programa se ejecuta secuencialmente hasta que llega a una sentencia go-to que trasfiere el flujo de control del programa incondicionalmente hasta otro punto. Nos genera un código spaghetti, que es un muy difícil de depurar. Y por lo tanto, para cualquier programa que haga uso de la sentencia *go to* existirá otro equivalente que no haga uso de ella.

