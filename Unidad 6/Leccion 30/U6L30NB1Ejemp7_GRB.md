# Sembrando arboles; la división (primero de secundaria; 5Ene2025) (U6L30NB1Ejemp7_GRB)

Código: U6L30NB1Ejemp7_GRB

## Descripcion

Vamos a Dividir, a través de este ejemplo.

En la comunidad de San Juan, los alumnos de una secundaria están organizando una colecta para sembrar árboles en el parque del pueblo. Cada árbol cuesta "x" pesos (dato que deberá ser ingresado por el usuario y debe ser leído por el programa solución). Los alumnos recolectaron "y" pesos (dato que también deberá ser ingresado por el usuario y debe ser leído por el programa solución).

1. ¿Cuántos árboles podrán comprar con esa "y" cantidad de dinero?
   Explicación de la solución de este ejemplo de la operación de división simple:

Se trata de determinar cuántos arboles podrán comprar los alumnos si reunieron “y” pesos (digamos 3,750 pesos), y cada árbol les cuesta "x" pesos. Significa que debemos calcular cuantas veces cabe el valor "x" pesos en el número "y" pesos que pudieron recolectar.

La forma de solucionar este problema es dividir el valor "y" entre el valor "x".

El programa con la solución completa la puedes ver, analizar y probar en la sección de la derecha de esta misma página.

### Ejemplo:

**Entrada:**

150 3750

**Salida:**

25

pero el programa solución puede ser probado con diferentes datos de entrada

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.
> Te sugerimos probar cada ejemplo y cada ejercicio con diferentes datos de casos de prueba de entrada.
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <iostream>

using namespace std;

int main( ){
    int precio, recaudado, cantASembrar;
    cin>>precio>>recaudado;
    cantASembrar = recaudado / precio;
    cout<< cantASembrar;

    return 0;
}
```
