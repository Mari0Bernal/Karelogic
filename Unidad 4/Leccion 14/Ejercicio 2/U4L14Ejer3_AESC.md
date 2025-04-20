# Ejercicio #2 El sumatorio de Karel (U4L14Ejer3_AESC)

Codigo del problema: U4L14Ejer3_AESC

## Descripcion

Karel se emociono al aprender a sumar 2 montones de trompos, y para emocionarse mas, decidio aprender a sumar con muchos montones de trompos, el problema... Es que no le enseñaron a sumar muchas cosas, le toca ingeniarselas y ha pedido ayuda.

### Problema

Enseña a Karel a sumar una n montones de trompos.

## Ejemplo

Entrada

![L14Ej2ME.png](L14Ej2ME.png?raw=true)

Salida

![L14Ej2MS.png](L14Ej2MS.png?raw=true)

### Consideraciones

- Karel tiene trompos infinitos en su mochila.
- Karel inicia en la posicion (1,1) orientado hacia el este.
- Karel inicia junto a un monton de trompos.
- Karel debe dejar todos los trompos que recolecte en la primera casilla que no tenga trompos.
- Karel debe terminar en la posicion (n+1,1) orientado hacia el este.
- Se debe usar una funcion recursiva.
- El mismo codigo será probado en varios mundos.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación.

```
class program {

    void contar(n){
        if(nextToABeeper()) {
            pickbeeper();
            if(notNextToABeeper()) {
                move();
            }
            contar(succ(n));
        }
        else {
           iterate(n) {
               putbeeper();
           }
        }
    }
    program () {
        // TODO poner codigo aqui
        contar(0);
        turnoff();
    }
}
```
