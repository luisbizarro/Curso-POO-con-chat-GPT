# 2. Clases y Objetos

## Definición de una Clase
En C++, una clase se define usando la palabra clave __class__. Aquí tienes un ejemplo básico:

```cpp
#include <iostream>
using namespace std;

// Definición de la clase Coche
class Coche {
public:
    // Atributos
    string color;
    string marca;
    int velocidad;

    // Métodos
    void acelerar() {
        velocidad += 10;
        cout << "La velocidad es ahora " << velocidad << " km/h." << endl;
    }

    void frenar() {
        velocidad -= 10;
        cout << "La velocidad es ahora " << velocidad << " km/h." << endl;
    }
};
```
### Creación y Uso de Objetos
Una vez que has definido una clase, puedes crear objetos de esa clase. Aquí tienes cómo hacerlo:
```cpp
int main() {
    // Crear un objeto de la clase Coche
    Coche miCoche;

    // Asignar valores a los atributos
    miCoche.color = "Rojo";
    miCoche.marca = "Toyota";
    miCoche.velocidad = 0;

    // Usar los métodos del objeto
    miCoche.acelerar(); // La velocidad es ahora 10 km/h.
    miCoche.frenar();   // La velocidad es ahora 0 km/h.

    return 0;
}
```
### Miembros de una Clase
1. Atributos: Son las variables que pertenecen a la clase. En el ejemplo, color, marca y velocidad son atributos de la clase Coche.

2. Métodos: Son las funciones que pertenecen a la clase. En el ejemplo,`acelerar()` y `frenar()` son métodos que operan sobre los atributos del objeto.

### Ejemplo Práctico
Vamos a ver un ejemplo más detallado. Imagina que quieres crear una clase Libro que tenga atributos como titulo, autor y año de publicacion, y métodos para mostrar la información del libro.

```cpp
#include <iostream>
using namespace std;

// Definición de la clase Libro
class Libro {
public:
    // Atributos
    string titulo;
    string autor;
    int anioPublicacion;

    // Método para mostrar información
    void mostrarInfo() {
        cout << "Título: " << titulo << endl;
        cout << "Autor: " << autor << endl;
        cout << "Año de Publicación: " << anioPublicacion << endl;
    }
};

int main() {
    // Crear un objeto de la clase Libro
    Libro miLibro;

    // Asignar valores a los atributos
    miLibro.titulo = "Cien años de soledad";
    miLibro.autor = "Gabriel García Márquez";
    miLibro.anioPublicacion = 1967;

    // Usar el método del objeto
    miLibro.mostrarInfo();

    return 0;
}
```
### Preguntas para Despertar la Curiosidad
1. ¿Cómo puedes usar clases y objetos para modelar otros elementos del mundo real en tus proyectos, como empleados o productos en un inventario?
2. ¿Qué pasaría si quisieras agregar más funcionalidades a la clase `Coche` o `Libro`? ¿Cómo organizarías esos métodos y atributos?
3. ¿Qué diferencias ves entre los métodos que modifican atributos y los que solo muestran información?