# UML
Un modelo permite documentar la estrectura de un sistema antes de codificarlo. Los UML se considera una técnica que permite la específicación del sistema en todas sus fases. UML (Unified Modeling Language), es el lenguaje de modelado más utlizado para documentar y construir una perpectiva POO.
El modelado se utiliza en la construccion de de software se utliza para:
- Comunicar la estructura de un sistema complejo
- Especificar el comprtamiento que se requiere del sistema
- Comprender de forma clara lo que se va a construir 

Los UML, se componen de varios elementos gráficos para comformar un diagrama. Entre los diagramas de estructura existe el diagrama de clases donde se enfatizan los elementos que deben existir en el sistema.

## Diagrama de clases
El diagrama de clases es de tipo estático, en este se describe la estrectura del sistema basado en clases, atributos y relaciones. El objetivo de un diagrama de clases es representar las clases del sistema en su fases de análisis y diseño para su posterir refinamiento en la fase de implementación.

### Perspectiva de los los diagramas de clases:
 1. Conceptual: Representa los concetos de dominio del objeto de estudio.
 2. Especificación: Representa las interfaces y traza la estructura a modelar.
 3. Da una vista de las clases pero sin implementación.
 
 ## Elementos del diagrama de clases:
  - Clases: son la la unidad básica que traza el modelo   
  - Atributos: Son las características de la clase
  - Métodos: son las operaciones.


|    Nombre de la Clase   	|
|:----------------------:	|
|       -Atributos       	|
| +Operaciones o Métodos 	| 

## Clases abtractas:
Se representan con un rectángulo dividido en tres áreas: la parte superior que contiene el nombre de calse, el aréa central con los atributos y la parte inferior las operaciones.

|    Nombre de la Clase   |
|:----------------------:	|
| atributo: Tipo / atributo deribado|
| +Operaciones o Métodos 	| 




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
  - Públicos: Cuando se quere que sean visibles para todas las calses.
  - Privados: Cuando son visibles o accesibles par la misma clase.
  - Protegisdos: Cuado solo se pueden acceder desde la propia clase que los definen y heredan de él.

*Símbolos de modificadores de acceso*

|  Público  	| + 	|
|:---------:	|:-:	|
|  Privado  	| - 	|
| Protegido 	| # 	|
  
## Relaciones entre clases
Las relaciones entre clases indican como se comounican los objetos entre sí:
- Asociacion: conexión entre clases 
- Dependecncia: relación de uso
- Generalización: relación de herencia

## Asociación: es una de las más utilizadas e indica que hay una conexión entre tipos de objetos. Existencuatro tipos de asociaciones:
- Asociaciones bidireccionales
- Asociaciones unidireccionales 
- Autoasociación 
- Asociaciones de números múltiples

Cada una de estas se represnta con una línea que une las dos clases y tiene las siguientes caracterìsicas:
1. Nombre de la sociación: se deble establecer un nombre de forma obligtoria
2. Rol: cada clase tiene un rol asociado 
3. Navegabilidad: Establece el vínculo y se representa con una flecha unidireccional o bidireccional 
4. Multiplicidad: epresentan el número de instancias de la clase.

[![Diagrama-relacion-de-asociacion-drawio.png](https://i.postimg.cc/nLWhzQZf/Diagrama-relacion-de-asociacion-drawio.png)](https://postimg.cc/QBp3YCHf)

## Herencia:
En una relación de herencia las subclases heredan las características (atributos) y los comportamientos (métodos) de las superclases.
## Agregación:
Este tipo de relación se representa con una línea que une la clase agregada junto a sus clases componentes, del lado de la clase agregada tiene un rombo que representa la relación de agregación.

## Composición:
Este tipo de relación se representa con una línea que une la clase agregada junto a sus clases componentes, del lado de la clase agregada tiene un rombo que representa la relación de agregación.

![](https://manuel.cillero.es/wp-content/uploads/2013/11/tipos-asociacion.png)

Referencias:
https://manuel.cillero.es/doc/metodologia/metrica-3/tecnicas/diagrama-de-clases/

## Patrones de diseño:

Los patrones de diseño son un plan de acción que define una solución a un problema recurrente. Los patrones de diseño se clasifican en tres campos generales:
- *Patrones creacionales*: estos se encargan de solucionar los problemas que implican la creación de objetos y las instancias de dichos objetos en una jerarqiía de clases complejas para simplificarla y hacerla más entendible.
  - Singleton: garantiza que la clase tenga una unica instancia y un acceso global a ella.
  - Factory Method: Es un método que permite crear instancias de un objeto encasulando la creacion de dicho objeto
- *Patrones estructurales*: separan la interfaz de la implementación, se ocupan de las clases y los objetos para formar estructuras más complejas.
- *Patrones de comportamiento* : Describe los objetos y clases implicadas y la comunicación entre ellos.

     
