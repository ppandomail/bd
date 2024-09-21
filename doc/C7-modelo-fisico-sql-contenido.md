# Modelo Físico

## Structured Query Language (SQL)

* Lenguaje para **definición** y **manipulación** de datos
* Desarrollado inicialmente en laboratorios de investigación de IBM
* Estándar desde 1986
* Es **declarativo**: se indica **qué datos** se requieren, sin especificar cómo

  |||||
  | -- | -- | -- | -- |
  | **DDL** | **Lenguaje de Definición de Datos** | permite crear y modificar el esquema de la base, tablas, restricciones, vistas, etc. | CREATE, DROP, ALTER |
  | **DML** | **Lenguaje de Manejo de Datos**     | permite consultar (selección) y actualizar datos (inserción, modificación, eliminación) | SELECT, INSERT, DELETE, UPDATE |
  | **DCL** | **Lenguaje de Control de Datos**    | permite gestionar el acceso a los datos | GRANT, REVOKE |
  | **TCL** | **Lenguaje de Control de Transacciones** | permite ejecutar varios comandos de forma simultánea como si fuera un comando atómico o indivisible | COMMIT, ROLLBACK |

## Crear o borrar una BD

| Sentencia SQL ||
| -- | -- |
| ```CREATE DATABASE nombre_bd;``` | genera una BD cuyo nombre se indica |
| ```DROP DATABASE nombre_bd;```   | elimina una BD completa (tablas y datos) |

## Operar contra Tablas de BD

| Sentencia SQL ||
| -- | -- |
| ```CREATE TABLE nombre_tabla (...);``` | genera una tabla en una BD |
| ```DROP TABLE nombre_tabla;```         | elimina una tabla del modelo |
| ```ALTER TABLE nombre_tabla (...);```  | modifica una tabla del modelo |

### Ejemplo creación tabla empresas

```sql
CREATE TABLE empresas (
  idempresa INTEGER UNSIGNED NOT NULL AUTO_INCREMENT, 
  empresa VARCHAR(100) NOT NULL,
  abreviatura VARCHAR(10) NULL,
  cuit VARCHAR(13) NULL,
  direccion VARCHAR(100) NULL,
  observaciones TEXT NULL,
  PRIMARY KEY(idempresa),
  UNIQUE INDEX empresas_index19108(empresa));
```

### Ejemplo creación tabla pacientesempresas

```sql
CREATE TABLE pacientesempresas (
  idpacienteempresa INTEGER UNSIGNED NOT NULL AUTO_INCREMENT,
  idpaciente_os INTEGER UNSIGNED NOT NULL,
  idempresa INTEGER UNSIGNED NOT NULL,
  fecha_desde DATE NOT NULL,
  fecha_hasta DATE NULL,
  PRIMARY KEY(idpacienteempresa),
  INDEX empleadosempresas_FKIndex1(idempresa),
  INDEX pacientesempresas_FKIndex2(idpaciente_os),
  FOREIGN KEY(idempresa)
    REFERENCES empresas(idempresa)
      ON DELETE RESTRICT
      ON UPDATE NO ACTION,
  FOREIGN KEY(idpaciente_os)
    REFERENCES pacientes_os(idpaciente_os)
      ON DELETE RESTRICT
      ON UPDATE NO ACTION);
```

### Ejemplo modificación tabla empresas

```sql
ALTER TABLE empresas (
  Add column razon_social VARCHAR(100) NOT NULL,
  Drop column cuit,
  Alter column direccion VARCHAR(50) NULL);
```

## Lenguaje de Manipulación de datos

### Estructura básica

```sql
SELECT lista_de_atributos
FROM lista_de_tablas
WHERE predicado
```

### Ejemplo modelos

![Modelo conceptual](img/modelo-conceptual-sql.png)

| | |
| -- | -- |
| **ALUMNOS** (idalumno, nombre, dni, idlocalidad, idcarrera)            | PK(idalumno) |
| **MATERIAS** (idmateria, nombre, año_curso, idcarrera)                 | PK(idmateria) |
| **CARRERA** (idcarrera, nombre, duración_años)                         | PK(idcarrera) |
| **INSCRIPCIONES** (idinscripcion, idalumno, idmateria, año, resultado) | PK(idinscripciones) |
| **LOCALIDADES** (idlocalidad, nombre)                                  | PK(idlocalidad) |

### Ejemplo estado de la BD en un momento particular

![Modelo físico](img/tablas-sql-1.png)
![Modelo físico](img/tablas-sql-2.png)

### Ejemplo 1: presentar todos los alumnos que figuran en la tabla Alumnos

```sql
SELECT nombre
FROM alumnos
```

| nombre |
| -- |
| García |
| Perez  |
| Gomez  |
| Pizarro |
| Castelli |
| Pettorutti |
| Montenzanti |
| Suarez |

### Ejemplo 2: presentar todos los datos de los alumnos que figuran en la tabla alumnos

```sql
SELECT idalumno, nombre, dni, idlocalidad, idcarrera 
FROM alumnos
```

o mediante operador *

```sql
SELECT *
FROM alumnos
```

### Ejemplo 3: presentar todos los alumnos que cursen la carrera cuyo código es 2

```sql
SELECT nombre
FROM alumnos
WHERE idcarrera = 2
```

| nombre |
| -- |
| Gomez  |
| Pizarro |
| Pettorutti |

### Ejemplo 4: presentar todos los alumnos que cursen la carrera cuyo código es 2 y vivan en la localidad con código 1

```sql
SELECT nombre
FROM alumnos
WHERE idcarrera = 2 AND idlocalidad = 1
```

| nombre |
| -- |
| Gomez  |
| Pizarro |

### Ejemplo 5: presentar todas las materias y el año en que se cursan

```sql
SELECT nombre, año_curso
FROM materias
```

| nombre | año_curso |
| -- | -- |
| Programación | 1 |
| Matemática   | 1 |
| IBD          | 2 |
| IS           | 2 |
| Conceptos    | 3 |
| Concurrente  | 3 |
| Fisica       | 1 |
| Quimica      | 1 |
| Organica     | 2 |
| Inorganica   | 2 |
| Contabilidad | 1 |
| Empresas     | 2 |
| Comercio     | 2 |
