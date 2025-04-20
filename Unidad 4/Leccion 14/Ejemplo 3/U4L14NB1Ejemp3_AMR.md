# Ejemplo #3 de Recursividad (uso del succ y del else); (U4L14NB1Ejemp3_AMR)

Código del ejemplo: U4L14NB1Ejemp3_AMR

Karel está en su casa, la cual tiene dos habitaciones, pero quiere saber cuál de las dos es más grande.

### Problema

Ayuda a Karel a medir las habitaciones y apagarse en la entrada de la que sea más grande.

## Ejemplos

### Ejemplo 1

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Entrada

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E3ME,E1.png](L14E3ME,E1.png?raw=true)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Salida

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E3MS,E1.png](L14E3MS,E1.png?raw=true)

### Ejemplo 2

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Entrada

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E3ME,E2.png](L14E3ME,E2.png?raw=true)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Salida

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E3MS,E2.png](L14E3MS,E2.png?raw=true)

### Consideraciones

- La altura de las habitaciones es la misma, lo que varía es la longitud.
- Karel deberá apagarse en la entrada de la habitación más grande.
- Siempre habrá una casilla de distancia entre las dos habitaciones.
- Solo se evalúa la posición final de Karel.
- Karel inicia sin trompos en la mochila.
- Recuerda que puedes apagar a Karel en cualquier punto del programa.
- Siempre habrá una habitación más grande que la otra, nunca serán iguales.

### Explicación

Primero, Karel comienza a recorrer la primera habitación, aumentando a la variable a (utilizando el succ), para guardar la longitud en la variable. Posteriormente, Karel se desplaza hacia la entrada de la siguiente habitación, para ahí comenzar a recorrerla. Aquí, Karel intenta avanzar la misma cantidad de veces que en la habitación anterior, y si en algún momento se encuentra con una pared, así sabrá que esta es más pequeña que la anterior. En caso de que se encuentre con una pared, vuelve a la primera habitación y se apaga en la entrada de la misma. Si no encuentra pared, siginificará que la segunda habitación es más grande que la primera, y en este caso solamente se posiciona en la entrada de la habitación, y se apaga.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void gira(x){//función para girar las
        iterate(x){// veces que se le indique
            turnleft();
        }
    }
    void encuentraElRectanguloMayor(a){
        if(rightIsBlocked){ //Avanza de manera recursiva
            move();        // hasta tener la derecha libre.
            encuentraElRectanguloMayor(succ(a));//Cuenta cuántas veces avanzó.
        }
        else {//Llegó al final de la primera habitación.
            gira(3);
            move();
            turnleft();
            move();
            while(leftIsBlocked){
                move();
            }
            turnleft();
            move();
            turnleft();
            move();
            iterate(a){ //Intenta avanzar la medida de la primera hab.
                if(frontIsClear){  //Sigue estando el frente libre.
                    move();
                }
                else { //Ha topado con una pared, entonces se posiciona
                    gira(2); // en la otra habitación
                    while(rightIsBlocked){
                        move();
                    }
                    gira(3);
                    move();
                    gira(3);
                    move();
                    while(rightIsBlocked){
                        move();
                    }
                    gira(3);
                    move();
                    turnleft();
                    move();
                    turnoff();
                }
            }
            gira(2);//Si no topó con ninguna pared, solo regresa
            while(rightIsBlocked){// a la entrada.
                move();
            }
            gira(2);
            move();
            turnoff();
        }
    }
    program () {
        encuentraElRectanguloMayor(0);
        turnoff();
    }
}
```
