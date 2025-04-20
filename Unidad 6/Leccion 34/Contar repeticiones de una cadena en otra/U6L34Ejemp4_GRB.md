# Bienvenido a tu entrenamiento de C/C++

Código del problema: U6L34Ejemp4_GRB

Un arreglo de una dimensión o vector es un conjunto de datos que son almacenados en
forma continua dentro de la memoria del programa. Todos los datos de un mismo
vector son del mismo tipo de dato

Cada elemento del vector tiene asignado un número de posición o de índice, y son
numerados comenzando desde cero [0] hasta el número [n-1]

![ejemplo.png](ejemplo.png?raw=true)

int vec[5] = { 1 , 2 , 3 , 4 , 5 };

![ejemploFilled.png](ejemplo.png?raw=true)

El número de “índice” o número de posición, en nuestro ejemplo de arriba del 0 al 4,
lo utilizamos para poder hacer referencia o acceder directamente al contenido de un
elemento específico del vector.

En el siguiente ejemplo se declarará un string o cadena de caracteres, que luego puede ser manipulado como un vector de caracteres

string cadena;

**Descripcion del problema**

Leer una cadena de caracteres, sin espacios, solo letras minusculas del abecedario, despues leer otra cadena de un tamaño igual o menor a la primer cadaena. El problema a resolver es cuantas veces aparece la segunda cadena dentro de la primer cadena.

**Explicacion de la solucion:**

### Ejemplo:

estaesunacadenadeentradadeejemplo

ade <---- es la segunda cadena de entrada

**Salida:**

3

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
using namespace std;

int contarOcurrencias(string texto, string buscar) {
    int veces = 0;
    size_t pos = 0;

    while ((pos = texto.find(buscar, pos)) != string::npos) {
        veces++;
        pos += buscar.length();
    }

    return veces;
}

int main(){
int conteo;
    string cadenaA, cadenaB;

    cin >> cadenaA;
    cin >> cadenaB;

    conteo = contarOcurrencias(cadenaA, cadenaB);

    cout << conteo;

    return 0;
}
```
