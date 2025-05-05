# Cero, positivo o negativo

**Problema:**

Dado un número entero, determinar si es positivo, negativo o cero.

**Consideraciones:**

- El programa debe leer un número entero.
- Usar if-else para determinar si el número es positivo, negativo o cero.
- Imprimir el resultado correspondiente.
- Imprimir la palabra en mayusculas "POSITIVO" "CERO" "NEGATIVO"

### Ejemplo:

Entrada: -5

Salida: NEGATIVO

Entrada:0

Salida:CERO

Entrada:5

Salida:POSITIVO

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación o preguntale a tu profesor.

```
#include<bits/stdc++.h>
using namespace std;

int main() {

    int n;
    cin >> n;

    if(n > 0){
        cout << "POSITIVO";
    } else if (n < 0){
        cout << "NEGATIVO";
    } else {
        cout << "CERO";
    }

    return 0;
}
```
