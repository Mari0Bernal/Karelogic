Código del problema: U5EjDiagSem3p3

**Descripción del problema:**

Leer un valor "n" maximo de 10k elementos, luego leer n parejas de datos numericos enteros. De cada pareja el mayor se almacenará en un vector, despues de este proceso iniciar otro para obtener la lista de valores del vector que sean mayores al promedio del mismo. La lista de resultados deberá aparecer en una sola linea, cada una separada por un espacio.

**Datos de entrada de ejemplo:**

5

10 20

20 10

5 10

10 5

10 20

**Datos de salida de ejemplo:**

20 20 20

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <vector>

using namespace std;

int main(){

    int n;
    cin >> n;

    if( n <= 0 || n > 10000){
        cout << "Favor de insertar un valor menor de 10000 o mayor a 0";
        return 1;
    }
    vector<int> mayores;

    for(int i=0; i < n; i++){
        int a, b;
        cin >> a >> b;
        mayores.push_back(max(a,b));
    }

    double suma = 0;
    for (int num=0; num < mayores.size(); num++) {
        suma += mayores[num];
    }
    double promedio = suma / n;

    for(int i=0; i < mayores.size(); i++){
        if(mayores[i] > promedio){
            cout << mayores[i] << " ";
        }
    }

	return 0;
}
```
