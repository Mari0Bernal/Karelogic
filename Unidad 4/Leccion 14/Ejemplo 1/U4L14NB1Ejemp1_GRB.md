# Ejemplo #1 de Recursividad, uso del succ( ), ( U4L14NB1Ejemp1_GRB)

Codigo del ejemplo: U4L14NB1Ejemp1_GRB

### Problema

La tarea de Karel es construir un triangulo de unos que crecera de norte a sur, ver figura del mundo de salida.

## Mundo de Entrada

![L14E1ME.png](L14E1ME.png?raw=true)

## Mundo de Salida

![L14E1MS.png](L14E1MS.png?raw=true)

### Consideraciones

- Karel inicia con su mochila vacia.
- Al comenzar Karel su tarea, se encuentra encima de un numero exacto de trompos para crear un triangulo de unos.
- Inicia en algun lugar de su mundo con direccion al sur.
- Se asegura que Karel si tiene espacio suficiente al sur para crear su famoso triangulo de las Bermudas.
- Karel debe terminar con direccion al sur en la posicion donde inicio su triangulito famoso.

### Explicación

Creamos la función "triangulo(x)", la cual, mediante un if , se estara llamando asi misma mientras tenga trompos en su mochila. En cada nueva llamada de la funcion recursiva, Karel incrementa en uno (con la funcion succ( x )) el valor del parametro "x", y con esto, incrementa en uno la cantidad de objetos trompo que dejara en cada nueva fila de unos del triangulo que esta creando.

Cuando ya se le terminan lo trompos de su mochila, Karel entrara al "else" para prepararse, volteando al norte, e iniciar su caminao a donde comenzo su tarea al norte.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {
    void gira(a){
            iterate(a){
                turnleft();
            }
    }
    void triangulo(x){
        if(anyBeepersInBeeperBag){
             iterate(x){
                 putbeeper();
                 move();
             }
             gira(2);
              iterate(x){
                 move();
             }
             gira(3);
             move();
             gira(3);
             triangulo(succ(x));
             move();
        }
        else{
            gira(3);
        }
    }
    program () {
        // TODO poner codigo aqui

        while(nextToABeeper()){
            pickbeeper();
        }
        gira(3);
        triangulo(1);
        gira(2);
        turnoff();
    }
}
```
