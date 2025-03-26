# Problema 1: Al otro lado del muro

Codigo del problema: U4L15Ejem_AAAC

### Descripción

Hay varios montones de trompos en el lado izquierdo del muro, Karel tiene la tarea de recoger todos los montones y dejarlos en el otro lado de forma que el orden de los montones se refleje (en los mundos de entrada/salida se muestra como debe ser).

## Mundo de Entrada

![L15P1ME.png](L15P1ME.png?raw=true)

## Mundo de Salida

![L15P1MS.png](L15P1MS.png?raw=true)

### Explicación

La explicacion se muestra en comentarios dentro del codigo, asi que aqui se explicara algo basico de la recursion anidada.

Si tenemos una o varias operaciones despues de una llamada a alguna funcion, esta(s) operacion(es) se guardaran en una "pila de comandos", pendientes para ejecutarse luego; cuando el codigo ya no encuentra operaciones por ejecutar, se ira a la pila de comandos y empezara a ejecutar las operaciones que esten en el tope de la pila hasta que se vacie.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
class program {

    void recursion(){

        if(nextToABeeper()){ //hay un beeper, lo recogeremos
            pickbeeper();
            recursion(); //llamamos a la funcion de nuevo
            putbeeper(); //esta accion se guarda a la pila de operaciones pendientes
        }
        else{ //no hay beeper, sigamos adelante
            if(frontIsClear()){ //significa que aun hay otra pila de trompos
                move();
                recursion(); //se llama a recursion
                move(); //se guarda a la pila de operaciones un move
            }
            else{ //hemos alcanzado el muro, entonces ya recogimos todos los trompos y hay que dejarlos en el otro lado
                turnleft(); //las operaciones en este else tienen como proposito rodear el muro
                move();
                iterate(3)turnleft();
                move();
                iterate(3)turnleft();
                move();
                turnleft();
            }
        }
    }

    program () {
        recursion(); //comenzamos la recursion llamando a la funcion
        turnoff(); //fin de ejecucion
    }
}
```
