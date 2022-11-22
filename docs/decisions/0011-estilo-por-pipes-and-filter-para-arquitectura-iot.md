# Estilo por Pipes and Filter para Arquitectura IoT

* Status: rejected
* Date: 2022-11-22

## Context and Problem Statement

Necesidad de la identificación de un estilo de arquitectura para la comunicación entre sensores IoT

## Considered Options

* Estilo por Pipes And Filter

## Decision Outcome

Chosen option: "Estilo por Pipes And Filter"

### Positive Consequences

* descomposición del problema en pasos independientes
* sistemas fáciles de mantener y mejorar
* facil escalabilidad

### Negative Consequences

* no adecuados para procesamiento interactivo
* problemas de rendimiento ya que los datos se transmiten en forma completa entre filtros
* dificulta el manejo de errores
