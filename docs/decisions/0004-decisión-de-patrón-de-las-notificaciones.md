# Decisión de patrón de las notificaciones

* Status: proposed
* Date: 2022-11-14

Technical Story: Seleccion del patron acorde a la funcionalidad de notificar eventos.

## Context and Problem Statement

Se necesita hacer que los eventos que se producen sean notficados a aquellos usuarios que esten suscritos.

## Considered Options

* Patron Observer

## Decision Outcome

Chosen option: "", because comes out best.

## Pros and Cons of the Options

### Patron Observer

Es un patrón de diseño de comportamiento que te permite definir un mecanismo de suscripción para notificar a varios objetos sobre cualquier evento que le suceda al objeto que están observando.

* Good, because cumple con el principio open/close, que permite añadir nuevos tipos de subscriptor sin cambiar la clase notificadora.
* Good, because el diseño es acoplado donde los objetos que interactuan no conocen mucho del otro.
* Bad, because los usuarios son notificados de forma aleatoria.
* Bad, because puede haber perdidas de memoria.
