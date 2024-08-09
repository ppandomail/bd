# Modelo Lógico Fase I - Transformación al MR

## Transformación de Entidades

* **Todas** las **entidades** del DER reestructurado se transforman a **tablas**
* Los **atributos identificadores** del DER serán ahora **CK**: ÚNICAS Y NO NULAS
* **Todos los atributos permiten nulos por defecto**, si no se indica lo contrario. Para **fines prácticos**, cuando lo resolvamos en un documento de texto, supondremos que no permiten nulos por defecto, y aclararemos cuando sí lo permitan
* A cada tabla se le agrega una **clave subrogada (ID)**: número entero autoincrementable, único y no nulo y será la PK de la tabla. **Notación**: PK(nombre), CS(nombre)

  ![Transformación de Entidades](img/transf-entidades.png)

  **empleado** (idemp, dni, cuil, nombre, direccion)
  PK (idemp) CS(idpemp) CK (dni) CK(cuil)

  **departamento** (iddepto, codigo, nombre)
  PK (idedepto) CS(iddepto) CK (codigo)

## Transformación de Relaciones N:N
