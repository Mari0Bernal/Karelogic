# Ejercicio 1 (funciones), Karel el multiplicador; U3L10NB1Ejercc1_GRB

Codigo del ejercicio: U3L10NB1Ejercc1_GRB

Karel se encuentra con direccion al este, necesita llegar a su casa que esta, al este, a una distancia no conocida representada por una barda.

Ahora Karel anda muy dadivoso y tiene el proposito de que, en el camino a su casa, si se encuentra monedas las va a multipilcar por cinco y dejarlas en el mismo lugar donde se las encuentre. Para suerte de Karel, le dijeron que solo podria encontrar montones de monedas de uno, dos o tres monedas (trompos).

### Problema

Ayuda a Karel a cumplir con su mision de caridad, colocando cinco veces mas monedas de las que se encuentra en cada celda, como se muestra en el ejemplo.

## Mundo de Entrada

![L10Ej1ME.png](L10Ej1ME.png?raw=true)

## Mundo de Salida

![L10Ej1MS.png](L10Ej1MS.png?raw=true)

### Consideraciones

- Karel inicia en la fila numero 5 orientado hacia el este.
- En la esquina donde inicia Karel no hay trompos o beepers.
- Karel inicia con trompos suficientes en su mochila para cumplir con su obra de caridad.
- Karel debe terminar, en su casa, del lado este de la barda (a la derecha de la barda, y con direccion al este).
- Donde Karel encuentre un trompo debe dejar 5, donde encuentre dos, debe dejar 10, y 15 donde encuentre 3.
- Requisito: utilizar al menos una funcion ademas de la funcion principal de "program( )".

### Tips

- A una funcion le puedes enviar un valor (1, 2 o 3), para indicarle a la funcion las veces por las que va a multiplicar el 5, y la puedes llamar como sigue: multiplicaPorCinco (2), multiplicaPorCinco(3), y la defines asi "void multiplicaPorCinco(a){ ......... }".
- En cada celda que vas visitando investigas para confirmar si ahi hay uno, dos o tres trompos, y en ese momento llamas a la funcion "multiplicaPorCinco(3)", enviandole el valor uno, dos, o tres segun corresponda.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void multiPorCinco(a){
        iterate(a) {
            iterate(5) {
                putbeeper();
            }
        }
    }
    program () {
        // TODO poner codigo aqui
        while(frontIsClear()) {
            move();
            if(nextToABeeper()) {
                pickbeeper();
                if(nextToABeeper()) {
                    pickbeeper();
                    if(nextToABeeper()) {
                        pickbeeper();
                        multiPorCinco(3);
                    }
                    else {
                        multiPorCinco(2);
                    }
                }
                else {
                    multiPorCinco(1);
                }
            }
        }
        turnleft();
        move();
        iterate(3) {
            turnleft();
        }
        move();
        iterate(3) {
            turnleft();
        }
        move();
        turnleft();

        turnoff();
    }
}
```
