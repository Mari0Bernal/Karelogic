# Ejemplo básico de funciones con recursividad (U3L10NB1Ejemp5_AMR)

Codigo del ejercicio: U3L10NB1Ejemp5_AMR

Karel transitaba por las calles de la ciudad de Monterrey, cuando se percató que estaban llenas de baches. Karel quiere ahora encontrar el tramo más grande sin baches.

### Problema

Ayuda a Karel a encontrar el tramo más grande, y apagarse en el extremo derecho del mismo.

## Mundo de Entrada

![L10E5ME.png](L10E5ME.png?raw=true)

## Mundo de Salida

![L10E5MS.png](L10E5MS.png?raw=true)

### Consideraciones

- El mundo de Karel es rectangular.
- Se asegura que la altura del rectángulo es mayor que la medida del tramo más grande.
- Karel lleva infinitos trompos en la mochila.
- Siempre habrá un solo tramo de mayor longitud, es decir, no habrá empates.

### Tips

- Utiliza una función para cada uno de los tramos.
- Recuerda utilizar la pila de Karel.
- Puedes recorrer todo el mundo.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {///Este problema esta resuelto con recursividad
    void funcion(){///Esta es un funcion recursiva
        if(rightIsBlocked){
            move();
            funcion();
            putbeeper();
        }
    }
    void funcion2(){///Esta tambien es una funcion recursiva
        if(nextToABeeper){
            pickbeeper();
            funcion2();
            move();
            putbeeper();
        }
        else {
            iterate(3)turnleft();
        }
    }
    void encontrar(){
        while(!nextToABeeper){
            if(frontIsClear){
                move();
            }
            else {
                turnleft();
                turnleft();
                while(frontIsClear)move();
                turnleft();
                move();
                turnleft();
            }
        }
        iterate(3)turnleft();
        while(frontIsClear)move();
        turnleft();
        turnleft();
        move();
        turnleft();
        move();
        turnleft();
        turnleft();
    }
    program () {
        while(frontIsClear){
            funcion();
            if(frontIsClear)move();
        }
        turnleft();
        turnleft();
        while(frontIsClear){
            if(nextToABeeper){
                funcion2();
                turnleft();
                turnleft();
                while(frontIsClear)move();
                turnleft();
                turnleft();
                move();
                turnleft();
            }
            else move();
        }
        iterate(3)turnleft();
        while(frontIsClear)move();
        iterate(3)turnleft();
        encontrar();
        turnoff();
    }
}
```
