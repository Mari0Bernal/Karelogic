# Bienvenido a tu entrenamiento de C/C++

Código del problema: U6L34Ejemp1_SENE

### Problema:

El programa deberá leer un arreglo A de tamaño N y deberá regresar la suma total de los elementos y el promedio de las cantidades pares del arreglo.

### Consideraciones:

- 1<=N<=10^5
- A_i<=1000
- El promedio puede contener decimales

### Ejemplo:

**Entrada:**

9

7 0 6 4 1 6 9 3 7

**Salida:**

43 4

**Explicación:**

La suma total de los elementos es igual a 43, los pares son 0, 6, 4, 6 y su promedio es 4.

## Código

> [!NOTE]  
> Antes de continuar, asegúrate de comprender el funcionamiento del código.  
> Si tienes dudas, consulta la documentación, haz un comentario para recibir ayuda o preguntale a tu profesor.

```
#include <bits/stdc++.h>

using namespace std;

int main(){
	int n;
	cin>>n;
	int sum=0;
	float sumPar=0, contPar=0, promPar; //Se crean las variables flotantes para mejor precisión
	vector<int> arreglo(n); //Se crea el vector de tamaño n
	for(int i=0; i<n; i++){
		cin>>arreglo[i];
		sum+=arreglo[i]; //Suma el valor de la posición actual
		if(arreglo[i]%2==0){ //Verifica la paridad
			sumPar+=arreglo[i]; //Suma al acumulado de pares
			contPar++; //Incrementa la cuenta de pares
		}
	}
	promPar=sumPar/contPar;
	cout<<sum<<" "<<promPar<<endl;
	return 0;
}
```
