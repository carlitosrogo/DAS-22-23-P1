# Decisión de Arquitectura IoT

* Status: accepted
* Date: 2022-11-10

Technical Story: Selección de estilo de arquitectura secundaria para los sensores IoT

## Context and Problem Statement

Necesidad de la identificación de un estilo de arquitectura para la comunicación entre sensores IoT

## Considered Options

* Estilo por capas
* Estilo por pipes y filtros

## Decision Outcome

Chosen option: "Estilo por pipes y filtros", because acorde a los distintos tipos de sensores dentro de la familia que conocemos, pensamos que se adapta mejor al diseño del sistema.

### Positive Consequences

* Tiente buena escalabilidad.
* Cada filtro tiene su funcionalidad individual y si surgieran problemas serian independientes de cada filtro

### Negative Consequences

* Exite la posibilidad de perdida de memoria por colapso.

## Pros and Cons of the Options

### Estilo por capas

Consta en dividir la aplicación en capas, con la intención de que cada capa tenga un rol muy definido.

* Good, because facilidad de desarollo ya que cada miembro o equipo tiene claro el objetivo de cada capa y sólo es necesario crear una interfaz clara de comunicación entre ellas
* Good, because capacidad de testeo individual ya que al tener cada capa por separado la implementación del testing es mucho mejor
* Good, because facilita la estandarización
* Bad, because debido a que cada funcionalidad está en una capa diferente normalmente este patrón sufre de menor rendimiento
* Bad, because mala escalabilidad porque cada capa depende de la anteriror y cuando se cambia una capa debes cambiar tambien algunas funcionalidades de las anteriores

### Estilo por pipes y filtros

Esta arquitectura se centra en la transformación de los datos de entrada para obtener los datos de salida, para lograr esto se utiliza los componentes del software como tuberías y filtros, estas tuberías están conectadas con un filtro anterior y posterior

* Good, because descomposición del problema en pasos independientes
* Good, because sistemas fáciles de mantener y mejorar
* Good, because facil escalabilidad
* Bad, because no adecuados para procesamiento interactivo
* Bad, because problemas de rendimiento ya que los datos se transmiten en forma completa entre filtros
* Bad, because dificulta el manejo de errores

## Links

* 0010 Estilo Por Capas Para Arquitectura IoT
* 0011 Estilo Por Pipes And Filter Para Arquitectura IoT
