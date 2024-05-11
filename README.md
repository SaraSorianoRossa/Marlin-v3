## Descripción general
Esta implementación viene dada a través de realizar una modificación a la [segunda versión](https://github.com/SaraSorianoRossa/Marlin-v2) del [algoritmo de Marlin](https://github.com/arkworks-rs/marlin). 
Esta nueva modificación está muy relacionada con la de la primera versión, de hecho es la continuación de ella. 
La única diferencia es que ahora no se envía un compromiso de $t(X)$ al verificador, ya que eso es lo que se comprobaba en el inner. 
Ahora $v(t)$ se envía directamente en el momento correspondiente. Es decir, una vez comienza el proceso de verificación de outer_sumcheck.
Para conseguirlo se ha estudiado las partes donde se debía de realizar este proceso y se han realizado una serie de modificación en los distintos archivos pemitiendo que este cambio siga ofreciendo la prueba de Marlin con una mayor eficiencia a la versión anterior.

A esta implementación se le ha aplicado una nueva modificación con tal de poder obtener un mejor rendimiento del algoritmo de Marlin:
1. [Tercera modificación](https://github.com/SaraSorianoRossa/Marlin-v4)

Además de esta modificación se ha definido un [nuevo proceso inner](https://github.com/SaraSorianoRossa/New-inner) en el cual se comprobaba la veracidad de la abertura del polinomio $t(X)$.

## Build
Para ejecutar este programa es necesario tener previamente instalado cargo y rust. Una vez se tienen instaladas las librerías necesarias para poder ejecutar la prueba con esta versión es necesario estar en el directorio y escribir en la terminal:
```sh
cargo build --release
```

## Test
En esta versión, igual que en el resto, se ofrece una serie de funciones para testear. Si se desea ejecutarlas para ver el resultado de ellas:
```sh
cargo test
```
## Todas las implementaciones
1. [Versión original](https://github.com/SaraSorianoRossa/Marlin-v1)
2. [Primera modificación](https://github.com/SaraSorianoRossa/Marlin-v2)
3. [Segunda modificación](https://github.com/SaraSorianoRossa/Marlin-v3)
4. [Tercera modificación](https://github.com/SaraSorianoRossa/Marlin-v4)
5. [Nuevo proceso inner](https://github.com/SaraSorianoRossa/New-inner)
