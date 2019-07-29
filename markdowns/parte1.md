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
clase como un tipo de dato personalizado, similar a las estructuras (`structs`), donde cada programador define los miembros que va a
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

Para declarar una clase en C++ se utiliza la palabra reservada `class`, se da un nombre a la clase y luego entre llaves
se declaran los miembros de la clase.

Las clases no pueden declararse al interior de funciones, ya que son una definición de un tipo de dato creado por el usuario (programador).
En general, las clases se declaran en bibliotecas (librerías) individuales cuyo nombre es usualmente el mismo nombre de la clase.

```cpp
class MiClase
{
  //Aquí van los miembros de la clase: Variables y funciones
}; //NO olvidar el ;
```
Los objetos, tal como se había mencionado con anterioridad, son variables (instancias) del tipo de dato definido por una clase. Por tanto, los
objetos se pueden declarar al interior o por fuera de funciones, tal y como una variable local o global respectivamente. Pueden ser declarados
como miembros de otras clases, es decir al interior de otras clases. Luego, para declarar un objeto primero se utiliza el mobre de la clase a la
que pertenece el objeto seguido de un nombre para el objeto y de una lista opcional de inicialización entre paréntesis. Dicha lista se verá más
adelante.

```cpp
MiClase objetoGlobal;  //Declaración de un objeto global de la clase MiClase

int main()
{
	MiClase objetoLocal; //Declaración de un objeto local de la clase MiClase  
}
```

# Encapsulamiento y nivel de acceso a miembros de la clase

El acceso a los miembros de una clase solo puede lograrse a través de una instancia de esa clase, es decir, de un objeto de dicha clase.
De modo que para acceder a un miembro en específico de una clase se llama al objeto recién declarado y con ayuda del operador punto `.` se hace
el llamado a la variable o método al cual se requiere acceder.

```cpp
int main()
{
	MiClase miObjeto; //Declarando un objeto de la clase
	
	miObjeto.cambiarVar1(5); //Accediendo a un miembro con el operador punto
	double var = miObjeto,calcularArea(34.6, 23.9); //Accediendo a un miembro con el operador punto
}
```