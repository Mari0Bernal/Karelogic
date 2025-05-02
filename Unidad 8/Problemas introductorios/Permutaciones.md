# Permutaciones

Una permutacion con los numeros 1,2,...,N se llama bello siempre y cuando no haya dos numeros adyacentes tal que su diferencia sea 1.

Dado N, imprime una permutacion bella si dicha permutacion existe.

### Entrada

Una sola linea con el entero N.

### Salida

Imprime una permutacion bella, si hay varias, puedes imprimir cualquiera de ellas. En caso de no existir, imprime "NO HAY SOLUCION" sin las comillas.

**Restricciones**

- 1 ≤ N ≤ 10^6

**Ejemplo**

Entrada:

5

Salida:

4 2 5 3 1

Entrada:

3

Salida:

NO HAY SOLUCION

**Explicacion**

Es sencillo de construir permutaciones bellas para casi cualquier valor de N, solo basta con como hacerlo e identificar los casos particulares donde no es factible.

De las varias formas que una permutacion bella se puede construir, una de las mas simples consiste en separar los numeros en 2 grupos: uno para numeros pares y otro para numeros impares. Ambos grupos se ordenan en una lista de menor a mayor y despues, se concatenan ambas listas.

Por ejemplo, digamos que N es 7, entonces se separan los numeros en los grupos [2,4,6] y [1,3,5,7], se ordenan en listas de menor a mayor (ya se muestran en orden) y se concatenan para formar [2,4,6,1,3,5,7].

Siguiendo este metodo encontramos existe una permutacion bella para cualquier valor de N a excepcion de N siendo igual a 2 o 3, porque?

Para N = 2, el 1 y 2 quedan lado a lado sin importar que hagas, y la diferencia entre ellas es 1, entonces no hay permutacion bella.

Para N = 3, el 2 es el problema, ya que quedara lado a lado con el 1 o el 3, donde su diferencia es 1, concluyendo que no hay permutacion bella.

Que hay sobre N = 1? Bueno, pues resulta que el 1 solo es permutacion bella porque cumple con las restricciones de una permutacion bella a pesar de estar por si solo, no hay dos numeros adyacentes tal que su diferencia sea 1.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
///Codigo de Arturo Alejandro Arellano Cruz

#include<bits/stdc++.h>
using namespace std;

int main(){

 int N; ///Entero de la entrada
 cin>>N; ///Leemos el valor de N

 if(N==1) ///La permutacion solo tendra el 1, asi que sera una permutacion bella
    cout<<"1"; ///Se imprime el 1 en este caso
 else if(N<=3) ///Aqui cubren los casos donde N es 2 o 3, por razones previamente mencionadas,
               ///estos casos no tienen solucion
    cout<<"NO HAY SOLUCION"; ///Entonces se imprime lo siguiente
 else{ ///Llegamos a este "else" si N es 4 o mayor, para el cual tendremos que construir una permutacion bella
    int i; ///Declaramos i
      for(i=2;i<=N;i+=2) ///Empezaremos imprimiendo los numeros pares de menor a mayor
        cout<<i<<" ";
      for(i=1;i<=N;i+=2) ///Despues, imprimimos los numeros impares de menor a mayor
        cout<<i<<" ";
 }
}
```
