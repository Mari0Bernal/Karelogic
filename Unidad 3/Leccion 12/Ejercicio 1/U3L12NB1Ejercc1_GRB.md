# Ejercicio Básico Numero 1 de la Lección 12, funciones (U3L12NB1Ejercc1_GRB)

Código del ejercicio: U3L12NB1Ejercc1_GRB

En su actual trabajo, el arquitecto Karel está encargado de pavimentar diferentes tramos de carretera hasta el palacio de Cantera. El problema es que los tramos son de diferentes características y dimensiones, además de que no se conoce la cantidad exacta de tramos a pavimentar. Los tramos más frágiles deberán ser reforzados con montones de 8 trompos en cada cuadra del tramo, y otros tramos más fuertes podrán ser pavimentados con montones de cinco trompos en cada cuadra.

### Problema

Ayuda a Karel a pavimentar de manera eficiente la carretera al palacio de Cantera. Se deben colocar montones de 8 trompos en cada cuadra de los tramos más frágiles, que están representados por tramos sin barda a su derecha, y con montones de 5 trompos los tramos más fuertes, que están representados por tamos con barda a su derecha.

## Mundo de Entrada

![L12Ej1ME.png](L12Ej1ME.png?raw=true)

## Mundo de Salida

![L12Ej1MS.png](L12Ej1MS.png?raw=true)

### Consideraciones

- Karel inicia con suficientes objetos trompo en su mochila.
- Karel inicia con dirección al norte, y la carretera esta de sur a norte.
- La posición inicial de Karel es donde comienza el primer tramo fuerte (con barda a su derecha).
- No se conoce la cantidad de ni las dimensiones de los tramos fuertes ni de los tramos frágiles.
- El palacio de Cantera está representado por una barda al norte y es de una cuadra de largo.
- Karel debe terminar con dirección al norte y junto a la barda que representa el palacio de Kantera.
- El último tramo de carretera puede ser de los frágiles o de los fuertes.

### Requisito

Tu solución deberá incluir al menos otra función o subprograma además de la función principal (program()).

### Explicación

Puedes crear dos funciones, una para los tramos de 5 trompos “rellenaTramo5()" y otra para los tramos de 8 trompos (rellenaTramo8()), y llamaras a una u otra, dependiendo si el nuevo tramo a rellenar tiene o no tiene barda a su derecha.
En términos generales, en la función principal "program()" solo usarías el siguiente "while()":
while(elFrenteEsteDespejado) {
"aquí escribes lo que falta para la solución";
}

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void rellenar(n){
        iterate(n) putbeeper();
    }

    void proceso(){
        if(rightIsBlocked()) {
            rellenar(5);
        }
        else {
            rellenar(8);
        }
    }
    program () {
        // TODO poner codigo aqui
        if(rightIsBlocked()) {
            rellenar(5);
        }
        while(frontIsClear()) {
            move();
            proceso();
        }
        turnoff();
    }
}
```
