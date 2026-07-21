# Ejemplo 1: Simulación de un cliente en una tienda

## Descripción

En este ejemplo se simula la llegada de un cliente a una tienda. El cliente entra al establecimiento, realiza sus compras durante cinco minutos y posteriormente abandona la tienda.

## Código

```python
import simpy

def cliente(env):
    print(f"El cliente entra a la tienda en el minuto {env.now}")

    yield env.timeout(5)

    print(f"El cliente sale de la tienda en el minuto {env.now}")

env = simpy.Environment()

env.process(cliente(env))

env.run()
```

## Explicación

Primero se crea un entorno de simulación utilizando `Environment`.

Después se define el proceso `cliente`, el cual representa el comportamiento de una persona.

Cuando el cliente entra a la tienda se imprime el tiempo actual utilizando `env.now`.

Posteriormente el proceso espera cinco minutos mediante:

```python
yield env.timeout(5)
```

Finalmente el cliente termina sus compras y abandona la tienda.

## Salida esperada

```
El cliente entra a la tienda en el minuto 0
El cliente sale de la tienda en el minuto 5
```

## Conclusión

Este ejemplo muestra cómo SimPy controla el tiempo de la simulación sin utilizar temporizadores reales. El tiempo avanza únicamente cuando ocurre un evento.
