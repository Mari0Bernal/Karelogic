# Tipo de cuadrado

**Problema:**

El programa deber leer 4 numeros y de los cuales determina si es posible armar un rectangulo, un cuadrado o nada

**Consideraciones:**

- El programa debe leer cuatro enteros positivos que representan los lados de la figura.
- Usar if-else para verificar el tipo de figura:
  - Es un cuadrado si los cuatro lados son iguales.
  - Es un rectángulo si los lados opuestos son iguales.
  - No es ninguna de las anteriores si no cumple las condiciones previas.
- Imprimir "CUADRADO" si la figura es un cuadrado, "RECTANGULO" si es un rectángulo, o "NADA" si no es ninguna de ellas.

### Ejemplo

Entrada:2 4 2 4

Salida:RECTANGULO

Entrada: 2 2 2 2

Salida:CUADRADO

Entrada:1 2 3 4

Salida:NADA

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación o preguntale a tu profesor.

```
#include<bits/stdc++.h>
using namespace std;

int main() {

    int a,b,c,d;
    cin >> a >> b >> c >> d;

    if(a == c && b == d && a != b){
        cout << "RECTANGULO";
    } else if(a == c && b == d && a == b){
        cout << "CUADRADO";
    } else {
        cout << "NADA";
    }
    return 0;
}
```
