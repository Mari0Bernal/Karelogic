# Ejemplo #2 de Recursividad (uso del succ y del else); (U4L14NB1Ejemp2_AMR)

Código del ejemplo: U4L14NB1Ejemp2_AMR

Karel se encuentra en el supermercado, comprando bolsas de limones. Él quiere hacer pollo al limón, pay de limón y limonada, pero no sabe cuál bolsa de limones llevarse.

### Problema

Como Karel necesitará muchos limones, tu tarea es ayudar a Karel a comparar las dos bolsas de limones, representadas por montones de trompos, encontrar la mayor, y apagarse en esa posición.

## Ejemplos

### Ejemplo 1

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Entrada

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E2ME,E1.png](L14E2ME,E1.png?raw=true)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Salida

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E2MS,E1.png](L14E2MS,E1.png?raw=true)

### Ejemplo 2

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Entrada

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E2ME,E2.png](L14E2ME,E2.png?raw=true)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Salida

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E2MS,E2.png](L14E2MS,E2.png?raw=true)

### Consideraciones

- Karel inicia sobre el montón izquierdo de trompos, orientado al este.
- Karel inicia con infinitos trompos en la mochila.
- Solo se evalúa la posición final de Karel.
- Recuerda utilizar el succ, y la recursividad para la solución de este problema.
- Los montones siempre tendrán una diferencia de al menos un trompo, es decir, no habrá equivalentes.

### Explicación

Karel inicia en el primer montón de trompos, el cual comienza a recoger mediante una función recursiva con succ( ), para así contar los trompos del montón. Una vez que terminó de recoger el primer montón, avanza al siguiente, donde intentará recoger la misma cantidad de montones que recogió en el primer montón (iterate(a), línea 9). Si en algún momento detecta que se terminan los trompos del segundo montón, esto quiere decir que el primer montón era mayor, así que volverá a la posición anterior y se apagará. En cambio, si Karel logra recoger todos los trompos que intentó, y aún quedan, esto quiere decir que este segundo montón es mayor que el primero, y solamente se apaga.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void quedateEnElMayor(a){
        if(nextToABeeper){           //recoge los trompos
            pickbeeper();            // del primer montón
            quedateEnElMayor(succ(a));
        }
        else {
            move();                  //avanza al segundo montón
            iterate(a){
                if(nextToABeeper){
                    pickbeeper();
                }
                else {
                    turnleft();
                    turnleft();
                    move();
                    turnoff();
                }
            }
        }
    }
    program () {
        quedateEnElMayor(0);
        turnoff();
    }
}
```
