# Problema 2: Invertido y arriba

Codigo del problema: U4L15Ejer_AAAC

### Descripción

Hay varios montones de trompos en linea y Karel debe moverlos a la fila de arriba (resuelve este problema usando recursion).

## Mundo de Entrada

![L15P2ME.png](L15P2ME.png?raw=true)

## Mundo de Salida

![L15P2MS.png](L15P2MS.png?raw=true)

### Consideraciones

- No importan la orientacion ni posicion de Karel
- Karel tiene infinitos trompos en su mochila

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
class program {
    void recursion(){
        if(nextToABeeper()) {
            pickbeeper();
            recursion();
            putbeeper();
        }
        else {
            move();
            if(nextToABeeper()) {
                recursion();
                move();
            }
            else {
                turnleft();
                move();
                turnleft();
                move();
            }
        }
    }
    program () {
        // TODO poner codigo aqui
        move();
        recursion();
        turnoff();
    }
}
```
