# UML
Un modelo permite documentar la estructura de un sistema antes de codificarlo. Los UML se considera una técnica que permite la especificación del sistema en todas sus fases. UML (Unified Modeling Language), es el lenguaje de modelado más utilizado para documentar y construir una perspectiva POO.
El modelado se utiliza en la construcción de software se utiliza para:
- Comunicar la estructura de un sistema complejo
- Especificar el comportamiento que se requiere del sistema
- Comprender de forma clara lo que se va a construir 

Los UML, se componen de varios elementos gráficos para conformar un diagrama. Entre los diagramas de estructura existe el diagrama de clases donde se enfatizan los elementos que deben existir en el sistema.

## Diagrama de clases
El diagrama de clases es de tipo estático, en este se describe la estructura del sistema basado en clases, atributos y relaciones. El objetivo de un diagrama de clases es representar las clases del sistema en sus fases de análisis y diseño para su posterior refinamiento en la fase de implementación.

### Perspectiva de los diagramas de clases:
 1. Conceptual: Representa los concetos de dominio del objeto de estudio.
 2. Especificación: Representa las interfaces y traza la estructura a modelar.
 3. Da una vista de las clases, pero sin implementación.
 
 
 ## Elementos del diagrama de clases:
  - Clases: son la unidad básica que traza el modelo   
  - Atributos: Son las características de la clase
  - Métodos: son las operaciones, y cada una posee su propia línea.
  - Señales: Son los símbolos que representan comunicación 
  - Tipo de datos: pueden ser de tipo primitivo o enumeraciones
  - Paquetes: Se utiliza para organizar clasificadores en un diagrama
  - Interfaces: Un conjuto de atributos con comportamiento uniforme
  - Enumeraciones: Representan tipos de datos definidos
  - Objetos: Instancias de una clase
  - Artefactos : Representan la entidad concreta de un sistema

## Clases abstractas:
Se representan con un rectángulo dividido en tres áreas: la parte superior que contiene el nombre de clase, el área central con los atributos y la parte inferior las operaciones.


```mermaid
classDiagram
    Animal <|-- Duck
    Animal <|-- Fish
    Animal <|-- Zebra
    Animal : +int age
    Animal : +String gender
    Animal: +isMammal()
    Animal: +mate()
    class Duck{
      +String beakColor
      +swim()
      +quack()
    }
    class Fish{
      -int sizeInFeet
      -canEat()
    }
    class Zebra{
      +bool is_wild
      +run()
    }
    
  ```
  
 ## Control de acceso o visibilidad de los atributos o métodos:
  - Públicos: Cuando se quiere que sean visibles para todas las clases.
  - Privados: Cuando son visibles o accesibles para la misma clase.
  - Protegidos: cuando solo se pueden acceder desde la propia clase que los definen y heredan de él.
  - 

*Símbolos de modificadores de acceso*

| **Modificador** | **Símbolo** | **Tipo de acceso** |
|---|:---:|:---:|
| Público | + | Indica que see puede acceder al atributo o función desde cualquier lugar de la aplicación |
| Privado | - | Se puede acceder al atributo o función únicamente desde la misma clase |
| Protegido | # | Puede ser accedida únicamente desde la misma clase o desde las clases que hereden de ella, clases derivadas |
| Paquete | ~ |  |
| Derivado | / |  |                                                                                                 	|                                                                                                          	                                                                |
 


  
## Relaciones entre clases
Las relaciones entre clases indican como se comunican los objetos entre sí:
- Asociación: conexión entre clases 
- Dependencia: relación de uso
- Generalización: relación de herencia

## Asociación: 
Es una de las más utilizadas e indica que hay una conexión entre tipos de objetos. Existen cuatro tipos de asociaciones:
- Asociaciones bidireccionales: pueden tener dos flechas i ninguna
- Asociaciones unidireccionales: tienen una soloa flecha
- Autoasociación: tienen una soloa flecha
- Asociaciones de números múltiples: En esta relación se puede agregar un número a la línea de asociación para indicar la multiplicidad.
  - 1..1: uno a uno
  - 0..*: cero a muchos
  - 1..*:uno a muchos
  - 0..1: cero a uno
  - m..n: al menos m, como máximo n (m<=n)

Cada una de estas se representa con una línea que une las dos clases y tiene las siguientes características:
1. Nombre de la asociación: se debe establecer un nombre de forma obligatoria
2. Rol: cada clase tiene un rol asociado 
3. Navegabilidad: Establece el vínculo y se representa con una flecha unidireccional o bidireccional 
4. Multiplicidad: representa el número de instancias de la clase.


[![Diagrama-relacion-de-asociacion-drawio.png](https://i.postimg.cc/nLWhzQZf/Diagrama-relacion-de-asociacion-drawio.png)](https://postimg.cc/QBp3YCHf)

## Herencia:

En una relación de herencia las subclases heredan las características (atributos) y los comportamientos (métodos) de las superclases.

[![Diagrama-herencia-drawio.png](https://i.postimg.cc/vHTTR6jy/Diagrama-herencia-drawio.png)](https://postimg.cc/kBrqKDqY)

## Agregación:

Este tipo de relación se representa con una línea que une la clase agregada junto a sus clases componentes(composición débil), del lado de la clase agregada tiene un rombo de color blanco que representa la relación de agregación.

[![Diagrama-relacion-de-agregacion-drawio.png](https://i.postimg.cc/Jz0W4fCH/Diagrama-relacion-de-agregacion-drawio.png)](https://postimg.cc/Yh5Pdy9t)


## Composición:
Este tipo de relación se representa con una línea que une la clase agregada junto a sus clases componentes, del lado de la clase agregada tiene un rombo que representa la relación de agregación.

![](https://manuel.cillero.es/wp-content/uploads/2013/11/tipos-asociacion.png)

Referencias:
https://manuel.cillero.es/doc/metodologia/metrica-3/tecnicas/diagrama-de-clases/

## Patrones de diseño:

Los patrones de diseño son un plan de acción que define una solución a un problema recurrente. Los patrones de diseño se clasifican en tres campos generales:
- *Patrones creacionales*: estos se encargan de solucionar los problemas que implican la creación de objetos y las instancias de dichos objetos en una jerarquía de clases complejas para simplificarla y hacerla más entendible.
  - *Singleton*: garantiza que la clase tenga una única instancia y un acceso global a ella.
  - *Factory Method:* Es un método que permite crear instancias de un objeto encapsulando la creación de dicho objeto
- *Patrones estructurales*: separan la interfaz de la implementación, se ocupan de las clases y los objetos para formar estructuras más complejas.
- *Patrones de comportamiento* : Describe los objetos y clases implicadas y la comunicación entre ellos.

[![Diagrama-composicion-drawio.png](https://i.postimg.cc/W4QBbtsh/Diagrama-composicion-drawio.png)](https://postimg.cc/SXfTgS2h)

     
