# Ejercicio #3 Contador de burocratas (U4L14Ejer4_AESC)

Codigo del problema: U4L14Ejer4_AESC

## Descripcion

Karel, harto de la burocracia, se encomendo a una labor interesante: debe hacer un trámite, pero al llegar se da cuenta de que llego mucha gente igual que el a hacer un tramite. Decide formarse en la primera ventanilla y le dicen que su tramite se puede hacer en la ventanilla que esta N pasos al este. Karel siguio las instrucciones, y al llegar a la siguiente ventanilla se le dice exactamente lo mismo.

Despues de hacer esto una cantidad incontable de veces, Karel por fin llega a la ventanilla que puede hacer su tramite.

### Problema

Karel debe llegar a la ventanilla donde pueden hacer su tramite, contar la cantidad de personas con las que hablo para llegar a dicha ventanilla y dejar un valor equivalente de trompos en esa ventanilla.

## Ejemplo

Entrada

![L14Ej3ME.png](L14Ej3ME.png?raw=true)

Salida

![L14Ej3MS.png](L14Ej3MS.png?raw=true)

### Consideraciones

- Karel tiene infinitos trompos en su mochila.
- Karel inicia en la posicion (1,1) orientado hacia el este.
- Karel inicia junto a un monton de trompos.
- Sabes que una persona puede hacer tu tramite cuando su N es 0, es decir, no tiene trompos.
- Karel debe terminar en una casilla sin trompos orientado hacia el este.
- Se garantiza que Karel pueda llegar al lugar de llegada.
- Se debe usar una funcion recursiva.
- El mismo codigo sera probado en varios mundos.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {

    void camino(n){
        if(nextToABeeper()) {
            pickbeeper();
            if(notNextToABeeper()) {
                camino(succ(n));
                putbeeper();
            }
            else {
                camino(succ(n));
            }
        }
        else {
            iterate(n) move();
            if(nextToABeeper()) {
                camino(0);
            }
        }
    }
    program () {
        // TODO poner codigo aqui
        camino(0);
        turnoff();
    }
}
```
