**Utilización de std::lower_bound y std::upper_bound**

En la biblioteca estándar (stl) de C++, las implementaciones de std::lower_bound y std::upper_bound pueden funcionar como una búsqueda binaria para encontrar el índice de un valor o para encontrar la posición donde debería insertarse un valor dentro de un arreglo o un vector ordenado.

Ambas funciones trabajan sobre un intervalo semiabierto [first, last). first corresponde al primer elemento dentro del arreglo, y last corresponde al elemento después del último elemento del arreglo (afuera del arreglo).

first
v
2 3 4 4 5 5 5 5 7 8 \_
^
last

Si queremos buscar un valor k = 5 dentro de los siguientes arreglos, lower_bound nos regresará un iterador al primer valor v del arreglo donde k <= v. En cambio, upper_bound nos regresará un iterador al primer valor v del arreglo donde k < v. Los iteradores funcionan como apuntadores a un rango de elementos y permiten iterar sobre los elementos de ese rango y acceder a ellos.

lower_bound
v
2 3 4 4 5 5 5 5 7 8
^
upper_bound

lower_bound
v
2 3 4 4 5 7 8
^
upper_bound

Si queremos insertar un valor, lower_bound nos indicará la primera posición donde deberíamos insertar el valor para preservar el orden (el nuevo elemento que se inserta será el primero en aparecer dentro del rango), y upper_bound nos indicará la última posición donde deberíamos insertar el valor para preservar el orden (el nuevo elemento que se inserta será el último en aparecer dentro del rango).

Por otro lado, si queremos buscar un valor k = 6 que no existe dentro del siguiente arreglo, tanto lower_bound como upper_bound nos regresarán el primer elemento v dentro del arreglo donde k < v.

           lower_bound
                v

2 3 4 4 5 5 5 5 7 8
^
upper_bound

               lower_bound
                    v

2 3 4 4 5 5 5 5 7 8 \_
^
upper_bound

Internamente, lower_bound y upper_bound implementan la búsqueda binaria. Dependiendo de qué queramos lograr, estas funciones pueden ayudarnos a encontrar un valor o la posición donde debería insertarse un valor para preserver el orden.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <iterator>
#include <vector>
#include <algorithm>

void showIndexes (
    std::vector<int>::iterator begin,
    std::vector<int>::iterator lower,
    std::vector<int>::iterator upper
) {
    std::cout << "\nEl índice de `lower_bound` es: " << std::distance(begin, lower);
    std::cout << "\nEl índice de `upper_bound` es: " << std::distance(begin, upper) << "\n";
}

int main() {
    std::vector<int> vec = {2, 4, 4, 4, 5, 7, 9};
    //                      ^  ^  ^  ^  ^  ^  ^
    //             Índices: 0  1  2  3  4  5  6


    // RANGO DE ELEMENTOS
    auto lower = std::lower_bound(vec.begin(), vec.end(), 4);
    auto upper = std::upper_bound(vec.begin(), vec.end(), 4);

    std::cout << "Dentro del vector, hay " << std::distance(lower, upper) << " elementos iguales a 4";
    std::cout << "\nRango que contiene todos los `4`: ";
    for (auto it = lower; it != upper; it++) {
        std::cout << *it << " ";
    }
    showIndexes(vec.begin(), lower, upper);


    // ELEMENTO `last`
    lower = std::lower_bound(vec.begin(), vec.end(), 100);
    upper = std::upper_bound(vec.begin(), vec.end(), 100);

    if(lower == vec.end()) {
        std::cout << "\nNo hay ningún 100 dentro del vector y todos los elementos del vector son menores a 100";
    }
    showIndexes(vec.begin(), lower, upper);

    // INSERTAR ELEMENTO
    lower = std::lower_bound(vec.begin(), vec.end(), 6);
    upper = std::upper_bound(vec.begin(), vec.end(), 6);

    if(lower != vec.end() && *lower != 6) {
        std::cout << "\nNo hay ningún 6 dentro del vector, pero podemos insertar uno en `lower_bound`";
    }
    showIndexes(vec.begin(), lower, upper);

    vec.insert(lower, 6);
    lower = std::lower_bound(vec.begin(), vec.end(), 6);
    upper = std::upper_bound(vec.begin(), vec.end(), 6);

    if(lower != vec.end() && *lower == 6) {
        std::cout << "\nHay al menos un 6 dentro del vector: ";
        std::copy(vec.begin(), vec.end(), std::ostream_iterator<int>(std::cout, ", "));
    }
    showIndexes(vec.begin(), lower, upper);

    return 0;
}
```
