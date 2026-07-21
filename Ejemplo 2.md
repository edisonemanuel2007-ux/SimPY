# Ejemplo 2: Simulación de una estación de gasolina

## Descripción

Se desea representar un automóvil que llega a una estación de gasolina, carga combustible durante tres minutos y posteriormente se retira.

## Código

```python
import simpy

def auto(env):
    print(f"El automóvil llega en el minuto {env.now}")

    yield env.timeout(3)

    print(f"El automóvil termina de cargar gasolina en el minuto {env.now}")

env = simpy.Environment()

env.process(auto(env))

env.run()
```

## Explicación

El proceso representa un automóvil.

Cuando llega a la estación se registra el tiempo.

Después espera tres minutos simulando el tiempo necesario para cargar combustible.

Al finalizar se imprime el momento en que abandona la estación.

## Salida

```
El automóvil llega en el minuto 0
El automóvil termina de cargar gasolina en el minuto 3
```

## Aplicaciones reales

Este tipo de simulaciones permite calcular:

- Tiempo promedio de atención.
- Cantidad de bombas necesarias.
- Tiempo de espera de los clientes.
- Número máximo de vehículos atendidos por día.
