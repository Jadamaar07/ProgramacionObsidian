## POO
#poo es un paradigma de programación, en el cual se basa en Clases y Objetos, que son capaces de representar entidades, objetos y conceptos mediante estas.

---
## Clases 

### <span style="color: blue;">Como lo entiendo:  </span>
Las #clases son moldes especificos que definen directamente el comportamiento de un Objeto 
# Teoría de Clases en Java y en General

La programación orientada a objetos (POO) es un paradigma que utiliza "clases" y "objetos" para organizar el código y facilitar su mantenimiento y reutilización. En Java, las clases son uno de los conceptos fundamentales de este paradigma. A continuación, se presenta una explicación sobre las clases en Java y en general.

## ¿Qué es una Clase?

Una **clase** es una plantilla o un modelo que define las características y comportamientos de un tipo de objeto. En términos más técnicos, una clase es una estructura que encapsula datos (atributos) y métodos (funciones) que operan sobre esos datos.

### Componentes de una Clase

1. **Atributos (o Propiedades)**: Son las variables que definen el estado de un objeto. Por ejemplo, en una clase `Coche`, los atributos podrían ser `color`, `marca`, `modelo`, etc.

2. **Métodos**: Son las funciones que definen el comportamiento de los objetos de la clase. Por ejemplo, en la clase `Coche`, podrías tener métodos como `acelerar()`, `frenar()`, `tocarBocina()`, etc.

3. **Constructores**: Son métodos especiales que se utilizan para crear instancias de la clase. Un constructor tiene el mismo nombre que la clase y no tiene un tipo de retorno. Se puede sobrecargar, lo que significa que puedes tener múltiples constructores con diferentes parámetros.


---
## Objetos
### <span style="color: blue;">Como lo entiendo:  </span>
Los #objetos son la instanciacion de la clase mediante el contructor.
# Teoría de Objetos en Java y en General

En la programación orientada a objetos (POO), un **objeto** es una instancia de una clase. Los objetos son fundamentales para este paradigma, ya que representan entidades del mundo real y encapsulan tanto datos como comportamientos. A continuación, se presenta una explicación sobre los objetos en Java y en general.

## ¿Qué es un Objeto?

Un **objeto** es una unidad que combina estado (atributos) y comportamiento (métodos). Cada objeto tiene su propia identidad y puede interactuar con otros objetos a través de sus métodos. Los objetos son instancias concretas de una clase, lo que significa que se crean a partir de la definición de una clase.

### Características de los Objetos

1. **Atributo(Estado)**: Representado por los atributos del objeto. Por ejemplo, un objeto `Coche` puede tener atributos como `color`, `marca` y `modelo`.

2. **Metodos(Comportamiento)**: Representado por los métodos del objeto. Por ejemplo, un objeto `Coche` puede tener métodos como `acelerar()`, `frenar()`, y `tocarBocina()`.

3. **Referencia(Identidad)**: Cada objeto tiene una identidad única, que lo distingue de otros objetos, incluso si tienen el mismo estado.


 


---
## Herencia ( cuantas clases pueden ser heredadas ) (estudiar referencia circular y como lo evito)

### <span style="color: blue;">Como lo entiendo:  </span>
La #herencia es la forma de acceder de una clase a otra, compartir sus metodos y sus atributos en mejores palabras heredaralas.
# Resumen de Herencia en Programación Orientada a Objetos

La **herencia** es uno de los conceptos fundamentales de la programación orientada a objetos (POO) que permite crear una nueva clase basada en una clase existente. La clase que se hereda se llama **clase base** o **clase padre**, y la nueva clase se llama **clase derivada** o **clase hija**. La herencia promueve la reutilización del código y establece una relación jerárquica entre las clases.

## Características de la Herencia

1. **Reutilización de Código**: La herencia permite que la clase hija herede atributos y métodos de la clase padre, lo que evita la duplicación de código. Esto facilita el mantenimiento y la extensión del software.

2. **Relación "Es-Un"**: La herencia establece una relación "es-un" entre la clase hija y la clase padre. Por ejemplo, si tienes una clase `Animal` y una clase `Perro` que hereda de `Animal`, puedes decir que un `Perro` es un `Animal`.

3. **Sobreescritura de Métodos**: La clase hija puede modificar el comportamiento de los métodos heredados de la clase padre mediante la **sobreescritura** (overriding). Esto permite que la clase hija implemente su propia versión de un método #overriding.

4. **Constructores**: Los constructores de la clase padre no se heredan, pero la clase hija puede llamar al constructor de la clase padre utilizando la palabra clave `super`.

## Ejemplo de Herencia en Java

Aquí tienes un ejemplo simple que ilustra la herencia en Java:

```java
// Clase padre
public class Animal {
    public void hacerSonido() {
        System.out.println("El animal hace un sonido.");
    }
}

// Clase hija
public class Perro extends Animal {
    @Override
    public void hacerSonido() {
        System.out.println("El perro ladra.");
    }
}

public class Main {
    public static void main(String[] args) {
        Animal miAnimal = new Animal();
        miAnimal.hacerSonido(); // Salida: El animal hace un sonido.

        Perro miPerro = new Perro();
        miPerro.hacerSonido(); // Salida: El perro ladra.
    }
}
```

### Tasks herencia
#DiamonProblem #ReferenciaCircular
* ¿cuantas clases pueden ser heredadas?
No se permite herencias multiples, solo se puede heredar una clase **pero** puede implementar multuples interfaces
* ¿Que es la referencia circular/diamond problem y como evitarla?
La referencia circular es un problema que se causa en Java no explicitamente con las multiples herencias como en caso de lenguajes que acepten esta, sino mas que todo en el caso de las interfaces.
¿Como se soluciona?
La solucion puede ser un Override en la clase que implementa las interfaces, para modificar el metodo dependiendo de la clase o interface que se este utilizando. O siendo explicito en la implementacion del metodo ejemplo:
```java
//Sintaxis `InterfaceName.super.methodName()`.
// Llamar a la implementación de B 
B.super.metodo(); // Salida: Método de B 
// Llamar a la implementación de C 
C.super.metodo(); // Salida: Método de C
```



---
## Polimorfismo 
### <span style="color: blue;">Como lo entiendo:  </span> (~~Parcialmente correcto~~)
El #polimorfismo es la el cambio o la mutacion de los metodos de una clase a un Objeto instanciado por una clase diferente. 
# Resumen de Polimorfismo en Programación Orientada a Objetos

El **polimorfismo** es uno de los conceptos fundamentales de la programación orientada a objetos (POO) que permite que una misma operación se comporte de diferentes maneras según el objeto que la invoque. El término "polimorfismo" proviene del griego y significa "muchas formas". Este concepto es esencial para lograr flexibilidad y extensibilidad en el diseño de software.

## Tipos de Polimorfismo
#tiposDePolimorfismo
1. **Polimorfismo de Tiempo de Compilación (o Estático)**:
   - Se refiere a la capacidad de un lenguaje para resolver la llamada a un método en tiempo de compilación. 
   - Se logra principalmente a través de la **sobrecarga de métodos** (method overloading) y la **sobrecarga de operadores**.
   - Ejemplo de sobrecarga de métodos:

     ```java
     public class Calculadora {
         public int sumar(int a, int b) {
             return a + b;
         }

         public double sumar(double a, double b) {
             return a + b;
         }
     }

     public class Main {
         public static void main(String[] args) {
             Calculadora calc = new Calculadora();
             System.out.println(calc.sumar(5, 10)); // Salida: 15
             System.out.println(calc.sumar(5.5, 10.5)); // Salida: 16.0
         }
     }
     ```

2. **Polimorfismo de Tiempo de Ejecución (o Dinámico)**:
   - Se refiere a la capacidad de un lenguaje para resolver la llamada a un método en tiempo de ejecución.
   - Se logra a través de la **sobreescritura de métodos** (method overriding) y se basa en la herencia.
   - Ejemplo de sobreescritura de métodos:

     ```java
     // Clase padre
     public class Animal {
         public void hacerSonido() {
             System.out.println("El animal hace un sonido.");
         }
     }

     // Clase hija
     public class Perro extends Animal {
         @Override
         public void hacerSonido() {
             System.out.println("El perro ladra.");
         }
     }

     // Clase hija
     public class Gato extends Animal {
         @Override
         public void hacerSonido() {
             System.out.println("El gato maulla.");
         }
     }

     public class Main {
         public static void main(String[] args) {
             Animal miAnimal;

             miAnimal = new Perro();
             miAnimal.hacerSonido(); // Salida: El perro ladra.

             miAnimal = new Gato();
             miAnimal.hacerSonido(); // Salida: El gato maulla.
         }
     }
     ```


- **Polimorfismo Estático (Tiempo de Compilación)**: Se resuelve en tiempo de compilación y se logra a través de la sobrecarga de métodos y operadores.
    
- **Polimorfismo Dinámico (Tiempo de Ejecución)**: Se resuelve en tiempo de ejecución y se logra a través de la sobreescritura de métodos en el contexto de la herencia.
## Ventajas del Polimorfismo

1. **Flexibilidad**: Permite que las funciones y métodos trabajen con diferentes tipos de objetos, lo que facilita la extensión del código sin modificar las clases existentes.

2. **Mantenibilidad**: Al utilizar polimorfismo, el código se vuelve más fácil de mantener y entender, ya que se pueden utilizar interfaces y clases abstractas para definir comportamientos comunes.

3. **Reutilización de Código**: Facilita la reutilización de código, ya que se pueden utilizar métodos genéricos que operan sobre diferentes tipos de objetos.

## Conclusión
El polimorfismo es un concepto clave en la programación orientada a objetos que permite que una misma operación se ejecute de diferentes maneras según el contexto. Al aprovechar el polimorfismo, los desarrolladores pueden crear aplicaciones más flexibles, mantenibles y reutilizables, lo que mejora la calidad del software y reduce el tiempo de desarrollo.

---

## Encapsulamiento
### <span style="color: blue;">Como lo entiendo:  </span>
 El #encapsulamiento es la forma de proteger metodos, parametros y atributos, que no sean accesibles para todos los packcage dependiendo la situacion, donde encontramos public, private y protected 
# Resumen de Encapsulamiento en Programación Orientada a Objetos

El **encapsulamiento** es uno de los principios fundamentales de la programación orientada a objetos que se refiere a la práctica de restringir el acceso a ciertos componentes de un objeto y proteger su estado interno. Este concepto ayuda a mantener la integridad de los datos y a ocultar la complejidad del sistema.

## Características del Encapsulamiento

1. **Ocultamiento de Datos**: El encapsulamiento permite ocultar los detalles internos de un objeto, exponiendo solo lo necesario a través de una interfaz pública. Esto significa que los atributos de un objeto no son accesibles directamente desde fuera de la clase.

2. **Control de Acceso**: Se utilizan modificadores de acceso (como `private`, `protected` y `public`) para controlar qué partes del código pueden acceder a los atributos y métodos de una clase. Esto ayuda a prevenir modificaciones no deseadas y a mantener la integridad del objeto.

3. **Interfaz Pública**: A través de métodos públicos (también conocidos como **métodos de acceso** o **getters y setters**), se puede interactuar con los atributos de un objeto de manera controlada. Esto permite validar o modificar datos antes de que se almacenen.

## Ejemplo de Encapsulamiento en Java

Aquí tienes un ejemplo que ilustra el encapsulamiento en Java:

```java
public class CuentaBancaria {
    // Atributos privados
    private String titular;
    private double saldo;

    // Constructor
    public CuentaBancaria(String titular, double saldoInicial) {
        this.titular = titular;
        this.saldo = saldoInicial;
    }

    // Método público para obtener el saldo
    public double getSaldo() {
        return saldo;
    }

    // Método público para depositar dinero
    public void depositar(double cantidad) {
        if (cantidad > 0) {
            saldo += cantidad;
        }
    }

    // Método público para retirar dinero
    public boolean retirar(double cantidad) {
        if (cantidad > 0 && cantidad <= saldo) {
            saldo -= cantidad;
            return true;
        }
        return false;
    }
}

public class Main {
    public static void main(String[] args) {
        CuentaBancaria cuenta = new CuentaBancaria("Juan", 1000.0);
        cuenta.depositar(500.0);
        System.out.println("Saldo: " + cuenta.getSaldo()); // Salida: Saldo: 1500.0

        if (cuenta.retirar(200.0)) {
            System.out.println("Retiro exitoso.");
        } else {
            System.out.println("Fondos insuficientes.");
        }

        System.out.println("Saldo: " + cuenta.getSaldo()); // Salida: Saldo: 1300.0
    }
}
```
# Modificadores de Acceso en Programación Orientada a Objetos

Los **modificadores de acceso** son palabras clave que se utilizan para especificar el nivel de acceso que tienen los atributos y métodos de una clase. Estos modificadores son fundamentales para implementar el principio de **encapsulamiento**, ya que controlan cómo y desde dónde se puede acceder a los miembros de una clase.

## Tipos de Modificadores de Acceso

En Java, hay cuatro modificadores de acceso principales:

1. **public**:
   - Los miembros (atributos o métodos) declarados como `public` son accesibles desde cualquier otra clase en cualquier paquete.
   - Esto significa que no hay restricciones sobre su acceso.

   ```java
   public class EjemploPublico {
       public int atributoPublico;

       public void metodoPublico() {
           // Código
       }
   }````
2. **private**:

- Los miembros declarados como `private` son accesibles solo dentro de la misma clase en la que se definen.
    
- No pueden ser accedidos desde otras clases, ni siquiera desde clases que heredan de la clase padre.
````java
public class EjemploPrivado {
    private int atributoPrivado;

    private void metodoPrivado() {
        // Código
    }
}
````
3. **protected**:

- Los miembros declarados como `protected` son accesibles dentro de la misma clase, en clases del mismo paquete y en clases que heredan de la clase padre, incluso si están en paquetes diferentes.
    
- Esto permite un mayor nivel de acceso que `private`, pero menos que `public`.
```java
public class EjemploProtegido {
    protected int atributoProtegido;

    protected void metodoProtegido() {
        // Código
    }
}
```

---
### <span style="color: blue;">Segundo fragmento </span>

## Task 
* interfaz(cuantas clases pueden implementar una interfaz, como puedo definir una implementacion en especifico si estas tienen varias) 
* clases abstractas 
* cuando interfaz cuando clase abstracta

## Interfaces: 
Las #interfaces son parecidas a las #clases estas se diferencia en que normalmente contienen metodos uno o mas , es posible crear constantes y lo recomendado es no utilizar variables, por defecto cuando se crean estas siempre vienen implicitamente con public, static y final incluso si se omiten en la declaracion de variables.

---


### <span style="color: blue;">Como lo entiendo </span>


---
### <span style="color: blue;">Tercer fragmento </span>

* Java casting (tipos casting) 
* Java Genericos (que son y que solucionan) estos nacen en Java 5.
---
## ***EXTRA***
***PARA VER EN CLASE (patrones de diseño)
