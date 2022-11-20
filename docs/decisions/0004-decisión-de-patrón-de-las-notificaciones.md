# Decisión de patrón de las notificaciones

* Status: accepted
* Date: 2022-11-14

Technical Story: Seleccion del patron acorde a la funcionalidad de notificar eventos.

## Context and Problem Statement

Se necesita hacer que los eventos que se producen sean notficados a aquellos usuarios que esten suscritos.

## Considered Options

* Patron Observer

## Decision Outcome

Chosen option: "Patron Observer", because cumple perfectamente con las necesidades y requisitos de nuestro diseño.

### Positive Consequences

* Tienen una gran independencia entre el objeto publisher y el suscriber.
* Permite añadir objetos suscriber sin tener que cambiar el objeto publisher.

### Negative Consequences

* Los usuarios pueden ser notificados de forma aleatoria.
* Existe probabilidad de perdida de datos.

## Pros and Cons of the Options

### Patron Observer

Es un patrón de diseño de comportamiento que te permite definir un mecanismo de suscripción para notificar a varios objetos sobre cualquier evento que le suceda al objeto que están observando.

* Good, because cumple con el principio open/close, que permite añadir nuevos tipos de subscriptor sin cambiar la clase notificadora.
* Good, because el diseño es acoplado donde los objetos que interactuan no conocen mucho del otro.
* Bad, because los usuarios son notificados de forma aleatoria.
* Bad, because puede haber perdidas de memoria.
