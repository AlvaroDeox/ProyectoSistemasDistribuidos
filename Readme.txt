Requisitos:
-JDK 12
-SPRING TOOLS SUITE
-VISUAL STUDIO CODE
-ANGULAR 10
-mariaDB
-postgresql
-mongodb

Instalacion de sistema de evalucacion online:
Instalacion de base de datos:
Mongodb:
1.crear la database: use db_microservicios_respuestas
2.Importar el script de la carpeta mongodb con la data, en caso se quisiera empezar desde cero, el microservicio usuarios, tienen la configuracion para crear las colleciones siempre que se tenga la db_microservicios_respuestas
Postgre:
1. Crear el database db_microservicios_usuarios
2. cargar los scripts que se encuentran en la carpeta postgre
MariaDB
1. Crear el database db_microservicios_examenes
2.Importar todos los scripts de la carpeta MySQL
CREATE TABLE public.alumnos (
    id bigint NOT NULL,
    apellido character varying(255),
    create_at timestamp without time zone,
    email character varying(255),
    foto oid,
    nombre character varying(255)
);

INSERT INTO alumnos (id,apellido,email,nombre) VALUES (1,'ku','jeffte.ku@gmail.com','Jeffte');
INSERT INTO alumnos (id,apellido,email,nombre) VALUES (2,'Inche',alvaro.inche@gmail.com','Alvaro');
INSERT INTO alumnos (id,apellido,email,nombre) VALUES (3,'Minchola','phiero.minchola@gmail.com','Phiero');

select * from alumnos;
delete from alumnos where nombre='xx';

Backend
1. Abrir el spring tools suite , importar de la carpeta backend todos las los microservicios
2.Para levantar cada microservicio seguir el siguiente order:
	2.0 Microservicio Eureka
	2.1 Microservicio Alumnos
	2.2 Microservicio Examenes
	2.3 Microservicio Cursos
	2.4 Microservicio Respuesta
	2.5 Microservicio Gateway
	2.6 Microservicio spring-boot-spring-security-jwt-authentication
3. Puede realizar puebras con postman para comprobar el funcionamiento de cada microservicio
	rutas : localhost:8090/api/alumnos
		localhost:8090/api/cursos
		localhost:8090/api/examenes
	Más detalle en Controllers de cada microservicio

Front end:
1.Abrir la carpeta de frontEnd
2.Abrir el power shell con la ruta especifica
3.Ejecutar el siguiente comando:
	npm install
4. Cuando alla finalizado, estara listo para levantar la aplicacion:
	//ng serve -o
	ng run serve
5.Url:
	localhost:4200