# Numero Perdido

Te dan todos los numeros de 1 a N, a excepcion de uno de ellos. Encuentra el numero restante.

### Entrada

La primera linea contiene un entero N.

La segunda linea contiene N - 1 numeros. Cada numero es distinto y tienen un valor entre 1 y N (inclusive).

### Salida

Imprime el numero faltante.

**Restricciones**

2 ≤ N ≤ 2⋅10^5

**Ejemplo**

Entrada:

5

2 3 1 5

Salida:

4

**Explicacion**

Queremos encontrar el numero que falta dentro del arreglo de numeros que nos dan, esto no es dificil de hacer.

Basta con usar una cubeta (otro arreglo donde cada posicion del arreglo representa una cubeta), lo que haremos aqui es lo siguiente:

- Recorremos el arreglo principal
- Para un i en el arreglo, marcaremos la cubeta con la posicion i con 1
- Despues recorremos la cubeta, si encontramos una cubeta con un 0, significa que no pasamos por ese numero en el arreglo principal.

De esta forma encontramos el numero perdido.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
///Codigo de Arturo Alejandro Arellano Cruz

#include<bits/stdc++.h>
using namespace std;

 const int Maxn = (2*1e5) + 5; ///Constante que define el tamanio del arreglo a continuacion

 int Cub[Maxn]; ///Este sera nuestro arreglo cubeta

int main(){

 int N,i; ///Entero de entrada y otro entero que se usara para la funcion for
 cin>>N; ///Leemos N
 int Num; ///Otro entero que usaremos para leer la entrada

 for(i=1;i<N;i++){ ///for para leer el arreglo principal
   cin>>Num; ///Leemos Num
    Cub[Num]=1; ///Obteniendo Num en el arreglo principal, marcamos su respectiva cubeta con 1
 }

 for(i=1;i<=N;i++){ ///Recorremos el arreglo cubeta
   if(Cub[i]==0){ ///Si la cubeta i es igual a 0, entonces ese numero no estaba en el arreglo principal, entonces i es nuestro numero perdido
     cout<<i; ///Imprimimos i
     return 0; ///Termina ejecucion
   }
 }


}
```
