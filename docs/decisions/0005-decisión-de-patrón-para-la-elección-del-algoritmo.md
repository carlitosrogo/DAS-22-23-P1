# Decisión de Patrón para la elección del algoritmo

* Status: accepted
* Date: 2022-11-17

Technical Story: Seleccion del patron para seleccionar el algoritmo en función de las predicciones que se hagan

## Context and Problem Statement

Se necesita cubrir la funcionalidad de la decision de algoritmos, que se eligen mediante predicciones que el mismo algoritmo realiza

## Considered Options

* Patron Strategy
* Patron State

## Decision Outcome

Chosen option: "Patron Strategy", because aunque tienen gran similitud state y strategy pensamos que el state es para una mayor cantidad de posibles estados, y nosotros solo tenemos dos.

### Positive Consequences

* permite aislar los detalles de implementación de un algoritmo del código que lo utiliza.
* se puede sustituir la herencia por composición.
* es posible intercambiar algoritmos usados dentro de un objeto durante el tiempo de ejecución.

### Negative Consequences

* una gran cantidad de lenguajes de programación modernos tienen un soporte de tipo funcional que te permite implementar distintas versiones de un algoritmo dentro de un grupo de funciones anónimas. Entonces puedes utilizar estas funciones exactamente como habrías utilizado los objetos de estrategia, pero sin saturar tu código con clases e interfaces adicionales.

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
