# Ejemplo básico #3 de funciones o subprogramas (U3L10NB1Ejemp3_AMR)

Codigo de ejemplo: U3L10NB1Ejemp3_AMR

Karel se encuentra en su casa, que es rectangular, y quiere pintar las paredes, pero de diferentes colores.

### Problema

Ayuda a Karel a pintar las paredes, poniendo 8 trompos en las paredes horizontales, y 5 trompos en las paredes verticales, como se muestra en el ejemplo.

## Mundo de Entrada

![L10E3ME.png](L10E3ME.png?raw=true)

## Mundo de Salida

![L10E3MS.png](L10E3MS.png?raw=true)

### Consideraciones

- Karel inicia en la esquina inferior izquierda del rectángulo, orientado hacia el este.
- Las esquinas deberán quedar vacías.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void funcion(){
        while(frontIsClear){
            if(facingNorth||facingSouth){ //identifica si la
                iterate(5)putbeeper();    // pared es vertical
            }
            if(facingEast||facingWest){   //identifica si la
                iterate(8)putbeeper();    // pared es horizontal
            }
            move();
        }
    }
    program () {
        iterate(4){      //se repite 4 veces,
            move();      // para las 4 paredes
            funcion();
            turnleft();
        }
        turnoff();
    }
}
```
