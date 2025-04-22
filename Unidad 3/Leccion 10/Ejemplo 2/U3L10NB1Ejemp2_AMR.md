# Ejemplo básico #2 de funciones o subprogramas (U3L10NB1Ejemp2_AMR)

Codigo de ejemplo: U3L10NB1Ejemp2_AMR

Karel se encuentra en una escalera. En cada escalón se puede encontrar un montón de 0, 1, o 2 trompos.

### Problema

Dependiendo de la cantidad de trompos en cada posición, si encuentra 0 zumbadores deberá dejar 5, si encuentra 1 deberá dejar 10, y si encuentra 2, deberá dejar 15.

## Mundo de Entrada

![L10E2ME.png](L10E2ME.png?raw=true)

## Mundo de Salida

![L10E2MS.png](L10E2MS.png?raw=true)

### Consideraciones

- No se conoce la cantidad de escalones.
- Karel inicia en el primer escalón, orientado hacia el este.
- Karel inicia con infinitos trompos en la mochila.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void gira(a){       //Función para girar las
        iterate(a){     // veces que se le indique
            turnleft();
        }
    }
    void funcion(){          //Cuenta los zumbadores y hace
        if(nextToABeeper){   //  lo necesario con cada montón
            pickbeeper();
            if(nextToABeeper){
                pickbeeper();
                iterate(15){
                    putbeeper();
                }
            }
            else {
                iterate(10){
                    putbeeper();
                }
            }
        }
        else {
            iterate(5){
                putbeeper();
            }
        }
    }
    program () {
        while(frontIsBlocked){   //Mientras siga habiendo
            funcion();           // escalones hace esto
            gira(1);
            move();
            gira(3);
            move();
        }
        funcion();   //LLamo de nuevo a la función para
        turnoff();   // que Karel atienda el último escalón
    }
}
```
