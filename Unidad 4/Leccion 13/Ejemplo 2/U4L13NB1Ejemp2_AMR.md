# Ejemplo 2 Recursividad (U4L13NB1Ejemp2_AMR)

Codigo del ejemplo: U4L13NB1Ejemp2_AMR

Karel va de camino a su casa, pero se da cuenta de que en el camino hay monedas tiradas. Ayuda a Karel a llevar las monedas a su casa.

### Problema

Ayuda a Karel a recolectar las monedas que se encuentra en su camino, y dejarlas en su casa.

## Mundo de Entrada

![L13E2ME.png](L13E2ME.png?raw=true)

## Mundo de Salida

![L13E2MS.png](L13E2MS.png?raw=true)

### Consideraciones

- Karel inicia orientado hacia su casa.
- Las monedas están representadas por montones de un trompo.
- Karel lleva infinitos trompos en la mochila.
- Recuerda que se puede llamar a una función recursiva desde distintos lugares de la misma.

### Explicación

Karel se encuentra ya en el camino hacia su casa, así que solo tendrá que recorrer en línea recta. Creamos una función (recogeTrompos), y en esta función agregamos un if(frontIsClear), para que la función se repita mientras el frente se encuentre despejado, recogiendo los trompos y dejando pendiente la instruccion de putbeeper(); en la línea 8 del programa, para que cuando termine de ejecutarse, atienda estas llamadas y pueda dejar los trompos en el lugar donde terminó, que es donde el frente se encontraba bloqueado.

El "else" de la línea 13, se encarga de avanzar cuando no encuentre trompos, y llama a la funcion recursiva, pero sin escribir un "putbeeper( )" despues de la llamada recursiva.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void recogeTrompos(){
        if(frontIsClear){//mientras el frente
                         // se encuentre libre
            if(nextToABeeper){//Si hay trompo lo levanta
                pickbeeper();
                move();
                recogeTrompos();//Karel carga a memoria otra
                            //nueva copia de la funcion
                putbeeper();//Aqui regresa Karel en
                          //en cada copia que habia dejado
            }             //pendiente de terminar de procesar
            else {
                move();
                recogeTrompos();
              //Aqui regresa, en algunas copias pendientes
              //pero no hace nada puesto que no hay instrucciones
            }
        }
    }
    program () {
        recogeTrompos();//llamamos a la función recursiva
        turnoff();
    }
}
```
