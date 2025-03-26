# Problema 3: Linea de comandos

Codigo del problema: U4L15Ejem_AAAC

### Descripción

Hay un linea de montones de 1 o 2 trompos frente a Karel que consisten de un conjunto de comandos que Karel debe seguir al pie de la letra.

- Los montones de 1 trompo significan moverse una casilla hacia el frente
- Los montones de 2 trompos significan girar a la izquierda una vez

Karel seguira el orden de estos comandos de izquierda a derecha empezando en la esquina (1,1) mirando hacia la derecha.

## Mundo de Entrada

![L15P3ME.png](L15P3ME.png?raw=true)

## Mundo de Salida

![L15P3MS.png](L15P3MS.png?raw=true)

### Consideraciones

- Solo importa la posicion y orientacion final de Karel
- La linea de montones de trompos comienza en la casilla (1,2)
- No hay trompos en la mochila de Karel

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
class program {

    void recursion(){
        if(nextToABeeper()){ ///hay un beeper
            pickbeeper(); //lo recogemos
            if(nextToABeeper()){ //si hay otro, entonces el comando es girar a la izquierda
                pickbeeper(); //recoge el beeper
                move(); //nos movemos a la siguiente casilla a ver si hay otro comando
                recursion(); ///llamamos a la funcion
                turnleft(); ///guardamos un turnleft en la pila de operaciones pendientes
            }
            else{ //si no, el comando es moverse hacia el frente
                move(); //nos movemos a la siguiente casilla a ver si hay otro comando
                recursion(); //llamamos a la funcion
                move(); //guardamos un turnleft en la pila de operaciones pendientes
            }
        }
        else{ //ya no hay mas comandos que checar, solo queda dejar que el codigo
            //ejecute lo que hay en la pila de pendientes
                //y por nuestro recorrido, terminamos en la casilla (1,1) viendo a la izquierda
            iterate(2)turnleft(); //nos acomodamos con turnleft y dejamos la pila de pendientes ejecutarse
        }
    }

    program () {
        // TODO poner codigo aqui
        move(); //por como funciona la recursion anidada
        //es necesario empezar desde la derecha de la linea
        while(nextToABeeper())move(); //nos movemos al otro lado
        iterate(2)turnleft();
        move();
        recursion(); //llamamos la funcion
        turnoff();
    }
}
```
