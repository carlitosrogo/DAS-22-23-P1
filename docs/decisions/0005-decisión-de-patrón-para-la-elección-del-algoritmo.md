# Decisión de Patrón para la elección del algoritmo

* Status: proposed
* Date: 2022-11-17

Technical Story: Seleccion del patron para seleccionar el algoritmo en función de las predicciones que se hagan

## Context and Problem Statement

Se necesita cubrir la funcionalidad de la decision de algoritmos, que se eligen mediante predicciones que el mismo algoritmo realiza

## Considered Options

* Patron Strategy
* Patron State

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### Patron Strategy

Es un patrón de diseño de comportamiento que te permite definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables.

* Good, because permite que durante la ejecucion se intercambien los distintos algoritmos que se pueden usar.
* Good, because principio de open/close. Puedes introducir nuevas estrategias sin tener que cambiar el contexto.
* Good, because permite aislar los detalles de las implementaciones de los algoritmos que se utilizan
* Bad, because en caso de tener algoritmos que raramente cambian, puede complicar el programa mas de lo necesario

### Patron State

Es un patrón de diseño de comportamiento que permite a un objeto alterar su comportamiento cuando su estado interno cambia. Parece como si el objeto cambiara su clase.

* Good, because cumple con el principio de responsabilidad única.
* Good, because principio de open/close. Introduce nuevos estados sin cambiar clases de estado existentes o la clase contexto.
* Good, because simplifica el código del contexto eliminando voluminosos condicionales de máquina de estados
* Bad, because aplicar el patrón puede resultar excesivo si una máquina de estados sólo tiene unos pocos estados o raramente cambia
