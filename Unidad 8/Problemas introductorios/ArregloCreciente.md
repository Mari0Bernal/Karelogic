# Arreglo Creciente

Se te da un arreglo de N enteros. Quieres modificar el arreglo de tal manera que este sea un arreglo creciente, que consiste en que todo elemento es mayor o igual a su anterior. En cada movimiento puedes sumarle 1 a un elemento del arreglo. ¿Entonces, cual es el menor numero de movimientos necesarios para volver el arreglo creciente?

### Entrada

La primera linea contiene un entero N, el tamaño del arreglo.

La segunda linea contiene los N enteros del arreglo: x1, x2, x3, ... , xN.

### Salida

Imprime el menor numero de movimientos necesario.

**Restricciones**

- 1 ≤ N ≤ 2⋅10^5
- xi es un entero positivo menor a 10^9

**Ejemplo**

Entrada:

5

3 2 5 1 7

Salida:

5

**Explicacion**

Este problema es simplificado por las restricciones de los movimientos, despues de todo, solo puedes sumarle 1 a un elemento en cada movimiento.

Para obtener el arreglo creciente, podemos hacer un recorrido y comparar cada elemento con el anterior a este, y si el anterior es mayor al elemento actual, sumarle 1 al elemento actual hasta que sea igual al elemento anterior.

Repetiremos esto con cada elemento mientras usamos un entero especificamente para contar los movimientos; cuando terminemos con todo el arreglo, tendremos no solo un arreglo creciente, pero tambien un entero que contiene el numero de movimientos que buscamos.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
/// Codigo de Arturo Alejandro Arellano Cruz

#include<bits/stdc++.h>
using namespace std;

 const int Maxn=(2*1e5)+5; ///Constante para establecer el tamanio del arreglo siguiente

 long long Arr[Maxn]; ///Arreglo

int main(){

 long long N; ///Entero de la entrada
 cin>>N; ///Leemos N
 long long i,Ans=0; ///Usaremos i para recorrer el arreglo y Ans como el contador de movimientos

 for(i=0;i<N;i++)cin>>Arr[i]; ///Leemos el arreglo

 for(i=1;i<N;i++){ ///Comencemos el recorrido
   if(Arr[i]<Arr[i-1]){ ///Si el actual es menor al elemento anterior
    Ans+=(Arr[i-1]-Arr[i]); ///Para no contar de 1 en 1, sumamos los movimientos necesarios para que el elemento actual sea igual al anterior
    Arr[i]+=(Arr[i-1]-Arr[i]); ///Igualamos el elemento actual al anterior
   }
 }

 cout<<Ans; ///Imprimimos Ans
}
```
