# Estilo por capas para arquitectura IoT

* Status: rejected
* Date: 2022-11-22

## Context and Problem Statement

Necesidad de la identificación de un estilo de arquitectura para la comunicación entre sensores IoT

## Considered Options

* Estilo por capas

## Decision Outcome

Chosen option: "Estilo por capas", because acorde a los distintos tipos de sensores dentro de la familia que conocemos, pesamos que cada tipo tiene una funcionalidad muy explicita y esto lo conseguimos con el estilo por capas.

### Positive Consequences

* Porque se ajusta a las necesidades de la arquitectura
* Porque cumple con la funcionalidad de notificar eventos
* Porque reacciona a eventos que se generan de forma no voluntaria

### Negative Consequences

* Porque cuando se producen muchos eventos simultáneos pueden surgir colapsos

## Pros and Cons of the Options

### Estilo por capas

* Good, because comunica eventos que surgen de forma no voluntaria.
* Good, because cumple con las partes de la arquitectura como un centro de Gestiones que seria el Gestor de Eventos, produce eventos y tiene un consumidor de eventos.
* Good, because es escalable y distribuida.
* Bad, because posibilidad de desborde.

## Links

* 0002 Decisión De Arquitectura Iot
