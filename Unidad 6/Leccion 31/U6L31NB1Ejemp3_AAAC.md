# Doble Producto

Código del problema: U6L31NB1Ejemp3_AAAC

**Problema:**

Recibiras un entero N y despues una lista de N numeros, deberas crear un programa que lea estos valores e imprima el doble producto de cada numero de la lista.

**Consideraciones:**

- N es un numero entero (no tiene decimal).
- Doble producto de un numero es dicho numero multiplicado por 2.
- Al imprimir el doble producto de cada numero, debes dejar un espacio entre cada uno.

A continuacion puedes ver el codigo del programa que deberas probar en el compilador Codeblocks. Todas las lineas que comiencen con 2 o 3 diagonales (///), o esten dentro de el simbolo (/_ comentario _/) son comentarios para explicar cada instruccion del programa y facilitar su comprension.

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

### Ejemplo:

**Entrada:**

4

8 1 3 5

**Salida:**

16 2 6 10

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include<bits/stdc++.h>
using namespace std;

//Autor: Arturo Alejandro Arellano Cruz

int main(){

  //Empezamos declarando las variables que usaremos
  int N, Res;
  cin>>N; //Leemos N

    ///La función for repetirá un conjunto de instrucciones:
    ///En el primer parámetro se incializan las variables locales del for
    ///En el segundo parámetro se colocará la condición que debe cumplirse para que las instrucciones que están dentro del for se sigan repitiendo.
    ///En el tercer parámetro se coloca la instrucción que se ejecutará al finalizar las instrucciones que están dentro del for en cada iteración.

    for( int i = 0 ; i < N ; i ++){
        //Como se van a leer N numeros de la lista, los leeremos dentro de la funcion for

        cin>>Res; //Leemos el numero actual de la lista

        Res = Res * 2; //Sacamos el doble producto del numero actual, se guarda en Res

        cout<<Res<<" "; //Imprimimos el resultado seguido de un espacio

    }

}
```
