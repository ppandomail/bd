# Modelo Conceptual

## Ingeniería de Software (IS)

* Es la disciplina que abarca todos los aspectos del desarrollo de software, conocido como **ciclo de vida**

### Ciclo de vida del software. Etapas

1. Comprender un problema
1. Analizarlo (Elicitación de requerimientos)
1. Diseñar una solución
1. Implementar dicha solución
1. Entregar el producto final
1. Modificar el producto por nuevos requerimientos

### Diseño de BD

* La metodología de diseño propuesta en este curso consiste en construir un modelo de datos en etapas:

1. **Diseño conceptual**: se lleva a cabo luego de la etapa de especificación de requerimientos, es independiente del SGBD a utilizar y da como resultado el esquema conceptual
1. **Diseño lógico**: tiene dos fases, una de refinamiento del esquema conceptual y otra para obtener el esquema de la BD, que depende del SGBD a utilizar. Usaremos el Modelo Relacional
1. **Diseño Físico**: es necesario tomar decisiones específicas, que tienen que ver con el SGBD específico a utilizar (índices, clusters, archivos)

  ![Proceso de Diseño de BD](img/proceso-de-diseño-de-bd.png)

* Si bien el modelado de datos forma parte de la etapa de diseño, las y los analistas no la respetaron y comenzaron a realizarlo en las etapas tempranas, como parte de la comprensión del problema, para luego refinarlo en las etapas de diseño

| Modelo | Tipo de SGBD | SGBD |
| -- | -- | -- |
| **Conceptual** | No se debe decidir | No se debe decidir |
| **Lógico**     | No se debe decidir | No se debe decidir |
| **Físico**     | No se debe decidir | No se debe decidir |

### Regla de Negocio

* Descripción breve, precisa y no ambigua de una política, procedimiento o principio dentro de una organización específica. También se la llama requisito o requerimiento
* "Las **reglas de negocio** forman parte del **Documento de Requisitos** de un sistema, que es el producto resultante de la etapa de **análisis** (elicitación de requerimientos)"
* Ejemplo:
  * "Una/un estudiante se inscribe en una carrera de la Universidad"
  * "Una cuenta corriente en pesos en el banco puede tener giro en descubierto"

## Modelo Entidad-Relación (MER)

* Modelo conceptual de BD
* "Los modelos de datos conceptuales permiten representar la información de un problema en un alto nivel de abstracción"

| Características ||
| -- | -- |
| **Expresividad** | Capturar y presentar de la mejor forma posible la semántica de los datos del problema a resolver |
| **Minimalidad**  | Cada elemento del modelo tiene una única forma de representación |
| **Formalidad**   | Requiere que cada elemento representado en el modelo sea preciso, bien definido y con una sola interpretación posible |
| **Simplicidad**  | El modelo debe ser fácil de entender por todas las personas involucradas (clientes, analistas, etc.) |

### Historia del MER

* **Peter Chen**
* Mientras trabajaba como profesor adjunto en la Escuela de Administración y Dirección de Empresas Sloan del MIT(Massachusetts Institute of Technology), publicó un documento influyente en 1976 llamado "Modelo entidad-relación: hacia una visión unificada de los datos", que posee las bases para la representación básica de las estructuras de datos que darán soporte a las BD

### ¿Qué es?

* Un diagrama entidad-relación (DER), también conocido como modelo entidad relación o ERD o ER, es un tipo de diagrama de flujo que ilustra cómo las "entidades" (personas, objetos o conceptos) se relacionan entre sí dentro de un sistema

### Constructores

* Emplea un conjunto definido de símbolos, tales como rectángulos, rombos, óvalos y líneas de conexión para representar la
interconexión de entidades, relaciones y sus atributos respectivamente

### Dominio

* Es un reflejo de la estructura gramatical del documento de requisitos y emplea sustantivos para las entidades y verbos para las relaciones (esto es así en la mayoría de los casos)

### MER - constructores básicos

* Entidades
* Relaciones entre esas entidades (interrelaciones)
* Atributos

* Tenemos la regla de negocio: "Una/un **estudiante** se ***inscribe*** en una **carrera** de la Universidad"

### Entidad

* Una cosa u objeto en el mundo real que es distinguible de todos los demás objetos". (Korn)
* En el Documento de Requisitos aparecen reflejadas "habitualmente" como **"sustantivos"**
* A cada una de las posibles ocurrencias de la entidad se la denomina **"ejemplar"**
* Tiene características o propiedades específicas - **Atributo** - que la describe
* Ejemplo:

  ```plain
  Existe un estudiante con:
    Nombre: Juan
    Apellido: Pérez
    DNI: 20.123.456 Legajo: 234569/5
    Dirección: Rivadavia 456 
    Teléfono: 236-444897
    Mail: juan_perez@gmail.com
  ```

* **Notación**: se denota con un **rectángulo**. El nombre es generalmente un sustantivo escrito en plural. Los **atributos** se denotan con **una línea y un óvalo**

  ![Entidad](img/entidad.png)

### Atributo

* Describe las características importantes de cada entidad
* Atributo = (nombre, valor) para cada entidad
* **Dominio del atributo**: es el conjunto de valores permitidos para un atributo (dominio de datos)
* **Funciones**: identificadores y descriptores
* Ejemplo:

  ```plain
  Entidad ESTUDIANTES
  Atributos: nombre, apellido, teléfono, dirección son descriptores
  Atributos: dni, legajo, mail son identificadores

  ¿Por qué? ¿Y si tengo un pasaporte como DNI porque es un estudiante de intercambio y es
  una persona extranjera?
  ```

* **Definición de Dominios**

  ||| Ejemplo |
  | -- | -- | -- |
  | **Por comprensión** | indicando el tipo de dato | precio: "números reales mayores que cero" |
  | **Por extensión**   | definiendo los valores del conjunto | sexo = {M, F, X} |

* **Tipos de datos**: Los tipos de datos básicos del estándar SQL para DBMS relaciones son:

  |||
  | -- | -- |
  | **Datos para Cadenas de caracteres** | CHAR, VARCHAR |
  | **Datos Numéricos**                  | INT, FLOAT, REAL, DECIMAL |
  | **Datos para Fechas y Horas**        | DATE, TIME, DATETIME, TIMESTAMP |
  | **Datos Booleanos**                  | BOOLEAN |

* **Clasificación (restricciones semánticas sobre los atributos)**

  ||| Ejemplo |
  | -- | -- | -- |
  | **Obligatorios u opcionales** | Define si un atributo debe o no tomar un valor. (Valores Nulos) - **Cardinalidad Mínima** | |
  | **Simples**                   | Atributos que no son divisibles | código de curso, nombre |
  | **Compuestos**                | Atributos formados por varios atributos simples | domicilio con ciudad, calle y número, CP |
  | **Univaluados o monovalentes**   | Pueden tomar solo un valor de su dominio | fecha_nac (1,1) o prepaga (0,1) |
  | **Multivaluados o polivalentes** | Toman más de un valor del dominio de datos | teléfonos (1, N), titulos (0, N) |
  | ***Derivados o calculados**      | Pueden ser calculados a partir de otros atributos | edad = fecha_actual - fecha_nac |

* **Cardinalidad de atributos**: cuántos valores del dominio puede tomar un atributo. Se denota como par ordenado (card min, card max)

  |||
  | -- | -- |
  | **Cardinalidad mínima** | 0 o 1 (u otro valor) |
  | **Cardinalidad máxima** | 1 o N (u otro valor) |
  | Por **convención** la cardinalidad de los atributos cuando es | (1,1) no se especifica en el modelo |

* **Tipos de atributos**

  ![Atributos](img/atributos.png)

* **Valores nulos**: Algunos atributos pueden no tener un valor específico para una entidad, estos atributos tendrán **valores nulos**. ¿Qué significa aceptar un valor nulo?

  ||| Ejemplo: Piso = NULL |
  | -- | -- | -- |
  | **Valor no aplicable** | no tiene sentido dar un valor de atributo para el ejemplar de la entidad | cuando es una casa |
  | **Valor perdido**      | el valor existe pero no se tiene | existe el piso pero no se sabe cual es |
  | **Valor no conocido**  | no se sabe si existe o no hat valor para el ejemplar | no se sabe si la dirección corresponde a un bloque de pisos o a una casa |

* **Atributo identificador o clave**
  * Restricción de unicidad del valor del atributo
  * Sirve para identificar de manera única a cada ejemplar de una entidad
  * Tiene que tener un valor conocido para cada entidad, no puede ser nulo

  ![ID](img/id.png)
