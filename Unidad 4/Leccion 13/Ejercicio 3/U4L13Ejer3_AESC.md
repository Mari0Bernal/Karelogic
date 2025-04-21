# Ejercicio #3 Unos trompos de Largo(U4L13Ejer3_AESC)

Codigo del problema: U4L13Ejer3_AESC

### Descripcion

Karel fue equipado con una cinta para medir, le pidieron determinar el largo de un trecho y Karel debe indicarles el largo correcto, asi que pusieron una pared como punto de parada. Karel no sabe como, ni porque o para que quieren la medidas, pero obtendra esa informacion.

### Problema

La tarea de Karel es recorrer n casillas hasta encontrar un muro y dejar n trompos al otro lado del muro.

## Mundo de Entrada

![L13Ej3ME.png](L13Ej3ME.png?raw=true)

## Mundo de Salida

![L13Ej3MS.png](L13Ej3MS.png?raw=true)

### Consideraciones

- Karel tiene infinitos trompos en la mochila.
- Karel inicia en la posicion (1,1) orientado hacia el norte.
- Solo hay un muro n casillas al norte.
- Karel debe terminar en la posicion (1,n+2) orientado hacia el norte.
- Karel solo dejara trompos en el lugar donde se apague.
- Se debe usar una funcion recursiva.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void contar(n){
        if(frontIsClear()) {
            move();
            contar(succ(n));
            putbeeper();
        }
        else {
            iterate(3) turnleft();
            move();
            turnleft();
            move();
            turnleft();
            move();
            iterate(3) turnleft();
        }
    }
    program () {
        // TODO poner codigo aqui
        contar(0);
        turnoff();
    }
}
```
