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







Los paquetes de MongoDB para PHP son bibliotecas que permiten que una aplicación escrita en PHP interactúe con bases de datos MongoDB. MongoDB es una base de datos NoSQL que almacena los datos en formato de documentos BSON (similar a JSON), lo que permite una gran flexibilidad y escalabilidad.

Al utilizar estos paquetes, los desarrolladores de PHP pueden realizar operaciones comunes en MongoDB, tales como:

1. **Conexión a la base de datos**: Establecer una conexión entre la aplicación PHP y el servidor MongoDB.
   
2. **CRUD (Crear, Leer, Actualizar, Eliminar)**: Permitir la creación, lectura, actualización y eliminación de documentos en las colecciones de MongoDB desde una aplicación PHP.

3. **Consultas avanzadas**: Realizar consultas complejas sobre los datos almacenados, como filtros, ordenamientos, proyecciones y agrupamientos.

4. **Manejo de índices**: Crear y gestionar índices en las colecciones para mejorar el rendimiento de las consultas.

5. **Gestión de sesiones y transacciones**: En versiones recientes, MongoDB permite realizar transacciones que se pueden utilizar para asegurar la consistencia en operaciones complejas.

6. **Funciones adicionales**: Los paquetes también proporcionan soporte para la administración de bases de datos, como la creación y eliminación de colecciones o bases de datos, y el manejo de errores.

### Paquetes principales

- **MongoDB PHP Driver**: Es el paquete básico que permite la comunicación con el servidor MongoDB. Este driver ofrece las funciones para realizar todas las operaciones esenciales como conectarse al servidor, ejecutar consultas y manejar la base de datos.

- **MongoDB ODM (Object Document Mapper)**: Es una capa adicional que facilita la integración de MongoDB con objetos PHP, permitiendo trabajar con documentos MongoDB como si fueran objetos PHP, lo cual es útil para trabajar con frameworks como Symfony o Laravel.

### Instalación

Para instalar el paquete oficial del driver de MongoDB para PHP, normalmente se usa Composer, que es el gestor de dependencias en PHP. Un ejemplo de comando para instalar el driver:

```bash
composer require mongodb/mongodb
```

Esto instalará la última versión del driver de MongoDB, y se podrá utilizar en tu aplicación PHP.

En resumen, los paquetes de MongoDB para PHP permiten a los desarrolladores interactuar eficientemente con MongoDB, aprovechando sus características de escalabilidad y flexibilidad, mientras se integran fácilmente en aplicaciones PHP.
-------------------------------------------------------
-------------------------------------------------------

Ejemplo de JSON
json
Copiar código
{
  "nombre": "Juan",
  "edad": 30,
  "esEmpleado": true,
  "hobbies": ["leer", "correr", "programar"],
  "direccion": {
    "calle": "Calle Falsa",
    "numero": 123,
    "ciudad": "Madrid",
    "codigoPostal": "28013"
  }
}
Ejemplo de BSON
El BSON (Binary JSON) no se puede mostrar directamente como un archivo de texto porque es una representación binaria. Sin embargo, su estructura sería equivalente al JSON anterior. Así se vería su contenido conceptual:

arduino
Copiar código
\x16\x00\x00\x00                      // tamaño del documento en bytes
\x02nombre\x00\x05\x00\x00\x00Juan\x00 // campo "nombre" con tipo cadena
\x10edad\x00\x1E\x00\x00\x00          // campo "edad" con tipo entero
\x08esEmpleado\x00\x01                // campo "esEmpleado" con tipo booleano
\x04hobbies\x00                       // campo "hobbies" con tipo array
  \x2F\x00\x00\x00                    // tamaño del array en bytes
  \x02\x30\x00\x05\x00\x00\x00leer\x00 // elemento 0
  \x02\x31\x00\x06\x00\x00\x00correr\x00 // elemento 1
  \x02\x32\x00\x0A\x00\x00\x00programar\x00 // elemento 2
  \x00                                // fin del array
\x03direccion\x00                     // subdocumento "direccion"
  \x28\x00\x00\x00                    // tamaño del subdocumento
  \x02calle\x00\x0B\x00\x00\x00Calle Falsa\x00
  \x10numero\x00\x7B\x00\x00\x00      // número 123
  \x02ciudad\x00\x06\x00\x00\x00Madrid\x00
  \x02codigoPostal\x00\x06\x00\x00\x0028013\x00
  \x00                                // fin del subdocumento
\x00                                  // fin del documento
Diferencias clave:
JSON es un formato basado en texto, fácil de leer y escribir.
BSON es un formato binario, más eficiente para almacenamiento y transmisión, pero no legible directamente por humanos.
BSON incluye información de longitud y tipos explícitos, lo que lo hace más rápido para ciertas operaciones.
