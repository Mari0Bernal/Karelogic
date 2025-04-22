# Ejercicio de funciones Karel el Agricultor

### Ejercicio 1 (funciones), Karel el multiplicador; U3L10NB1Ejercc1_GRB

Codigo del ejercicio: U3L10NB1Ejercc1_GRB

Karel se encuentra con direccion al este, necesita llegar a su casa que esta, al este, a una distancia no conocida representada por una barda.

Karel heredo un pequeño terreno y desea plantar maíz en surcos designados, para que el maiz de frutos, es necesario plantar varios granos en un solo zurco, karel desea plantar 7 granos en cada zurco para asegurar que el maiz de frutos.

### Problema

Ayuda a Karel a cumplir con su mision de caridad, colocando siete granos de maiz en cada celda disponible, como se muestra en el ejemplo.

## Mundo de Entrada

![L10AME.png](L10AME.png?raw=true)

## Mundo de Salida

![L10AMS.png](L10AMS.png?raw=true)

### Consideraciones

- Karel el tamaño de la hilera donde karel plantará su maiz puede variar.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    program () {
        // TODO poner codigo aqui
        while(frontIsClear()) {
            iterate(7) {
                putbeeper();
            }
            move();
            if(frontIsBlocked()) {
                iterate(7) {
                    putbeeper();
                }
            }
        }
        turnoff();
    }
}
```
