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
  

