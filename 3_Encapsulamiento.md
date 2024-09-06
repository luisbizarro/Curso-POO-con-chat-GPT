# 3. Encapsulamiento
## ¿Qué es el Encapsulamiento?
El encapsulamiento es un principio fundamental de la Programación Orientada a Objetos que consiste en ocultar los detalles internos de una clase y exponer solo lo necesario. Esto se logra mediante modificadores de acceso que controlan la visibilidad de los atributos y métodos de una clase.

Modificadores de Acceso
En C++, los modificadores de acceso son:

1. `public`:

Los miembros `public` son accesibles desde cualquier parte del programa.
Se utilizan para métodos y atributos que deben ser accesibles fuera de la clase.

2. `private`:

Los miembros `private` solo son accesibles desde dentro de la misma clase.
Se utilizan para ocultar detalles internos y proteger los datos. Solo métodos de la clase pueden acceder a ellos.

3. `protected`:

Los miembros `protected` son accesibles desde dentro de la misma clase y desde clases derivadas.
Se utilizan principalmente en el contexto de la herencia.

### Ejemplo de Encapsulamiento
Veamos cómo aplicar encapsulamiento en la clase `Coche` que definimos anteriormente:
```cpp
#include <iostream>
using namespace std;

class Coche {
private:
    // Atributos privados
    string color;
    string marca;
    int velocidad;

public:
    // Constructor para inicializar atributos
    Coche(string c, string m, int v) : color(c), marca(m), velocidad(v) {}

    // Métodos públicos para acceder y modificar los atributos
    void acelerar() {
        velocidad += 10;
        cout << "La velocidad es ahora " << velocidad << " km/h." << endl;
    }

    void frenar() {
        velocidad -= 10;
        cout << "La velocidad es ahora " << velocidad << " km/h." << endl;
    }

    // Métodos getter y setter
    string getColor() const {
        return color;
    }

    void setColor(const string& c) {
        color = c;
    }

    string getMarca() const {
        return marca;
    }

    void setMarca(const string& m) {
        marca = m;
    }
};

int main() {
    // Crear un objeto de la clase Coche
    Coche miCoche("Rojo", "Toyota", 0);

    // Usar métodos públicos
    miCoche.acelerar();
    miCoche.frenar();

    // Acceder a los atributos a través de métodos getter
    cout << "Color del coche: " << miCoche.getColor() << endl;
    cout << "Marca del coche: " << miCoche.getMarca() << endl;

    // Modificar atributos usando métodos setter
    miCoche.setColor("Azul");
    miCoche.setMarca("Honda");
    cout << "Nuevo color del coche: " << miCoche.getColor() << endl;
    cout << "Nueva marca del coche: " << miCoche.getMarca() << endl;

    return 0;
}
```
### ¿Por Qué es Importante el Encapsulamiento?
1. Protección de Datos: Previene modificaciones inesperadas o incorrectas de los atributos internos de la clase.
2. Abstracción: Permite a los usuarios de la clase interactuar con ella a través de una interfaz pública, sin necesidad de conocer los detalles internos.
3. Flexibilidad: Hace que sea más fácil realizar cambios en la implementación interna sin afectar a otras partes del programa.

## Preguntas para Despertar la Curiosidad
- ¿Cómo crees que el encapsulamiento puede ayudarte a evitar errores en proyectos grandes al mantener los detalles internos ocultos?
- ¿Qué problemas podrían surgir si los atributos de una clase fueran públicos y accesibles desde cualquier parte del código?
- ¿Cómo utilizarías los métodos getter y setter para implementar restricciones adicionales en los atributos de una clase?
