# Par o Impar

Código del problema: U6L31NB1Ejemp4_AAAC

**Problema:**

Recibiras un entero N y despues una lista de N numeros, deberas crear un programa que lea estos numeros y, para cada uno de ellos, imprima "PAR" o "IMPAR" dependiendo de la paridad del numero.

**Consideraciones:**

- N es un numero entero (no tiene decimal).
- La paridad de un numero se determina checando si es divisible entre 2 o no.
- Si el numero es par, imprime "PAR"; si el numero es impar, imprime "IMPAR".

A continuacion puedes ver el codigo del programa que deberas probar en el compilador Codeblocks. Todas las lineas que comiencen con 2 o 3 diagonales (///), o esten dentro de el simbolo (/_ comentario _/) son comentarios para explicar cada instruccion del programa y facilitar su comprension.

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

### Ejemplo:

**Entrada:**

5

10 5 8 6 7

**Salida:**

PAR

IMPAR

PAR

PAR

IMPAR

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include<bits/stdc++.h>
using namespace std;

 //Autor: Arturo Alejandro Arellano Cruz

int main(){

 //Declaramos las variables que usaremos
 int N,Num;
 cin>>N; //Leemos N

 /*
 Este apartado se usara para explicar algunos elementos y funciones basicas importantes.
 Primero el operador %, este operados saca el modulo de un numero en base a otro numero.
 Que es el modulo? En pocas palabras, es el residuo de una division.

 Ej.
 7 entre 2 es 3 y el residuo es 1
 12 entre 5 es 2 y el residuo es 2
 9 entre 3 es 3 y el residuo es 0

 Entonces si nos enfocamos en el primer ejemplo y escribimos:
 Variable = 7 % 2;
 "Variable" guardara el valor 1

 Siguiente, la sentencia if-else; esta sentencia checa si una condicion se cumple; si cumple, ejecutara las lineas dentro del if;
 en caso contrario, ejecutara las lineas dentro del else.

 Su estructura es la que sigue:
    if(condicion){
       codigo que se ejecuta si cumple la condicion
    }
    else{
       codigo que se ejecuta si no cumple la condicion
    }

 Finalmente, queda checar el operador de igualdad ==; este operador se usa en una condicion para checar si dos valores son iguales:
 A==B checa si el valor de A es igual al valor de B

 Todo esto se muestra para poder explicar como resolver este problema.

 Usaremos la sentencia if para checar la paridad del numero leido, entonces la condicion preguntara si es par de la siguiente formar:
 Num % 2 == 0

 Esta condicion pregunta si Num % 2 (o el residuo de Num entre 2) es igual a 0.
 Si cumple, eso significa que Num es divisible entre 2, en consecuencia, es par.
 Pero si NO cumple, Num no es divisible entre 2, entonces es impar.
 */

 for(int i = 0 ; i < N ; i++){
    ///Leemos Num
    cin>>Num;

    ///Preguntamos si Num es par
    if(Num % 2 == 0){ //Si cumple, imprime PAR
        cout<<"PAR\n";
    }
    else{ //Si no, imprime IMPAR
        cout<<"IMPAR\n"; //El "\n" representa lo que es presionar ENTER en un documento word, util para mantener la salida mas organizada
    }

 }

}
```
