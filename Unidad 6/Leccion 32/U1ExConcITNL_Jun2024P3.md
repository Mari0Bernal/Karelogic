# Sumatorio de Duplas

Código del ejercicio: U1ExConcITNL_Jun2024P3

**Problema:**

Dadas N parejas de enteros (a,b). Calcular, de cada pareja, a+b y ademas, la sumatoria de todas las sumas.

El programa debera leer n parejas de dos enteros a y b e imprimir el resultado de la suma de cada pareja, acumularla y mostrar, al final, el acumulado de todas las sumas de parejas.

**Consideraciones:**

- a y b son enteros sin signo (valores numericos sin decimales).
- 0 < N < 128
- Utilizar el estatuto de asignacion (=) para asignar a una variable el valor correspondiente.
- Mostrar en la pantalla del usuario los datos solicitados.

### Ejemplo:

**Entrada:**

2

2 3

4 5

**Salida:**

5

9

14

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación o preguntale a tu profesor.

```
#include <bits/stdc++.h>
#include <new>
using namespace std;

int main(){

    int N;
    cin >> N;
    if(N < 0 || N > 128){
        cout << "Favor de colocar un numero entre 0 y 128";
        return 0;
    }

    int a[N], b[N], sumaP[N], suma = 0;

    for(int i=0; i < N; i++){
        cin >> a[i] >> b[i];
        sumaP[i] = a[i] + b [i];
        cout << sumaP[i] << "\n";
        suma += sumaP[i];
    }

    cout << suma;
	return 0;
}
```
