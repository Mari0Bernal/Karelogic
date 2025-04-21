# Ejemplo 1 (Recursividad) avanza n cuadras (U4L13NB1Ejemp1_GRB)

Codigo del ejemplo: U4L13NB1Ejemp1_GRB

Karel inicia con direccion al norte, encima de un numero no conocido de objetos trompo o beeper.

### Problema

Ayudale a Karel a que avance tantas cuadras como trompos tenga debajo de el, ahi donde inicia su tarea. Es decir, que por ejemplo, si hay cinco trompos en la cuadra donde inicia Karel su terea, entonces debera avanzar cinco cuadras al norte y ahi apagarse.

## Mundo de Entrada

![L13E1ME.png](L13E1ME.png?raw=true)

## Mundo de Salida

![L13E1MS.png](L13E1MS.png?raw=true)

### Consideraciones

- Karel inicia con direccion al norte, en algun punto dentro de su mundo.
- Karel inicia con un numero infinito de trompos dentro de su mochila.
- Karel debe terminar con direccion al norte.

### Explicación

Mientras Karel, este encima de al menos un trompo, estara llamando recursivamente a la funcion "levantaYAvanza()". Por cada llamada a la funcion recursiva, Karel carga a su memoria una nueva copia de esa funcion recursiva, y suceden dos cosas:

1.- Inicia desde el principio, el proceso de ejecutar cada nueva copia que carga a su memoria.

2.- Deja pendiente de terminar de procesar cada nueva copia, desde donde ocurrio la llamada a funcion recursiva. Pero Karel se va a a acordar en donde se quedo pendiente de terminar de procesar cada una de las copias de la funcion recursiva.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void levantaYAvanza(){
         if(nextToABeeper){
              pickbeeper();
              levantaYAvanza();
              move();
         }
    }
    program () {
        levantaYAvanza();
        turnoff();
    }
}
```
