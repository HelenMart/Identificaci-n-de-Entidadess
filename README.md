
# Identificación de Entidades, Atributos, Dominios y Clave Primaria + Creación de Base de Datos en PostgreSQL
# Conceptos básicos de Bases de Datos
## Entidad
Una *entidad* es un objeto o cosa del mundo real sobre la que se guarda información en la base de datos.  
En el modelo de gestión de torneos deportivos, las entidades son por ejemplo: *Torneo, **Equipo, **Estadio* y *Partido*.  
En la práctica, *cada entidad corresponde a una tabla*.

---

## Atributo
Los *atributos* son las características o propiedades que describen una entidad.  
Ejemplos:  
- La entidad *Equipo* tiene atributos como: nombre_oficial, anio_fundacion, entrenador_principal.  
- La entidad *Estadio* tiene atributos como: nombre, capacidad, ubicacion.  
En la práctica, *cada atributo corresponde a una columna en la tabla*.

---

## Clave primaria (CLAVE PRIMARIA)
La *clave primaria* es un atributo (o conjunto de atributos) que identifica de manera *única* a cada registro de una tabla.  
- No se puede repetir.  
- No puede estar vacío (NULL).  

Ejemplos:  
- En *Torneo*: id_torneo.  
- En *Equipo*: id_equipo.  
- En *Estadio*: id_estadio.  

---

## Clave foránea (CLAVE EXTRANJERA)
La *clave foránea* es un atributo que sirve para *relacionar dos entidades*.  
Un registro en una tabla está vinculado a otro en otra tabla.  

Ejemplo:  
- En la tabla *Partido, el atributo id_equipo_local hace referencia al id_equipo de la tabla **Equipo*.  
- Así se sabe qué equipos jugaron, en qué estadio y en qué torneo.

---

## Dominio
El *dominio* define el *tipo de datos permitido* en un atributo.  
Ejemplos:  
- nombre_oficial → VARCHAR(100) (texto de hasta 100 caracteres).  
- anio_fundacion → INT (entero).  
- fecha_inicio → FECHA (fecha).  
- capacidad → INT CHECK (capacidad > 0) (entero, debe ser mayor que cero).  

Esto garantiza que los datos que se ingresen en la base de datos sean *válidos y consistentes*.

## Entidades y atributos EN sql

### Torneo
- *id_torneo*: Entero, clave primaria.
- *nombre*: Texto (100).
- *fecha_inicio*: Fecha.
- *fecha_fin*: Fecha.
- *ciudad_sede*: Texto (50).

### Equipo
- *id_equipo*: Entero, clave primaria.
- *nombre_oficial*: Texto (100).
- *anio_fundacion*: Entero.
- *entrenador_principal*: Texto (100).

### Estadio
- *id_estadio*: Entero, clave primaria.
- *nombre*: Texto (100).
- *capacidad*: Entero.
- *Ubicación*: Texto (100).
