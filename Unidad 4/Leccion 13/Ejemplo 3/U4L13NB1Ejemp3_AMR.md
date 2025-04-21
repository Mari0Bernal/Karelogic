# Ejemplo 3 Recursividad (U4L13NB1Ejemp3_AMR)

Codigo del ejemplo: U4L13NB1Ejemp3_AMR

Karel quiere medir la distancia a la pared que se encuentra en frente de él.

### Problema

Tu tarea es medir la distancia a la pared, y dejar este número del otro lado de la misma.

## Mundo de Entrada

![L13E3ME.png](L13E3ME.png?raw=true)

## Mundo de Salida

![L13E3MS.png](L13E3MS.png?raw=true)

### Consideraciones

- Karel lleva infinitos trompos en la mochila.
- Karel deberá dejar la distancia del lado derecho de la pared.

### Explicación

Creamos la función mide, la cual, mediante el if de la línea 3, avanza hasta encontrar una pared, dejando a la vez pendiente el putbeeper(); de la línea 6.

Cuando Karel llega a la pared, entra al else de la función, se posiciona al otro lado del muro, y atiende las llamadas pendientes (putbeeper).

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void mide(){
        if(frontIsClear){   //mientras el frente
            move();         // está libre
            mide();
            putbeeper();    //llamada pendiente
        }
        else {              //brinca la barda
            turnleft();
            move();
            iterate(3){
                turnleft();
            }
            move();
            iterate(3){
                turnleft();
            }
            move();
        }
    }
    program () {
        mide();         //llamamos a la función
        turnoff();
    }
}
```
