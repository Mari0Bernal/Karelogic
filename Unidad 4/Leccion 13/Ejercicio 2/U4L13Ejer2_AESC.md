# Ejercicio #2 Reubicando cajas (U4L13Ejer2_AESC)

Codigo del problema: U4L13Ejer2_AESC

### Descripcion

Karel fue encontrado vacio y descargado, se le ha proporcionado una bateria y un monton de n trompos, la bateria le permitira moverse n casillas y asi podra dejar los trompos donde debe estar.

### Problema

La tarea de Karel es recoger los n trompos y dejarlos n casillas mas adelante.

## Mundo de Entrada

![L13Ej2ME.png](L13Ej2ME.png?raw=true)

## Mundo de Salida

![L13Ej2MS.png](L13Ej2MS.png?raw=true)

### Consideraciones

- Karel inicia con su mochila vacia.
- Karel inicia en la posicion (1,1) orientado hacia el este.
- Karel inicia junto a un monton de n trompos.
- Karel debe terminar en la posicion (n+1,1) orientado hacia el este.
- Se debe usar una funcion recursiva
- Tu solucion sera evaluada con diferentes mundos de entrada, es decir, mundos donde al inicio Karel esta encima de un numero difrente a 10 beepers o trompos, que puedes ser 5 o 14 o alguno numero diferentes de beepers.
- Se asegura que el numero de beepers o trompos donde inicia Karel sera menor a 100.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void contar(n){
        if(nextToABeeper()) {
            pickbeeper();
            contar(succ(n));
            move();
        }
    }
    program () {
        // TODO poner codigo aqui
        contar(0);
        while(anyBeepersInBeeperBag()) {
            putbeeper();
        }
        turnoff();
    }
}
```
