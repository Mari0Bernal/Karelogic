# (U6 L34 problema2)

Código del problema: U6L34 Ejcc

**Descripción del problema:**

Leer un valor "n" maximo de 10k elementos, luego leer n datos numericos enteros, se asegura que los datos leidos ya estan ordenados de menor as mayor. Despues, mientras no sea leido un valor negativo, el programa debera estar leyendo datos numericos, por cada dato leido deberan mostrar, en una nueva linea, todos los datos del vector pero ya insertado el nuevo dato leido en el lugar que le corresponde para que el vector siga ordenado de menor a mayor, en una misma linea (cada dato separado por un espacio).

**Datos de entrada de ejemplo:**

5

10 20 30 40 50

70 14 -1

**Datos de salida de ejemplo:**

10 20 30 40 50 70

10 14 20 30 40 50 70

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

int main( ){

    int n;
    cin >> n;
    if(n <= 0 || n > 10000){
        cout << "Error";
        return 1;
    }

    vector<int> datos(n);
    for (int i = 0; i < n; ++i) {
        cin >> datos[i];
    }

    int nuevo;
    while (cin >> nuevo && nuevo >= 0) {
        // Insertar en orden usando lower_bound
        auto pos = lower_bound(datos.begin(), datos.end(), nuevo);
        datos.insert(pos, nuevo);

        // Imprimir vector actualizado
        for (int val : datos) {
            cout << val << " ";
        }
        cout << endl;
    }

    return 0;
}
```
