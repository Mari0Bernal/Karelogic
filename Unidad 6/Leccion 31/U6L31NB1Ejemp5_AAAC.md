# Par o Impar contados

Código del problema: U6L31NB1Ejemp5_AAAC

**Problema:**

Recibiras un entero N y despues una lista de N numeros, deberas crear un programa que lea estos numeros y, para cada uno de ellos, imprima "PAR" o "IMPAR" dependiendo de la paridad del numero. Al final, imprimiras la cantidad de pares que hay en la lista.

**Consideraciones:**

- N es un numero entero (no tiene decimal).
- La paridad de un numero se determina checando si es divisible entre 2 o no.
- Si el numero es par, imprime "PAR"; si el numero es impar, imprime "IMPAR"

A continuacion puedes ver el codigo del programa que deberas probar en el compilador Codeblocks. Todas las lineas que comiencen con 2 o 3 diagonales (///), o esten dentro de el simbolo (/_ comentario _/) son comentarios para explicar cada instruccion del programa y facilitar su comprension.

Te pedimos compilar y luego probar el programa con diferentes datos en la plataforma de Codeblocks.

### Ejemplo:

**Entrada:**

5

10 5 8 6 7

**Salida:**

Salida

PAR

IMPAR

PAR

PAR

IMPAR

3

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include<bits/stdc++.h>
using namespace std;

 //Autor: Arturo Alejandro Arellano Cruz

int main(){

 //En esta ocasion se nos pide contar la cantidad de pares en la lista, para eso ocuparemos una variable que se encargue de esto
 //Declaramos las variables que usaremos
 int N,Num,Cont;
 cin>>N; //Leemos N
 Cont=0; //Inicializamos Cont en 0


 for(int i = 0 ; i < N ; i++){
    ///Leemos Num
    cin>>Num;

    ///Preguntamos si Num es par
    if(Num % 2 == 0){ //Si cumple, imprime PAR
        Cont = Cont + 1; //Encontramos un par, entonces se suma 1 a Cont
        cout<<"PAR\n";
    }
    else{ //Si no, imprime IMPAR
        cout<<"IMPAR\n";
    }

 }
 cout<<Cont; //Imprimimos Cont ahora que ya tiene guardado la cantidad de pares que hay en la lista
}
```
