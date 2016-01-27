
#Programación Orientada a Objetos
La programación orientada a objetos es el paradigma de programación dentro de la programación imperativa que se basa en el uso de objetos y sus relaciones para construir programas y aplicaciones.
Un objeto está caracterizado por:

- Su estado: Conjunto de datos que posee
- Su comportamiento: Conjunto de métodos a los que responde
- Su identidad: Identificador interno

##Clase
Una clase es una colección de métodos y datos que se utiliza como plantilla para instanciar objetos.
    
	#Esto es una clase en lenguaje Ruby
	class MyClass
	end

##Objeto
Un objeto es una instancia de una determinada clase:

    #Esto es un objeto de la clase MyClass
	obj = MyClass.new

##Métodos de acceso
Los métodos de acceso son aquellos que nos permite acceder y/o modificar el estado de un determinado objeto. Tenemos dos tipos de métodos de acceso:

-	Getters: Nos muestran el valor de una determinada variable de instancia de un objeto.
-	Setters: Nos permiten modificar el valor de una determinada variable de instancia de un objeto.

- ###Encapsulación:
Es el concepto de la P.O.O. que consiste en ocultar el estado de un objeto para evitar que este pueda ser alterado por otro objeto de una manera directa sin acceder o utilizar los métodos de acceso o interfaz que proporciona el objeto para su estado.

##Herencia
La herencia es el concepto dentro de la P.O.O que permite a una clase, llamada clase hija/subclase, acceder a los métodos y variables de una clase madre o superclase. Según el tipo de herencia estamos hablando de:

-	Herencia simple: Una clase solo puede tener una clase madre o superclase
-	Herencia múltiple: Una clase puede tener varias clases madres

Además en función del tipo de acceso que se tenga a los métodos y datos heredados también podemos distinguir entre:

-	Herencia pública: Los datos y métodos públicos de la clase madre son públicos en la clase hija, y los métodos y datos protegidos de la superclase son protegidos en la clase hija.
-	Herencia protegida: Los datos y métodos públicos y protegidos de la clase madre son protegidos en la clase hija.
-	Herencia privada:  Los datos y métodos públicos y protegidos de la clase madre son privados en la clase hija.

- ###Clase Abstracta:
	Es aquella que posee métodos que no están definidos dentro de ella y que se definirán en una clase hija.

- ###Clase Concreta:
	Es una clase que no posee ningún métodod que no esté definido dentro de ella.

##Polimorfismo
El polimorfismo es el concepto dentro de la POO que consiste en escribir código que puede ejecutarse con objetos de múltiples clases y tipos a la vez.

-	La clase de un objeto es siempre la misma, es la que se le asigna cuando se hace la instancia del objeto.
-	El tipo del objeto hace referencia al comportamiento del objeto, a lo que el objeto sabe hacer, es decir, a los métodos que responde.


