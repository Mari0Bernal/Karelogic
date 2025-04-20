# Ejercicio #1 Reparto Equitativo (succ, pred, iszero)(U4L14NB1Ejercc2_GRB)

Código del ejercicio: U4L14NB1Ejercc2_GRB

Karel se encuentra con direccion desconocida, encima de un numero no conocido de objetos trompo (beepers), en la esquina de mas al surOeste de un rectangulo de dimensiones que tampoco se conoce. Karel esta empeñado en tapizar todo el rectangulo de un mismo numero de n trompos en cada una de las k celdas internas del rectangulo.

### Problema

Ayuda a Karel a lograr su objetivo, de dejar el mismo numero n de trompos en cada una de las k celdas del rectangulo. (Ver ejemplo)

## Ejemplo de un posible mundo:

Entrada

![L14Ej1ME.png](L14Ej1ME.png?raw=true)

Salida

![L14Ej1MS.png](L14Ej1MS.png?raw=true)

### Consideraciones

- La cantidad de trompos que hay donde inicia Karel su tarea son nk (n: cantidad de trompos que debera haber finalmente en cada una de las k celdas dentro del rectangulo, y k: cantidad total de celdas dentro del rectangulo).
- Karel inicia con direccion desconocida, encima de un numero no conocido de objetos trompo (nk)(beepers), y en la esquina de mas al surOeste dentro de un rectangulo.
- No se conoce las dimensiones del rectangulo.
- Karel debe terminar en la esquina al suroeste del rectangulo orientado al norte.
- La mochila de Karel tiene infinitos trompos.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void girar(g){
        iterate(g) turnleft();
    }

    void contar(c){
        if(nextToABeeper()) {
            pickbeeper();
            contar(succ(c));
        }
        else {
            dejar(c);
        }
    }

    void dejar(d){
        if(!iszero(d)) {
            if(frontIsClear()) {
                putbeeper();
                move();
                dejar(pred(d));
            }
            else {
                if(leftIsBlocked()) {
                    putbeeper();
                    girar(2);
                    while(frontIsClear()) move();
                    turnleft();
                    move();
                    turnleft();
                    dejar(pred(d));
                }
                else {
                    if(rightIsBlocked()) {
                        putbeeper();
                        girar(2);
                        while(frontIsClear()) move();
                        girar(3);
                        while(frontIsClear()) move();
                        girar(3);
                        dejar(pred(d));
                    }
                    else {
                        putbeeper();
                        girar(2);
                        while(frontIsClear()) move();
                        turnleft();
                        move();
                        turnleft();
                        dejar(pred(d));
                    }
                }
            }
        }
        else {
             if(notFacingNorth()) {
                  turnleft();
             }
        }
    }
    program () {
        // TODO poner codigo aqui
        contar(0);
        turnoff();
    }
}
```
