# (U6 Lcc34 EjerccDiag problema3)

Código del problema: U6Lcc34Ejcc3

**Descripción del problema:**

Leer un valor "n" maximo de 10k elementos, luego leer n datos numericos enteros. Despues de leer todos los datos del vector, el programa debera leer un valor k numerico entero. El problema a resolver es mostrar al usuario , en una misma linea (cada dato separado por un espacio), solamente los valores que sean pares y que sean mayores al valor k. Y ademas mostrar, en una nueva linea, el promedio de todos los valores mostrados.

Se asegura que siempre habra al menos un valor par mayor a k.

El promedio se debe redondear eliminando las decimales

**Datos de entrada de ejemplo:**

5

10 20 30 40 80

25

**Datos de salida de ejemplo:**

30 40 80

50

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>
#include <vector>

using namespace std;

int main(){

    int n, k;
    // Leer el valor de n
    cin >> n;
    if(n <= 0 || n > 10000){
        cout << "Error";
        return 1;
    }

    // Crear y leer el vector de n elementos
    vector<int> numeros(n);
    for (int i = 0; i < n; i++) {
        cin >> numeros[i];
    }

    // Leer el valor de k
    cin >> k;

    // Mostrar números pares mayores que k
    vector<int> paresYMayores;
    for(int i=0; i < n; i++){
        if(numeros[i] % 2 == 0 && numeros[i] > k){
            cout << numeros[i] << " ";
            paresYMayores.push_back(numeros[i]);
        }
    }

    cout << endl;

    // Calcular y mostrar el promedio
    int suma = 0;
    for (int num : paresYMayores) {
        suma += num;
    }
    int promedio = suma / paresYMayores.size();
    cout << promedio << endl;

    return 0;
}
```
