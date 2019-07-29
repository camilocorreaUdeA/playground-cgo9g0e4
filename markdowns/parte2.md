# Miembros de clase en C++: Variables y Métodos

Las variables de clase en C++ son datos de distinto tipo que sirven para describir el estado actual de un objeto de esa clase.
Se declaran al interior de una clase de la misma forma en que se declaran variables en una aplicación convencional de C++. Es decir,
tipo de dato (calificadores opcionales), nombre para la variable y un valor inicial opcional.

Los métodos de una clase son funciones que sirven para manipular las variables de la clase, de ahí viene la primera característica relevante
de la programación orientada a objetos que es el `encapsulamiento`, ya que en lo posible se va a tratar de que solo pueda accederse a una
variable de clase a través de un método de la clase. Los métodos se declaran y definen de la misma manera que una función cualquiera en una
aplicación convencional de C++, dicho de otro modo, en su firma expresan el tipo del valor de retorno, un nombre para el método y una lista
de parámetros de entrada. Usualmente se hace la declaración de los métodos al interior de la clase, mientras que la definición se hace por fuera
de la clase ayudandose del operador de resolución de ámbito `::` para indicar que el método que se está definiendo pertenece a la clase en cuestión.

```cpp
class MiClase
{
	int var1; //Variable de clase
	const double var2 = 3.14159;  //Variable de clase
	
	void cambiarVar1(int a); //Declaración de un método de la clase
	double calcularArea(const double& x, const double& y); //Declaración de un método de la clase
};

void MiClase::cambiarVar1(int a)  //Definición del método por fuera de la clase
{
	var1 = a;
}

double MiClase::calcularArea(const double& x, const double& y) //Definición del método por fuera de la clase
{
	return x*y;
}
```