# ¿Qué es SimPy?

## Introducción

SimPy es una biblioteca (librería) de Python diseñada para crear simulaciones de eventos discretos. Un evento discreto es un cambio que ocurre en un momento específico del tiempo, por ejemplo, la llegada de un cliente a una tienda, el inicio de una reparación o la salida de un vehículo de una estación de servicio.

Con SimPy es posible representar el comportamiento de sistemas reales sin necesidad de construirlos físicamente. Esto permite analizar diferentes escenarios, detectar problemas y mejorar procesos antes de implementarlos.

La biblioteca utiliza un entorno de simulación que controla el tiempo y coordina la ejecución de los procesos definidos por el programador.

---

# ¿Para qué sirve?

SimPy es utilizada para modelar sistemas donde existen recursos limitados y procesos que ocurren con el paso del tiempo.

Algunas aplicaciones son:

- Simulación de bancos.
- Hospitales y salas de espera.
- Supermercados.
- Aeropuertos.
- Líneas de producción.
- Redes de computadoras.
- Sistemas de transporte.
- Centros de atención telefónica.

---

# Características

Entre las principales características de SimPy se encuentran:

- Es gratuita y de código abierto.
- Está escrita completamente en Python.
- Es fácil de aprender.
- Permite controlar el tiempo de la simulación.
- Maneja recursos limitados como empleados, máquinas o cajas de pago.
- Puede simular cientos o miles de procesos al mismo tiempo.

---

# Conceptos principales

## Environment

Es el entorno donde ocurre toda la simulación. Controla el tiempo y ejecuta los procesos.

```python
env = simpy.Environment()
```

---

## Process

Representa una actividad que sucede durante la simulación.

Ejemplos:

- Un cliente.
- Un automóvil.
- Una máquina.
- Un trabajador.

Los procesos normalmente utilizan la instrucción:

```python
yield env.timeout(tiempo)
```

para indicar cuánto tiempo tarda una actividad.

---

## Timeout

Sirve para hacer que un proceso espere una determinada cantidad de tiempo.

Ejemplo:

```python
yield env.timeout(5)
```

Significa que el proceso esperará cinco unidades de tiempo antes de continuar.

---

## Resource

Representa un recurso limitado.

Por ejemplo:

- Una caja registradora.
- Un cajero.
- Una bomba de gasolina.
- Una impresora.

Cuando un recurso está ocupado, los demás procesos deben esperar.

---

# Instalación

Para instalar SimPy se utiliza el siguiente comando:

```bash
pip install simpy
```

---

# Ventajas

- Reduce costos al evitar pruebas reales.
- Permite experimentar sin riesgos.
- Ayuda a optimizar procesos.
- Facilita la toma de decisiones.
- Es ampliamente utilizada en investigación y empresas.

---

# Conclusión

SimPy es una herramienta muy útil para representar situaciones reales mediante simulaciones de eventos discretos. Gracias a esta biblioteca es posible estudiar el comportamiento de sistemas complejos, analizar tiempos de espera, utilización de recursos y mejorar la eficiencia antes de implementar un sistema en la vida real.
