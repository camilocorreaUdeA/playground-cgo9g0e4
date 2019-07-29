# Programación Orientada a Objetos en C++

El paradigma de programación orientada a objetos es una metodología especial de programación de software
en la que un programa informático se diseña como la interrelación entre un conjunto de instancias conocidas
como objetos. Dichos objetos son entidades que tienen un estado que está descrito por sus variables internas que
se conocen como atributos o propiedades; y que tienen comportamientos que están plasmados en funciones o métodos
que se utilizan para manipular las variables que describen el estado del objeto.

La programación orientada a objetos al igual que la programación estructurada sigue el método de programación imperativa,
es decir, el programador escribe los métodos de forma que se a través de un algoritmo se dicta la funcionalidad de los métodos.

Los objetos que tienen estado y comportamiento idénticos se agrupan o clasifican en "clases".

La programación orientada a objetos ofrece los conceptos de encapsulamiento, abstracción, herencia y polimorfismo.

Puede profundizar acerca del concepto de Programación Orientada a Objetos en los siguientes enlaces:
[POO1](https://es.quora.com/Qu%C3%A9-es-la-programaci%C3%B3n-orientada-a-objetos)
[POO2](https://www.webopedia.com/TERM/O/object_oriented_programming_OOP.html)
[POO3](https://www.freecodecamp.org/news/object-oriented-programming-concepts-21bb035f7260/)

# Clases y Objetos en C++
1. Clases:

Una clase es en general un modelo, receta o plantilla que define el estado y comportamiento de cierto tipo de objetos.
Una clase puede pensarse como una colección de variables (atributos o propiedades) y funciones (métodos) que permiten representar 
un conjunto de datos y especificar las operaciones o procedimientos que permiten manipular tales datos. Se puede inclusive entender una
clase como un tipo de dato personalizado, similar a las estructuras (structs), donde cada programador define los miembros que va a
tener su tipo de dato. De hecho, los tipos de dato nativos de C++ son en realidad clases.

2. Objetos:

Un objeto es una instancia de una clase, es decir una entidad que se construye a partir
de las descripciones consignadas en una clase (datos y funciones). Por tanto, un objeto
se puede entender como una "variable" que se declara del tipo de dato de cierta clase. Un objeto es como tal
la entidad tangible que permite acceder a los datos y funciones modeladas al interior de la clase

Ejemplo:

Una analogía para entender las clases y los objetos puede ser una fabrica ensambladora de carros.
Hay un modelo o diseño (clase) especifico de un auto, pero este modelo en si no es un carro, es solo una descripción 
de que características y funcionalidades deben tener los carros que sean de ese modelo.
Los carros ensamblados en la fabrica de acuerdo a dicho modelo serían los objetos, es decir entidades tangibles que se
construyeron a partir de las descripciones y especificaciones consignadas en el diseño o modelo (o sea la clase).

Clase:
![analog clase](/img/car_class.png)

Objetos:
![analog objeto1](/img/car_obj1.png)
![analog objeto2](/img/car_obj2.png)

Para declarar una clase en C++ se utiliza la palabra reservada class, se da un nombre a la clase y luego entre llaves se declaran los
miembros de la clase.

```cpp
class MiClase
{
  //Aquí van los miembros de la clase: Variables y funciones
}; //NO olvidar el ;
```