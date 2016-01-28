
#Programación Orientada a Objetos
La [Programación Orientada a Objetos][1] (POO) es el paradigma de programación dentro de la programación imperativa que se basa en el uso de objetos y sus relaciones para construir programas y aplicaciones.
Un objeto está caracterizado por:

- Su estado: Conjunto de datos que posee
- Su comportamiento: Conjunto de métodos a los que responde
- Su identidad: Identificador interno

##Clase
Una [Clase][2] es una colección de métodos y datos que se utiliza como plantilla para instanciar objetos.
    
```ruby
#Esto es una clase en lenguaje Ruby
class MyClass
end
```

##Objeto
Un [Objeto][3] es una instancia de una determinada clase:

```ruby
#Esto es un objeto de la clase MyClass
obj = MyClass.new
```

##Métodos de acceso
Los métodos de acceso son aquellos que nos permite acceder y/o modificar el estado de un determinado objeto. Tenemos dos tipos de métodos de acceso:

-	Getters: Nos muestran el valor de una determinada variable de instancia de un objeto.
-	Setters: Nos permiten modificar el valor de una determinada variable de instancia de un objeto.

- ###Encapsulación:
Es el concepto de la POO que consiste en ocultar el estado de un objeto para evitar que este pueda ser alterado por otro objeto de una manera directa sin acceder o utilizar los métodos de acceso o interfaz que proporciona el objeto para su estado.

##Herencia
La herencia es el concepto dentro de la POO que permite a una clase, llamada clase hija/subclase, acceder a los métodos y variables de una clase madre o superclase. Según el tipo de herencia estamos hablando de:

-	Herencia simple: Una clase solo puede tener una clase madre o superclase

![Herencia Simple](http://2.bp.blogspot.com/-YuYQJcpGSPU/ThGw_VvtWdI/AAAAAAAAADQ/M_GlGBrXZks/s320/herencia.jpg)

-	Herencia múltiple: Una clase puede tener varias clases madres.

![Herencia Múltiple](http://static.commentcamarche.net/es.kioskea.net/pictures/poo-images-animaux2.gif)


Además en función del tipo de acceso que se tenga a los métodos y datos heredados también podemos distinguir entre:

-	Herencia pública: Los datos y métodos públicos de la clase madre son públicos en la clase hija, y los métodos y datos protegidos de la superclase son protegidos en la clase hija.
-	Herencia protegida: Los datos y métodos públicos y protegidos de la clase madre son protegidos en la clase hija.
-	Herencia privada:  Los datos y métodos públicos y protegidos de la clase madre son privados en la clase hija.

- ###Clase Abstracta:
Es aquella que posee métodos que no están definidos dentro de ella y que se definirán en una clase hija.

- ###Clase Concreta:
Es una clase que no posee ningún métodod que no esté definido dentro de ella.

```ruby
class Clase
    def mostrarMensaje
        "#{decir} #{algo}"
    end
end

class SClase < Clase
    def decir (arg)
        "#{arg}"
    end
    
    def algo(arg)
        "#{arg}"
    end
end
```

Los métodos y datos privados de la superclase no son heredados en la subclase y por lo tanto una instancia de la subclase no podrá invocar o acceder a estos métodos y variables. Pero por el contrario, desde la subclase si que se puede invocar a un método de la superclase:

```ruby
class Madre
        def initialize(arg)
            @var = arg
        end
        private
        def metodo ()
            " --> En clase Madre"
        end
    end

class Hija < Madre
        def initialize(arg)
            @x = arg
            super
        end

        def a_method
            cadena = "En clase Hija "
            cadena << metodo
        end
    end
puts(Hija.new("arg").a_method) # => En clase Hija --> En clase Madre
puts(Hija.new("arg").metodo)#private method `metodo' called for #<Hija(MethodError)
```
**Ojo: Private, Protected o Public en Ruby no son palabras reservadas como en la mayoría de lenguajes, se tratas de métodos de instancia definidos en la clase Module.**

- ###Invalidación de un método
La invalidación o *overridden* de un método es el concepto de la POO que consiste en redefinir, en una subclase, un método que ha sido heredado desde una superclase para que cuando este método sea invocado por un objeto receptor instanciado de la clase hija el comportamiento que tenga este método sea el que se redefinió en la clase hija y no el que se había definido previamente en la clase madre.
```ruby 
class ClaseMadre
    def initialize(param)
        @variable = param
    end
    
    def intimo
        "Esto es un metodo de ClaseMadre"
    end
end

class ClaseHija < ClaseMadre
    def initialize(param)
        super
    end
    
    def intimo
        "Este es un metodo de la clase Hija"
    end
end
```


##Polimorfismo
El polimorfismo es el concepto dentro de la POO que consiste en escribir código que puede ejecutarse con objetos de múltiples clases y tipos a la vez.

-	La clase de un objeto es siempre la misma, es la que se le asigna cuando se hace la instancia del objeto.
-	El tipo del objeto hace referencia al comportamiento del objeto, a lo que el objeto sabe hacer, es decir, a los métodos que responde.

![Polimorfismo](http://virtual.uaeh.edu.mx/repositoriooa/paginas/Origenes_beneficios_Programacion_Orientada_Objetos/Polimorfismo.jpg)


[1]: http://www.codeproject.com/Articles/22769/Introduction-to-Object-Oriented-Programming-Concep#OOP
[2]:http://www.codeproject.com/Articles/22769/Introduction-to-Object-Oriented-Programming-Concep#Class
[3]:http://www.codeproject.com/Articles/22769/Introduction-to-Object-Oriented-Programming-Concep#Object


*[POO]: Programación Orientada a Objetos

