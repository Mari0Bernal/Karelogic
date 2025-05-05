# Aprobado o Reprobado

**Problema:**

Dada la calificación de un estudiante, determinar si aprobó o reprobó.

**Consideraciones:**

- El programa debe leer la calificación de un estudiante (entero entre 0 y 100).
- Usar if-else para determinar si el estudiante aprobó (calificación >= 60) o reprobó.
- Imprimir el resultado correspondiente.
- Imprimir el resultado en mayusculas "APROBADO" o "REPROBADO" respectivamente

### Ejemplo:

**Entrada:**

75

**Salida:**

APROBADO

**Entrada:**

48

**Salida:**

REPROBADO

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación o preguntale a tu profesor.

```
#include<bits/stdc++.h>
using namespace std;

int main() {
    int calif;
    cin >> calif;
    if (calif < 0 || calif > 100){
        cout << "Favor de ingresar un numero entre 0 y 100";
        return 0;
    }

    if (calif >= 60){
        cout << "APROBADO";
    } else {
        cout << "REPROBADO";
    }
    return 0;
}
```
