# Ejercicios práctica 1

1. Primer ejercicio práctico: 

Desarrolle una sencilla aplicación en la que se tienen las siguientes clases:

* Una clase ListadeObjetos es una clase que contiene un arreglo en el que se pueden almacenar objetos de la clase A, el arreglo puede guardar como
máximo 20 objetos de la clase A. 

Debe tener un método para almacenar un objeto de la clase A en el arreglo, este método debe verificar que el arreglo
tenga espacio disponible para guardar el objeto. En caso contrario se debe mostrar un mensaje indicando que el arreglo está lleno.

Debe tener un método para retirar un objeto del arreglo, este método debe verificar que si haya algo para sacar del arreglo, es decir que el arreglo
no vaya a estar vacío, en cuyo caso debe desplegar un mensaje diciendo que no hay nada para sacar de arreglo.

Debe tener un método para desplegar la información de un objeto almacenado en alguna posición del arreglo. Debe verificar que dicha posición si
tiene algo guardado, en caso contrario debe avisar de la situación con un mensaje. Este mismo método debe permitir de manera alternativa que se despliegue la información
de todos los objetos que estén de momento almacenados en el arreglo.

* Una clase A que tiene los siguientes miembros privados:
Un miembro tipo int para un número serial que identifica al objeto

Un miembro tipo std::string para darle una denominación al objeto

* Los objetos de la clase A solo se pueden crear y configuar a través de una función externa llamada "nuevoObjetoLista". Esta función crea un 
objeto de la clase A asignando valores al serial y al nombre del objeto. Luego almacena el objeto en la ListadeObjetos invocando el método
que esta clase tiene para almacenar objetos de la clase A.

* La aplicación debe tener un sencillo menú de opciones que permita ejecutar distintas acciones como agregar objetos a la lista, retirar objetos de la lista o desplegar información de un objeto individual o de todos los objetos de la lista.

2. Segundo ejercicio práctico: 

Desarrolle una aplicación sencilla de Agenda de Citas y Compromisos que tiene las siguientes clases y funcionalidades:

Una clase "Cita" que tiene los siguientes miembros de clase: Miembros para almacenar de manera individual los nombre de las dos personas
que van a reunirse o citarse. Un miembro de clase para almacenar el nombre del lugar donde van a reunirse. Un miembro que es un objeto
de una clase llamada "Fecha".

Dicha clase "Fecha" cuenta con miembros privados para el almacenamiento del año, el mes, el día y la hora, y también un método para
verificar que la fecha sea correcta, es decir, que no hayan más de 12 meses, que la hora no sea superior a 24 horas ni inferior a 0
horas, que el día no sea cero o menor a cero y que respete el máximo de días de acuerdo con el mes, y que verifique si el año es
bisiesto para el caso del mes de febrero. Esta clase tiene una sobrecarga adicional para ese método ya que se debe permitir ingresar
el mes en letras o en números.

Una clase externa "ClaseExterna" que permite crear objetos de la clase "Cita" que tiene un método que permite crear una cita, este método recibe como parámetros de entrada todos los datos para almacenar en los miembros del objeto cita. Además este método debe ir agregando las citas que se van creando en una lista de citas (la lista puede guardar máximo 10 citas). Dicha lista debe poder ser consultada a través de una función externa llamada "consultarCitas".

Agregue un pequeño menú de opciones que permita crear citas e ir agregandolas a la lista de citas y también visualizar las citas que ya se han agendado.
