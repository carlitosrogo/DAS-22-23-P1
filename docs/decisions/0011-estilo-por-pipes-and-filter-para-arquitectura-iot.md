# Estilo por Pipes and Filter para Arquitectura IoT

* Status: accepted
* Date: 2022-11-22

## Context and Problem Statement

Necesidad de la identificación de un estilo de arquitectura para la comunicación entre sensores IoT

## Considered Options

* Estilo por Pipes And Filter

## Decision Outcome

Chosen option: "Estilo por Pipes And Filter", because acorde a los distintos tipos de sensores dentro de la familia que conocemos, pensamos que se adapta mejor al diseño del sistema.

### Positive Consequences

* Porque se ajusta a las necesidades de la arquitectura
* Porque cumple con la funcionalidad de notificar eventos
* Porque reacciona a eventos que se generan de forma no voluntaria

### Negative Consequences

* Porque cuando se producen muchos eventos simultáneos pueden surgir colapsos

## Pros and Cons of the Options

### Estilo por Pipes And Filter

* Good, because comunica eventos que surgen de forma no voluntaria.
* Good, because cumple con las partes de la arquitectura como un centro de Gestiones que seria el Gestor de Eventos, produce eventos y tiene un consumidor de eventos.
* Good, because es escalable y distribuida.
* Bad, because posibilidad de desborde.

## Links

* 0002 Decisión De Arquitectura Iot
* 0010 Estilo Por Capas Para Arquitectura IoT
