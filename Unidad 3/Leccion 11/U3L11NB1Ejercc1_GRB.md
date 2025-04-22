# Ejercicio 1 (funciones), Karel el Triangulador; U3L11NB1Ejercc1_GRB

Código del ejercicio: U3L11NB1Ejercc1_GRB

A Karel se le ocurrió decorar la mitad de su recamara. Como se cree muy creativo y original, decidió decorar su habitación en forma triangular.

### Problema

Ayuda a Karel a pintar en su recamara un triangulo de unos, formado por las paredes del norte y del oeste de su recamara.

## Mundo de Entrada

![L11Ej1ME.png](L11Ej1ME.png?raw=true)

## Mundo de Salida

![L11Ej1MS.png](L11Ej1MS.png?raw=true)

### Consideraciones

- El mundo de Karel es un cuadrado de dimensiones desconocidas.
- Se asegura que las dimensiones del cuadrado son tales que si completara con los objetos trompo de su mochila.
- Karel inicia con dirección desconocida en la esquina interna de más al suroeste de su habitación cuadrada.
- No importa la posición ni la orientación final de Karel.

### Requisito

Tu solución deberá incluir al menos otra función o subprograma además de la función principal (program()).

### Explicación

Comienzas por colocar a Karel con dirección al norte, luego, puedes utilizar dos while´s anidados, y recorrer el cuadrado en diagonal al noreste, comenzando por la diagonal principal. El siguiente "while" puede ser el más interno:

    while(frontIsClear ){

              "muevesAKarelEnDiagonal al noreste, hasta llegar a la pared del norte";

              "Y en cada celda al noreste dejas un trompo";

      }

Al salir del while anterior preguntas si su izquierda esta libre, de ser así (significa que aún faltan más diagonales), y por lo tanto debes llevar a Karel a la siguiente celda al norte de donde iniciaste la diagonal que acabas de completar.

Y la condición del while más externo puede ser "leftIsClear".

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void funcion1(){
        if(frontIsClear()) {
            move();
            putbeeper();
            funcion1();
            move();
        }
        else {
            girar(2);
        }
    }

    void girar(n){
        iterate(n) turnleft();
    }

    program () {
        // TODO poner codigo aqui
        while(notFacingEast()) {
            turnleft();
        }
        while(leftIsClear()) {
            putbeeper();
            turnleft();
            funcion1();
            girar(2);
            move();
            girar(3);
            move();
        }

        if(leftIsBlocked()) {
            putbeeper();
        }
        turnoff();
    }
}
```
