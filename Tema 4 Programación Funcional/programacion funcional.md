#Programación Declarativa (en Ruby)

> In computer science, declarative programming is a programming paradigm—a style of building the structure and elements of computer programs—that expresses the logic of a computation without describing its control flow.[1]


##Bloque
Un bloque en Ruby es un conjunto de código que va entre llaves, o entre un do-end. Se caracteriza porque no es un objeto y porque solo puede ser usado si es pasado como parámetro a un método e invocado desde dentro del método con un *yield*. Además pueden ser devueltos como un resultado.

    { puts ("Esto es un bloque") }

	do 
		puts ("Esto es un bloque")
	end

##Iterador
Un iterador es un mecanismo que nos permite recorrer una estructura sin importar su contenido. Por ejemplo *each* en Ruby.

##Funciones de Orden Superior. (HOF)
Las funciones de orden superior son aquellas que se pueden pasar como parámetro y devolver como resultado.
> Otra de las características comunes de los lenguajes funcionales es tratar a las funciones como «ciudadanos de primera clase». Es decir, las funciones son valores más o menos normales que se pueden pasar como parámetros, asignar a variables y devolver como resultado de la llamada a una función. Las funciones que utilizan esta característica, es decir, que manipulan o devuelven funciones, reciben el nombre de funciones de orden superior. Afortunadamente, muchos lenguajes populares tienen este tipo de funciones.
La primera vez que uno se encuentra funciones de orden superior puede pensar que sus usos son limitados, pero realmente tienen muchas aplicaciones. Por un lado, tenemos las funciones y métodos que traiga el lenguaje de serie, por lo general de manejo de listas. Por otro, tenemos la posibilidad de escribir nuestras propias funciones y métodos de orden superior, para separar o reutilizar código de manera más efectiva.[2]

Veamos un ejemplo de lo primero en Ruby. Algunos de los métodos de la clase Array reciben una función como parámetro (en Ruby se los llama bloques), lo que permite escribir código bastante compacto y expresivo:

    # Comprobar si todas las palabras tienen menos de 5 letras
	if words.all? {|w| w.length < 5 }
   	# ...
	end

##Clausura
Una clausura es un conjunto de código que tiene asociado un ambiente, y el ambiente es el conjunto de variables que estaban definidas en el ámbito en el que se creó la clausura. Para crear clausuras en lenguaje Ruby tenemos que hacerlo a partir de bloques y utilizando o bien la clase *Proc* o el método *lambda* del módulo Kernel.
La diferencia entre Proc y lambda es que Proc no comprueba el número de parámetros que se le pasan a la clausura y en cambio lambda si, y no deja realizar la llamada o ejecución de la clausura si el número de parámetros no es el correcto. Cuando pasamos un Proc/lambda como parámetro a un método lo hacemos junto con su ambiente, por lo que no ve las variables locales a la función.

	#Esto es un ejemplo de clausura a partir de un bloque que recibe un parámetro
    a = Proc.new {|x| puts x} 
	b = lambda {|x| puts x}
	
	#Para ejecutar
	a.call("Hello World") => "Hello World"
	b.call("Hello World") => "Hello World"

	#Proc permite hacer esto
	a.call("Hello World", "Hola Mundo") => "Hello World"
	
	#En cambio con lambda
	b.call("Hello World", "Hola Mundo") => `block in <main>': wrong number of arguments (2 for 1) (ArgumentError)



Hay una sintaxis alternativa para definir lambdas que es:

    a = ->(x) {....}
	a = -> x {}
	a = -> x do .... end
	#Variables con valor por defecto	
	a = -> x,j=0 {}
	#Definiendo i,j como variables locales a la clausura
	a = -> (x,y;i,j) {}

También se pueden crear clausuras pasando un bloque como parámetro a un método y poniendo un ampersand:

    def create_block(&block)
		block
	end

	bo = create_block {|arg| puts "The argument is #{arg}"}





1. Lloyd, J.W., Practical Advantages of Declarative Programming
2. [Lecciones de aprender un lenguaje funcional](http://emanchado.github.io/camino-mejor-programador/html/ch04.html)