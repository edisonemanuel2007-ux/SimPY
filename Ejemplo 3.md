# Ejemplo 3: Simulación de una línea de producción

## Descripción

En este ejemplo una máquina fabrica un producto cada cinco minutos durante quince minutos de simulación.

## Código

```python
import simpy

def maquina(env):

    while env.now < 15:

        print(f"Producto terminado en el minuto {env.now}")

        yield env.timeout(5)

env = simpy.Environment()

env.process(maquina(env))

env.run()
```

## Explicación

La función `maquina()` representa una máquina de producción.

Mientras el tiempo de simulación sea menor a quince minutos, la máquina fabrica un producto.

Después espera cinco minutos antes de fabricar el siguiente.

Todo el control del tiempo lo realiza SimPy mediante el objeto `Environment`.

## Salida

```
Producto terminado en el minuto 0
Producto terminado en el minuto 5
Producto terminado en el minuto 10
```

## Aplicaciones

Este tipo de simulación puede utilizarse para:

- Calcular la producción diaria.
- Analizar tiempos muertos.
- Determinar cuántas máquinas son necesarias.
- Mejorar la eficiencia de una fábrica.

## Conclusión

SimPy facilita la representación de procesos industriales mediante eventos discretos, permitiendo analizar la productividad sin detener una planta real.
