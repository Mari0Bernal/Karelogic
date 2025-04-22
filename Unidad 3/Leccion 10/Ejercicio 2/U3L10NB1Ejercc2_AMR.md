# Ejercicio básico de funciones o subprogramas #2 (U3L10NB1Ejercc2_AMR)

Codigo del ejercicio: U3L10NB1Ejercc2_AMR

Karel se encuentra en el polo norte, ayudando a Santa Claus a fabricar juguetes; pero en su tiempo libre le gusta salir a pescar en el hielo, y para esto hizo algunos agujeros en el piso. Karel quiere saber cuánta carnada comprar, pero para esto necesita saber cuántos peces hay en los agujeros que cavó.

### Problema

Ayuda a Karel a checar en cada pozo si hay peces, representados por montones de 3 o más trompos, y debes dejar en la posición inicial cuántos agujeros tenían peces en ellos.

## Mundo de Entrada

![L10Ej2ME.png](L10Ej2ME.png?raw=true)

## Mundo de Salida

![L10Ej2MS.png](L10Ej2MS.png?raw=true)

### Consideraciones

- No se conoce la profundidad de cada pozo.
- Los pozos comienzan en la casilla siguiente a donde inicia Karel.
- No se conoce la profundidad de cada pozo.
- Karel inicia orientado hacia el este.
- Karel no lleva trompos en la mochila.
- Deberás utilizar al menos una función.

### Tips

- Solo se evalúa la cantidad final de trompos en la casilla inicial de Karel.
- Recuerda que puedes dejar trompos en el mundo.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void girar(a){
        iterate(a) {
            turnleft();
        }
    }

    void pozo(){
        while(frontIsClear()) {
            move();
            if(nextToABeeper()) {
                pickbeeper();
                if(nextToABeeper()) {
                    pickbeeper();
                    if(nextToABeeper()) {
                        while(nextToABeeper()) {
                            pickbeeper();
                        }
                        girar(2);
                        while(leftIsBlocked()) {
                            move();
                        }
                        putbeeper();
                        girar(2);
                    } //3er if
                }//2nd if
            }//Termian 1er if
        }//Termina whi
        girar(2);
        while(leftIsBlocked()) {
            move();
        }
        girar(3);
    }

    void irFrenteYGirar2(){
        girar(2);
        while(frontIsClear()) {
            move();
        }
    }

    program () {
        // TODO poner codigo aqui
        while(frontIsClear()) {
            move();
            girar(3);
            pozo();
        }
        girar(2);
        while(leftIsClear()) {
            if(nextToABeeper()) {
                pickbeeper();
                while(frontIsClear()) {
                    move();
                }
                putbeeper();
                irFrenteYGirar2();
                girar(2);
            }
            else {
               move();
            }
        }
        turnoff();
    }
}
```
