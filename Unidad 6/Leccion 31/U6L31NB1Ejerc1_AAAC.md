# Triple Producto mas Uno

Código del problema: U6L31NB1Ejerc1_AAAC

**Problema:**

Recibiras un entero N y despues una lista de N numeros, deberas crear un programa que lea estos valores e imprima el triple producto mas uno de cada numero de la lista.

**Consideraciones:**

- N es un numero entero (no tiene decimal).
- El triple producto de un numero es dicho numero multiplicado por 3.
- Al imprimir el resultado de cada numero, debes dejar un espacio entre cada uno.

### Ejemplo:

**Entrada:**

4

5 3 6 1

**Salida:**

16 10 19 4

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include<bits/stdc++.h>
using namespace std;

int main(){

 int N;
 cin>>N; //Leemos N
 int lista[N];

 for(int i=0; i < N; i++){
     cin >> lista[i];
     cout << (lista[i] * 3) + 1 << " ";
 }

 /*
 for(int i=0; i < N; i++){
     cout << (lista[i] * 3) + 1 << " ";
 }
*/


 return 0;
}
```
