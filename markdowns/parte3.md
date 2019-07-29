# Acceso a miembros privados de una clase: Funciones y Clases "Amigas"

Una función o una clase "Amiga" es aquella a la que se le ha otorgado la capacidad de tener acceso a los miembros privados de la clase que la
ha declarado como amiga. Para que una clase declare a otra clase o a una función como amiga se debe declarar esa función o esa clase al interior de
la clase y se debe utilizar la palabra reservada `friend` en esa declaración.

Nota: La amistad en C++ es unívoca, es decir, si la clase A declara a la clase B como amiga eso no quiere decir que la clase B considere a la clase A
como amiga.

Una función amiga o un método de una clase amiga reciben com parámetro de entrada una referencia a un objeto de la clase que las declaro como amiga.

Declaración de una función amiga:

```C++ runnable
#include<iostream>

using namespace std;

class MiClase
{
	public:
	void printMembers();
	friend void funcionAmiga(int x, MiClase& mc); //Se usa la palabra friend y uno de los parámetros es una referencia a la clase MiClase
	private:
	int a;
};

void MiClase::printMembers()
{
	cout<<"El valor de 'a' es: "<<a<<endl;
}

void funcionAmiga(int x, MiClase& mc)
{
	mc.a = x; //Acceso a un miembro privado del objeto mc de la clase MiClase
}

int main()
{
	MiClase obj;
	funcionAmiga(5, obj);
	obj.printMembers();
	
	return 0;
}
```
Declaración de una clase amiga:

```C++ runnable
#include<iostream>

using namespace std;

class MiClase
{
	public:
	void printMembers();
	friend class OtraClase; //Se usa la palabra friend y se nombra la clase amiga
	private:
	int a;
};

void MiClase::printMembers()
{
	cout<<"El valor de 'a' es: "<<a<<endl;
}

class OtraClase
{
	public:
	void metodoClaseAmiga(int x, MiClase& mc);
};

void OtraClase::metodoClaseAmiga(int x, MiClase& mc)
{
	mc.a = x; //Acceso a un miembro privado del objeto mc de la clase MiClase
}

int main()
{
	MiClase obj;
	OtraClase obj2;
	obj2.metodoClaseAmiga(10, obj);
	obj.printMembers();
	
	return 0;
}
```
