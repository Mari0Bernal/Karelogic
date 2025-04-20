# Ejemplo #4 de Recursividad (U4L14NB1Ejemp4_AMR)

Código del ejemplo: U4L14NB1Ejemp4_AMR

Karel está jugando un juego de canicas, el cual consiste en pasar la canica que se encuentre más cerca a un extremo, al otro lado de un palito.

### Problema

Ayuda a Karel a encontrar cuál de las dos canicas (trompos) se encuentra más cerca del extremo, y pásalo al otro lado, en la misma fila. (Ver ejemplo)

## Ejemplos

### Ejemplo 1

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Entrada

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E4ME,E1.png](L14E4ME,E1.png?raw=true)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Salida

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E4MS,E1.png](L14E4MS,E1.png?raw=true)

### Ejemplo 2

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Entrada

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E4ME,E2.png](L14E4ME,E2.png?raw=true)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Salida

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; ![L14E4MS,E2.png](L14E4MS,E2.png?raw=true)

### Consideraciones

- Solo se evalúa el trompo que debe quedar al lado izquierdo del muro.
- Karel inicia en algún punto, pegado al lado derecho del muro.
- Karel inicia con orientación al norte.
- La mochila de Karel tiene infinitos trompos.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void encuentra(a){
        if(!nextToABeeper){
            iterate(a)putbeeper();
            move();
            encuentra(succ(a));
        }
        else {
            pickbeeper();
            iterate(a)putbeeper();
            while(rightIsBlocked)move();
            turnleft();
            turnleft();
            encuentra2(0);
        }
    }

    void encuentra2(b){
        if(!nextToABeeper){
            iterate(b)putbeeper();
            move();
            encuentra2(succ(b));
        }
        else {
            pickbeeper();
            iterate(b)putbeeper();
            compara();
        }
    }
    void compara(){
        if(nextToABeeper){
            pickbeeper();
            compara();
            if(nextToABeeper)pickbeeper();
            else {
                if(!facingSouth){
                    turnleft();
                    turnleft();
                    while(!nextToABeeper)move();
                    turnleft();
                    turnleft();
                    move();
                    turnleft();
                    turnleft();
                }
            }
        }
        else {
            while(!nextToABeeper)move();
        }
    }
    void pasaAlOtroLado(){
        if(facingNorth){
            if(leftIsBlocked){
                move();
                pasaAlOtroLado();
                move();
            }
            else {
                turnleft();
                move();
                turnleft();
            }
        }
        else if(facingSouth){
            if(rightIsBlocked){
                move();
                pasaAlOtroLado();
                move();
            }
            else {
                iterate(3)turnleft();
                move();
                iterate(3)turnleft();
            }
        }
    }
    program () {
        while(leftIsBlocked)move();
        turnleft();
        turnleft();
        encuentra(0);
        if(facingNorth){
            turnleft();
            turnleft();
            move();
            while(!nextToABeeper)move();
            turnleft();
            turnleft();
            move();
        }
        if(facingSouth){
            turnleft();
            turnleft();
            move();
            while(!nextToABeeper){
                move();
            }
            turnleft();
            turnleft();
            move();
            turnleft();
            turnleft();
        }
        pasaAlOtroLado();
        putbeeper();
        turnoff();
    }
}
```
