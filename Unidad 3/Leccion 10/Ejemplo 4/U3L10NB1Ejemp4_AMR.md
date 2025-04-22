# Ejemplo básico #4 de funciones o subprogramas (U3L10NB1Ejemp4_AMR)

Código de ejemplo: U3L10NB1Ejemp4_AMR

Karel se encuentra en su casa, que es rectangular, y quiere redecorar las celdas internas, para empezar, necesita contar las celdas manchadas dentro de su casa. Las celdas manchadas están representadas por montones de tres trompos, las celdas no manchadas tienen montones de cero uno o dos trompos.

### Problema

Ayuda a Karel a contar la cantidad de celdas manchadas, colocando el resultado en la esquina de más al suroeste de su habitación, como se muestra en el ejemplo.

## Mundo de Entrada

![L10E4ME.png](L10E4ME.png?raw=true)

## Mundo de Salida

![L10E4MS.png](L10E4MS.png?raw=true)

### Consideraciones

- Karel inicia en la esquina inferior izquierda del rectángulo, orientado hacia el norte.
- En la esquina donde inicia Karel no hay trompos o beepers.
- Karel inicia sin trompos en su mochila.
- El resultado debe quedar en la esquina donde Karel inicio su tarea. Los trompos deberán quedar como cuando inicio Karel su tarea, excepto las celdas donde estaban las manchas y donde debe quedar el resultado.
- No importa la posición o dirección final de Karel.
- Karel debe terminar sin trompos en su mochila.

### Explicacion

Vamos a recorrer el rectángulo de abajo hacia arriba, y de izquierda a derecha. Cada vez que llegue Karel a la barda del norte, me regreso por la misma columna (invocando a una función para este propósito), y al llegar a la barda del sur (de esa misma columna por donde baje), giro a la izquierda, para preguntar si está libre al frente, de ser así avanzo una cuadra al este, y giro a la izquierda para quedar viendo al norte, e iniciar el recorrido de otra nueva columna. Pero si cuando bajo del norte al sur, al llegar a la barda de más al sur, y girar a la izquierda está bloqueado, es porque ya terminé de recorrer el rectángulo y solo me dirijo a dejar el resultado donde se me indico (utilizando una función).

En cada celda que voy visitando investigo para confirmar si ahí hay tres trompos, de ser así levanto uno de ellos (esto lo hago con otra función).

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void siSonTresLevantaUno(){
        if(nextToABeeper){
            pickbeeper();
            if(nextToABeeper){
                pickbeeper();
                if(nextToABeeper){
                    putbeeper();//eran 3, regreso uno
                }               //y me quedo con uno
                else{//eran dos regreso los dos
                    putbeeper();
                    putbeeper();
                }
            }
            else{//era uno,lo regreso
                putbeeper();
            }
        }
    }
    void meRegreso(){
         turnleft();
         turnleft();
         while(frontIsClear){
             move();
         }
    }
    program () {
        // TODO poner codigo aqui
        while(frontIsClear){
            while(frontIsClear){
                 move();
                 siSonTresLevantaUno();
            }
            meRegreso();
            turnleft();
            if(frontIsClear){
                move();
                turnleft();
            }
        }
        //Ya recorrio todo el rectangulo
        meRegreso();
        iterate(3){//Lo volteo al norte
            turnleft();
        }
        while(anyBeepersInBeeperBag){
            putbeeper();
        }
        turnoff();
    }
}
```
