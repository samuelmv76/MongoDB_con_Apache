# MongoDB con Apache y PHP

## ¿Qué es MongoDB?

MongoDB es una base de datos NoSQL, orientada a documentos, que utiliza un formato de datos basado en JSON (BSON) para almacenar los registros. A diferencia de las bases de datos relacionales como MySQL, MongoDB no utiliza tablas ni filas, sino que almacena datos en documentos estructurados en colecciones. Es ideal para aplicaciones que necesitan alta disponibilidad, escalabilidad y manejan grandes volúmenes de datos no estructurados.

### Características principales de MongoDB:
- **Modelo de datos flexible**: Los documentos pueden tener diferentes estructuras.
- **Escalabilidad horizontal**: MongoDB se puede escalar fácilmente mediante "sharding" (particionado de datos).
- **Alta disponibilidad**: Ofrece replicación mediante réplicas de conjuntos.
- **Rendimiento**: Buen rendimiento en lecturas y escrituras gracias a su arquitectura orientada a documentos.

---

## Comparar MongoDB con MySQL

### 1. **Modelo de Datos**
   - **MongoDB**: Utiliza un modelo orientado a documentos. Los datos se almacenan en documentos BSON (una forma binaria de JSON), lo que permite almacenar información compleja en un solo documento.
   - **MySQL**: Utiliza un modelo relacional basado en tablas, filas y columnas.

### 2. **Escalabilidad**
   - **MongoDB**: Escalabilidad horizontal mediante "sharding", lo que permite distribuir la base de datos entre varios servidores.
   - **MySQL**: Generalmente, escalabilidad vertical (mejorando el hardware del servidor), aunque también permite replicación y particionamiento en algunas configuraciones avanzadas.

### 3. **Consistencia de Datos**
   - **MongoDB**: Ofrece consistencia eventual y tiene una configuración opcional para garantizar la consistencia.
   - **MySQL**: Proporciona una consistencia fuerte por defecto, usando transacciones ACID (Atomicidad, Consistencia, Aislamiento y Durabilidad).

### 4. **Consultas y Lenguaje**
   - **MongoDB**: Usa un lenguaje de consulta específico para MongoDB, basado en JSON, que permite consultas más flexibles sobre documentos no estructurados.
   - **MySQL**: Usa SQL (Structured Query Language), un lenguaje estándar para interactuar con bases de datos relacionales.

### 5. **Transacciones**
   - **MongoDB**: Aunque inicialmente no soportaba transacciones multi-documento, ahora permite transacciones ACID en múltiples documentos a partir de la versión 4.0.
   - **MySQL**: Soporta transacciones ACID completas de forma nativa.

### 6. **Casos de uso**
   - **MongoDB**: Ideal para aplicaciones web modernas, big data, y sistemas que manejan grandes volúmenes de datos no estructurados o semi-estructurados (como logs, redes sociales, IoT, etc.).
   - **MySQL**: Ideal para sistemas con datos estructurados y necesidades de transacciones fuertes, como aplicaciones financieras o CRM.

---

## Instalar el Controlador de MongoDB en PHP

Para utilizar MongoDB con PHP, necesitas instalar el controlador adecuado. El controlador oficial para PHP es `mongodb` y se instala mediante `pecl`.

### Pasos para instalar el controlador:

1. **Instalar `pecl` (si aún no lo tienes)**
   Si aún no tienes `pecl` instalado, puedes instalarlo siguiendo las instrucciones en [PECL Installation](https://pecl.php.net/manual/en/install.php).

2. **Instalar el controlador MongoDB**
   Para instalar el controlador MongoDB, ejecuta el siguiente comando en tu terminal:
   
   ```bash
   pecl install mongodb

---

## Paquetes para usar MongoDB en php

Extensión oficial mongodb (moderna y recomendada) 

Proporciona acceso de bajo nivel a MongoDB. 

Sustituye a la extensión obsoleta mongo. 

 

Comando instalación: sudo pecl install mongodb 

 

Doctrine MongoDB ODM 

Ofrece un ODM (Object-Document Mapper) para trabajar con documentos en MongoDB como si fueran entidades PHP. 

Requiere configuración avanzada. 

 

Comando instalación: composer require doctrine/mongodb-odm 

 

Jenssegers MongoDB para Laravel 

Un paquete que integra MongoDB con el framework Laravel. 

Extiende Eloquent para permitir consultas y operaciones en bases de datos MongoDB. 

 

Comando instalación: composer require jenssegers/mongodb 

 

 

PHPMongo ODM 

Un Object-Document Mapper (ODM) minimalista para MongoDB en PHP. 

No es tan robusto ni activo como Doctrine ODM. 

 

 

Mandango 

Un ODM alternativo para MongoDB en PHP. 

Útil para proyectos más antiguos o específicos. 

 

 

Alcaeus MongoDB Adapter 

Una capa de compatibilidad que permite usar la API de la antigua extensión mongo con la extensión moderna mongodb. 

Útil para proyectos de migración. 

 

Comando instalación: composer require alcaeus/mongo-php-adapter 

 

Laravel MongoDB Passport 

Amplía la funcionalidad del paquete de Jenssegers para usar Passport con bases de datos MongoDB. 

 

Comando instalación: composer require oscarafdev/mongodb-passport 

 

 

Simple ODM 

Un ODM ligero para MongoDB en PHP. 

Enfocado en la simplicidad. 

 

 

Monga 

Un wrapper ligero para trabajar con MongoDB. 

Proporciona un enfoque minimalista en comparación con otras herramientas. 
