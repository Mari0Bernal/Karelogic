# Repeticiones

Te dan una secuencia de ADN: una cadena que consiste de los caracteres 'A', 'C', 'G' Y 'T'. Tu tarea es encontrar la repeticion mas larga dentro de la cadena. Esta consiste en una subcadena del mayor tamaño posible en donde todos los caracteres son iguales.

### Entrada

Una sola linea que consiste de una cadena hecha de N caracteres.

### Salida

Un entero: la longitud de la repeticion mas larga

**Restricciones**

1 ≤ N ≤ 10^6

**Ejemplo**

Entrada:

ATTCGGGA

Salida:

3

**Explicacion**

Para este problema queremos encontrar la subcadena mas larga hecha de solo 1 tipo de caracter. Podemos obtener nuestra respuesta recorriendo la cadena.

Digamos que encontramos una 'T' en la posicion i y la posicion anterior no tiene 'T', entonces podemos checar la posicion i+1, y si tiene una 'T', podemos checar la posicion i+2 por otra 'T', luego la posicion i+3 y asi sucesivamente hasta que ya no encontremos una 'T' o hasta que lleguemos al final de la cadena.

Con esto sacamos la longitud de esa subcadena; entonces, con este proceso, podemos recorrer toda la cadena para obtener la longitud de todas las subcadenas candidatas y guardar unicamente el valor de la cadena mas larga.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
///Codigo de Arturo Alejandro Arellano Cruz

#include<bits/stdc++.h>
using namespace std;

int main(){

 string ADN; ///Cadena del problema
 cin>>ADN; ///Leemos la cadena
 int i; ///Entero para recorrer la cadena
 int Ans=0,Longi; ///Longi guardara la longitud de cada subcadena que vayamos pasando por, Ans guardara el valor mas grande que obtenga Longi

 i=0; ///Empezamos al inicio de la cadena

 while(i<ADN.size()){ ///Mientras no hayamos llegado al final de la cadena
   Longi=1; ///Inicializamos Longi en 1, puesto que estamos al inicio de una nueva subcadena
    i+=1; ///Vamos a la siguiente posicion
    while(ADN[i]==ADN[i-1]&& i < ADN.size()){ ///Mientras la posicion actual y la anterior son iguales, y aun no llegamos al final de la cadena
      Longi+=1; ///Aumentamos en 1 Longi
      i+=1; ///Pasamos a la siguiente posicion
    }
   ///Cuando el while se rompe, es debido a que la posicion actual y la anterior ya no son iguales (o por llegar al final de la cadena)
   Ans=max(Ans,Longi); ///Guardamos el valor mas grande entre Ans y Longi
 }

 cout<<Ans; ///Imprimimos Ans
}
```
