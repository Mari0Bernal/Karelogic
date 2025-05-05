# Signo del producto

**Problema:**

El programa debe leer 2 números los cuales debe calcular el valor del signo que da el producto de ambos

**Consideraciones:**

- El programa debe leer dos números enteros.
- Usar if-else para determinar el signo del producto sin calcularlo directamente:
  - Si ambos números son positivos o ambos son negativos, el producto es positivo.
  - Si un número es positivo y el otro negativo, el producto es negativo.
  - Si al menos uno de los números es cero, el producto es cero.
- Imprimir "POSITIVO", "NEGATIVO" o "CERO", según corresponda.

### Ejemplo

Entrada: 2 0

Salida: CERO

Entrada: 2 1

Salida: POSITIVO

Entrada: 2 -1

Salida: NEGATIVO

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación o preguntale a tu profesor.

```
#include<bits/stdc++.h>
using namespace std;

int main() {

    int a, b;
    cin >> a >> b;

    if(a == 0 || b == 0){
        cout << "CERO";
    } else if(a > 0 && b > 0 || (a < 0 && b < 0)){
        cout << "POSITIVO";
    } else {
        cout << "NEGATIVO";
    }
    return 0;
}
```
