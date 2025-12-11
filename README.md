# MOD_6_INDIVIDUAL_3



M6_AE3_ABP-Ejercicio individual[Actividad Evaluada]


Ejercicio individual
Contexto

Estás desarrollando una aplicación para una pequeña biblioteca que necesita llevar el control de su inventario de libros y autores. El cliente quiere poder consultar, registrar, actualizar y eliminar libros, así como asociar cada libro con un autor. Deberás implementar dos mecanismos distintos de acceso a datos: uno con JdbcTemplate y otro con JPA, y manejarás transacciones en las operaciones de servicio para asegurar consistencia de datos.

Instrucciones

1. Configuración inicial

Crea un proyecto Spring Boot en STS que incluya:

spring-boot-starter-jdbc

spring-boot-starter-data-jpa

Driver de base de datos (por ejemplo, H2 o MySQL)

Configura en application.properties el DataSource, spring.jpa y la estrategia de inicialización.

2. Módulo JDBC Template

Crea la tabla libros directamente en la base de datos.

Crea una clase Libro con los campos: id, titulo, anioPublicacion.

Implementa un LibroDAO que utilice JdbcTemplate:

Método para insertar un nuevo libro

Método para consultar todos los libros

Método para consultar por año

Método para actualizar título

Método para eliminar un libro

Usa RowMapper para mapear los resultados a objetos Libro.

Crea un servicio LibroServiceJdbc que invoque este DAO.

3. Módulo JPA

Crea las clases Libro y Autor como entidades JPA, con una relación @ManyToOne (un autor puede tener muchos libros).

Crea un LibroRepository y un AutorRepository usando JpaRepository.

Implementa métodos para:

Guardar un nuevo autor

Guardar un libro asociado a un autor

Consultar todos los libros con sus autores

Eliminar un libro

Actualizar el nombre de un autor

Crea un servicio LibroServiceJpa que invoque a estos repositorios.

4. Transaccionalidad

Crea una operación que:

Registre un autor

Registre un libro con ese autor

Marca el servicio con @Transactional y documenta qué pasaría si ocurre un error a mitad del proceso.

5. Validaciones y pruebas

Verifica la creación de datos con ambos métodos (JdbcTemplate y JPA).

Agrega validaciones básicas (por ejemplo: que no se pueda guardar un libro sin título).

Escribe una prueba simple con @SpringBootTest que valide la operación transaccional.

Entrega

Archivo zip o enlace a Github con el código.
Duración: 1 jornada de clases.
Ejecución: Individual.
