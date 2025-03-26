# Problema 4: Pasillo Estrecho

Codigo del problema: U4L15Ejer_AAAC

### Descripción

Karel esta en el inicio de un pasillo de ancho 1, tiene como idea llegar el final del pasillo tomando en cuenta la cantidad de veces que giro a la izquierda y derecha.

Terminando de recorrer el pasillo hara lo siguiente:

- Pondra un monton de beepers que equivale a la cantidad de veces que giro a la izquierda
- Dara un giro a la izquierda por cada vez que giro a la derecha recorriendo el pasillo

## Mundo de Entrada

![L15-P4-ME.png](L15-P4-ME.png?raw=true)

## Mundo de Salida

![L15-P4-MS.png](L15-P4-MS.png?raw=true)

### Consideraciones

- Karel tiene infinitos trompos en la mochila
- Importa la orientacion de Karel y los beepers que deje al final del pasillo

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
class program {

    void recursion(){
        if(frontIsClear()) {
            move();
            recursion();
        }
        else {
            if(leftIsClear()) {
                turnleft();
                recursion();
                putbeeper();
            }
            else {
                if(rightIsClear()) {
                    iterate(3) turnleft();
                    recursion();
                    turnleft();
                }
            }
        }
    }
    program () {
        // TODO poner codigo aqui
        recursion();
        turnoff();
    }
}
```
