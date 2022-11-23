# Patrón State

* Status: rejected
* Date: 2022-11-23

Technical Story: Seleccion del patron para seleccionar el algoritmo en función de las predicciones que se hagan

## Context and Problem Statement

Se necesita cubrir la funcionalidad de la decision de algoritmos, que se eligen mediante predicciones que el mismo algoritmo realiza

## Considered Options

* Patrón State

## Decision Outcome

Chosen option: "Patrón State"

### Positive Consequences

* Porque se ajusta a las necesidades de la arquitectura
* Porque cumple con la funcionalidad de notificar eventos
* Porque reacciona a eventos que se generan de forma no voluntaria

### Negative Consequences

* Porque cuando se producen muchos eventos simultáneos pueden surgir colapsos

## Pros and Cons of the Options

### Patrón State

* Good, because comunica eventos que surgen de forma no voluntaria.
* Good, because cumple con las partes de la arquitectura como un centro de Gestiones que seria el Gestor de Eventos, produce eventos y tiene un consumidor de eventos.
* Good, because es escalable y distribuida.
* Bad, because posibilidad de desborde.

## Links

* 0005 Decisión De Patrón Para La Elección Del Algoritmo
* 0014 Patrón Strategy
