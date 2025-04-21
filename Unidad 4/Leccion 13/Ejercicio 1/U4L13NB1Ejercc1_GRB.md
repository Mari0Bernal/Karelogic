# Ejercicio # 1 Recursividad, contar las bardas de la izquierda(U4L13NB1Ejercc1_GRB)

Codigo del ejercicio: U4L13NB1Ejercc1_GRB

Karel va de camino a su casa, pero se da cuenta de que en el camino, en algunas cuadras hay una barda a su izquierda. Ayuda a Karel a contar estas bardas de la izquierda, en su camino a su casa.

### Problema

Ayuda a Karel a contar las bardas que se encuentre a su izquierda en su camino a casa, y dejar el resultado en la siguiente cuadra al norte de su casa.

## Mundo de Entrada

![L13Ej1ME.png](L13Ej1ME.png?raw=true)

## Mundo de Salida

![L13Ej1MS.png](L13Ej1MS.png?raw=true)

### Consideraciones

- Karel inicia orientado hacia su casa.
- Karel debe terminar una cuadra al norte despues de donde deje su resultado.
- Junto a la casa de Karel no hay barda a su izquierda.
- Karel lleva infinitos trompos en la mochila.
- Cada barda es de una cuadra de longitud, y podra haber dos o mas bardas seguidas, cada una de una cuadra.
- Recuerda que se puede llamar a una función recursiva desde distintos lugares de la misma.

### Explicación

Karel se encuentra ya en el camino hacia su casa, así que solo tendrá que recorrer en línea recta. Creamos una función (cuentaBardas( )), y en esta función agregamos un if(frontIsClear) con su "else", para que la función se repita mientras el frente se encuentre despejado, pero en cada cuadra debera ver si hay o no hay barda a su izquierda; te recomendamos ver de nuevo el segundo ejemplo de esta misma Leccion 13. Las instrucciones del "else" del primer "if", dentro de la funcion recursiva, es lo que procesara Karel cuando ya llega a su casa.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void problema(n){
        if(frontIsClear()) {
            if(leftIsBlocked()) {
                move();
                problema(succ(n));
                putbeeper();
            }
            else {
                move();
                problema(n);
            }
        } else {
            turnleft();
            move();
        }
    }
    program () {
        // TODO poner codigo aqui
        problema(0);
        move();
        turnoff();
    }
}
```
