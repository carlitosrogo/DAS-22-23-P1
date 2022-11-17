# Decisión de patrón para el centro de notificaciones

* Status: proposed
* Date: 2022-11-17

Technical Story: Selecionar el patron adecuado para cumplir con la funcionalidad el centro de notificaciones

## Context and Problem Statement

Se necesita que el centro de notificaciones gestione todas las funcionalidades del software

## Considered Options

* Patron Mediator

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### Patron Mediator

Es un patrón de diseño de comportamiento que te permite reducir las dependencias caóticas entre objetos. El patrón restringe las comunicaciones directas entre los objetos, forzándolos a colaborar únicamente a través de un objeto mediador.

* Good, because cumple con el principio de responsabilidad única. Puedes extraer las comunicaciones entre varios componentes dentro de un único sitio, haciéndolo más fácil de comprender y mantener.
* Good, because cumple con el principio de open/close. Puedes introducir nuevos mediadores sin tener que cambiar los propios componentes..
* Good, because se puede reducir el acoplamiento entre varios componentes de un programa
* Good, because permite reutilizar componentes individuales con mayor facilidad.
* Bad, because con el tiempo, un mediador puede evolucionar a un objeto todopoderoso.
