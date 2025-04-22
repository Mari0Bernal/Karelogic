# Ejemplo básico #1 de funciones o subprogramas (U3L10NB1Ejemp1_AMR)

Código de ejemplo: U3L10NB1Ejemp1_AMR

Karel quiere visitar a su abuela, cuya casa está representada por un trompo, pero quiere marcar el camino para no perderse de regreso.

### Problema

Algunas esquinas tienen paredes a la izquierda. Ayuda a Karel a marcar el camino, poniendo 5 trompos en las casillas que tienen paredes a la izquierda, y 7 trompos en las casillas que no. (Ver caso de ejemplo).

## Mundo de Entrada

![L10E1ME.png](L10E1ME.png?raw=true)

## Mundo de Salida

![L10E1MS.png](L10E1MS.png?raw=true)

### Consideraciones

- Karel inicia en algún lugar del mundo, orientado hacia la casa de su abuela.
- Karel tiene infinitos trompos en la mochila.
- Se evaluará la cantidad de trompos en cada casilla.
- No hay más trompos en el mundo además de la casa de su abuela.
- Karel deberá terminar en la posición donde se encuentre el trompo.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void funcion(){
        if(leftIsBlocked){  //Si la izquierda está
            iterate(5){     //  bloqueada
                putbeeper();
            }
        }
        else {              //Si la izquierda está
            iterate(7){     //  libre
                putbeeper();
            }
        }
    }
    program () {
        while(notNextToABeeper){  //Mientras no haya
            funcion();            // encontrado el trompo
            move();
        }
        turnoff();
    }
}
```
