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

* cumple con el principio de responsabilidad única.
* principio de open/close. Introduce nuevos estados sin cambiar clases de estado existentes o la clase contexto.
* simplifica el código del contexto eliminando voluminosos condicionales de máquina de estados

### Negative Consequences

* aplicar el patrón puede resultar excesivo si una máquina de estados sólo tiene unos pocos estados o raramente cambia
