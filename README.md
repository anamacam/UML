# UML
Un modelo permite documentar la estructura de un sistema antes de codificarlo. Los UML se considera una técnica que permite la especificación del sistema en todas sus fases. UML (Unified Modeling Language), es el lenguaje de modelado más utilizado para documentar y construir una perspectiva POO.
El modelado se utiliza en la construcción de software se utiliza para:
- Comunicar la estructura de un sistema complejo
- Especificar el comportamiento que se requiere del sistema
- Comprender de forma clara lo que se va a construir 

Los UML, se componen de varios elementos gráficos para conformar un diagrama. Entre los diagramas de estructura existe el diagrama de clases donde se enfatizan los elementos que deben existir en el sistema.

## Diagrama de clases:

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
  
*Símbolos de modificadores de acceso*


| **Modificador** | **Símbolo** | **Tipo de acceso** |
|---|:---:|:---:|
| Público | + | Indica que see puede acceder al atributo o función desde cualquier lugar de la aplicación |
| Privado | - | Se puede acceder al atributo o función únicamente desde la misma clase |
| Protegido | # | Puede ser accedida únicamente desde la misma clase o desde las clases que hereden de ella, clases derivadas |
| Paquete | ~ |  |
| Derivado | / |  |                                                                                                 	|                                                                                                          	                                                                |
 
## Clases abstractas:

- Tienen miemboros abtractos
  - Deben ser implimentados en las clases deribadas:
- Obligan:
  - Herencia
- Se representan:
  - Con letras itálicas
- No permiten :
  - Instancias o crear objetos de ellas
- Permiten:
   - Declarar variables y constantes
   - Implementar métodos y propiedades
  - Heredar :
    - Otras Calses
    - Interfases 
   
Se representan con un rectángulo dividido en tres áreas: la parte superior que contiene el nombre de clase, el área central con los atributos y la parte inferior las operaciones.


[![Diagrama-clases-abtractas-drawio.png](https://i.postimg.cc/v8ks1XMS/Diagrama-clases-abtractas-drawio.png)](https://postimg.cc/Z08g28Wr)

  
## Relaciones entre clases:

Las relaciones entre clases indican como se comunican los objetos entre sí:
- Asociación: conexión entre clases 
- Dependencia: relación de uso
- Generalización: relación de herencia

## 1. Asociación: 

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

## 2. Herencia:

En una relación de herencia las subclases heredan las características (atributos) y los comportamientos (métodos) de las superclases.


[![Diagrama-herencia-drawio.png](https://i.postimg.cc/vHTTR6jy/Diagrama-herencia-drawio.png)](https://postimg.cc/kBrqKDqY)


## 3. Agregación:

Este tipo de relación se representa con una línea que une la clase agregada junto a sus clases componentes(composición débil), del lado de la clase agregada tiene un rombo de color blanco que representa la relación de agregación.

[![Diagrama-relacion-de-agregacion-drawio.png](https://i.postimg.cc/Jz0W4fCH/Diagrama-relacion-de-agregacion-drawio.png)](https://postimg.cc/Yh5Pdy9t)


## 4. Composición:

Este tipo de relación se representa con una línea que une la clase agregada junto a sus clases componentes, del lado de la clase agregada tiene un rombo que representa la relación de agregación.


[![Diagrama-composicion-drawio.png](https://i.postimg.cc/RhM44qTw/Diagrama-composicion-drawio.png)](https://postimg.cc/YGyJxrZS)


## Diferencias entre Composición y Agregación

| **Agregación** | **Composición** |
|---|:---:|
| Un subconjunto de las asociaciones | Un subconjunto de la agregación  |
| Un tipo de Asociación débil | Un tipo de asociación fuerte |
| Los objetos enlazados son  indepentientes entre sí. | Los objetos enlazados son  altamente depentientes entre sí |
| Se representan con una línea sólida y una ponta de flacha vacía | Es representado por una línea sólida con una punta de flecha rellena |
| La agregación se define como  una relación "tiene-un" | La composición se define como una relación "parte-de" |

## 5. Realización / Implementación :

Es ta relacionada con la relación entre interfaces y las clases de implementación

[![Diagrama-implementcion-drawio.png](https://i.postimg.cc/mgKxky9y/Diagrama-implementcion-drawio.png)](https://postimg.cc/4Yv2FtBY)

## 6. Relación de dependencias:

Las dependecias se reflejan en una relación de uso, un cambio afectará las otras clases que dependan de estas.

[![Diagrama-dependecia-drawio.png](https://i.postimg.cc/Z5x3KV21/Diagrama-dependecia-drawio.png)](https://postimg.cc/4YnnWbJ5)



Referencias:

Diagrama de Clases

https://manuel.cillero.es/doc/metodologia/metrica-3/tecnicas/diagrama-de-clases/

La comparación entre UML Asociación, Agregación y Composición

https://www.edrawsoft.com/es/article/uml-aggregation-vs-composition.html

Curso de programación orientado a objetos

http://www.itnuevolaredo.edu.mx/takeyas/apuntes/poo/Apuntes/04.-%20Clases%20Abstractas%20e%20Interfaces.pdf

¿Cuáles Son Los Seis Tipos De Relaciones En Los Diagramas De Clases UML?

https://blog.visual-paradigm.com/es/what-are-the-six-types-of-relationships-in-uml-class-diagrams/


     
