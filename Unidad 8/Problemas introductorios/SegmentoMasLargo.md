# Segmento mas largo de valores crecientes

Se te da un arreglo de N enteros. Se trata de obtener la lista mas larga de elementos con valores crecientes, es decir que en esa lista contiguos de elementos, cada dato es mayor a su anterior.

### Entrada

La primera linea contiene un entero N, el tamaño del arreglo.

La segunda linea contiene los N enteros del arreglo: x1, x2, x3, ... , xN.

### Salida

Imprime la lista mas larga de elementos con valores crecientes, es decir que en esa lista contiguos de elementos, cada dato es mayor a su anterior.

**Restricciones**

- 1 ≤ N ≤ 2⋅10^5
- xi es un entero positivo menor a 10^9

**Ejemplo**

Entrada:

5

3 2 5 1 7

Salida:

2 5

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <vector>
using namespace std;

int main() {
    int n;
    cin >> n;

    vector<int> array(n);
    for (int i = 0; i < n; ++i) {
        cin >> array[i];
    }

    int maxlen = 1, currentlen = 1;
    int startidx = 0, maxstartidx = 0;

    for (int i = 1; i < n; ++i) {
        if (array[i] > array[i - 1]) {
            currentlen++;
        } else {
            if (currentlen > maxlen) {
                maxlen = currentlen;
                maxstartidx = startidx;
            }
            currentlen = 1;
            startidx = i;
        }
    }

    // Verificar al final si la última secuencia es la más larga
    if (currentlen > maxlen) {
        maxlen = currentlen;
        maxstartidx = startidx;
    }

    for (int i = maxstartidx; i < maxstartidx + maxlen; ++i) {
        cout << array[i] << " ";
    }
    cout << endl;

    return 0;
}
```
