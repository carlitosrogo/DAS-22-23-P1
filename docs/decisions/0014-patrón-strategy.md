# Patrón Strategy

* Status: accepted
* Date: 2022-11-23

Technical Story: Seleccion del patron para seleccionar el algoritmo en función de las predicciones que se hagan

## Context and Problem Statement

Se necesita cubrir la funcionalidad de la decision de algoritmos, que se eligen mediante predicciones que el mismo algoritmo realiza

## Considered Options

* Patron Strategy

## Decision Outcome

Chosen option: "Patron Strategy", because aunque tienen gran similitud state y strategy pensamos que el state es para una mayor cantidad de posibles estados, y nosotros solo tenemos dos.

### Positive Consequences

* permite aislar los detalles de implementación de un algoritmo del código que lo utiliza.
* se puede sustituir la herencia por composición.
* es posible intercambiar algoritmos usados dentro de un objeto durante el tiempo de ejecución.

### Negative Consequences

* una gran cantidad de lenguajes de programación modernos tienen un soporte de tipo funcional que te permite implementar distintas versiones de un algoritmo dentro de un grupo de funciones anónimas. Entonces puedes utilizar estas funciones exactamente como habrías utilizado los objetos de estrategia, pero sin saturar tu código con clases e interfaces adicionales.

## Links

* 0015 Patrón State
* 0005 Decisión De Patrón Para La Elección Del Algoritmo
