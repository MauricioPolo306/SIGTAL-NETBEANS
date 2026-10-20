# Sistema Integral de Gestión para Taller Automotriz Londoño (SIGTAL)



## 1. Descripción del proyecto



SIGTAL es una aplicación web desarrollada para apoyar la gestión de las operaciones de un taller automotriz. El proyecto busca centralizar la información y facilitar la administración de los clientes, los vehículos, el inventario y la facturación.



El sistema contempla los siguientes módulos:



- Inicio de sesión.

- Dashboard.

- Clientes y Vehículos.

- Inventario.

- Facturación.

- Reportes.

- Configuración.



La disponibilidad y el alcance funcional de cada módulo deben verificarse en la versión desplegada de la aplicación.



## 2. Tecnologías utilizadas



Las principales tecnologías y herramientas utilizadas en el proyecto son:



- Java 21.

- Maven para la compilación y generación del paquete de despliegue.

- MariaDB como sistema gestor de bases de datos.

- Apache Tomcat como servidor de aplicaciones web.

- NetBeans como entorno de desarrollo.

- Git para el control de versiones.

- GitHub para alojar el repositorio remoto.

- XAMPP para administrar el entorno local de base de datos y los servicios necesarios.



## 3. Requisitos previos



Antes de ejecutar el proyecto, se recomienda disponer de:



1. JDK 21 instalado y configurado.

2. Apache NetBeans con soporte para proyectos Maven.

3. Apache Tomcat compatible con la aplicación.

4. XAMPP con MariaDB iniciado.

5. Git instalado.

6. Una base de datos `sigtal` con la estructura necesaria para la aplicación.



Las versiones concretas de las herramientas deben comprobarse en el entorno donde se realizará la instalación.



## 4. Obtener el código fuente


El repositorio oficial del proyecto es:



https://github.com/MauricioPolo306/SIGTAL-NETBEANS



Para clonar el repositorio, ejecutar:



git clone https://github.com/MauricioPolo306/SIGTAL-NETBEANS.git



Ingresar en la carpeta del proyecto:



cd SIGTAL-NETBEANS



La rama de entrega es main.



## 5. Configuración de la base de datos



La aplicación utiliza una conexión JDBC con MariaDB.



La configuración de conexión se encuentra en la clase:



src/main/java/com/mycompany/sigtal/util/ConexionBD.java

La configuración local utilizada actualmente es:



- Servidor: localhost

- Puerto: 3306

- Base de datos: sigtal

- Usuario: root

- Contraseña: vacía en el entorno local actual



**Importante:** esta configuración corresponde al entorno local de desarrollo. No debe trasladarse sin revisión a un entorno de producción.



Para preparar la base de datos:



1. Iniciar MySQL/MariaDB desde XAMPP.

2. Abrir phpMyAdmin.

3. Crear o seleccionar la base de datos `sigtal`.

4. Importar el respaldo SQL del proyecto, si está disponible.

5. Verificar que existan las tablas y columnas requeridas por el código.

6. Confirmar que los datos de conexión de `ConexionBD.java` coincidan con el entorno.



No se incluye aquí un script SQL de creación porque debe utilizarse el esquema real del proyecto.



## 6. Compilación del proyecto

Abrir una terminal en la carpeta raíz del proyecto, donde se encuentra `pom.xml`.



Ejecutar:



mvn clean package



En el entorno de desarrollo utilizado, Maven también puede ejecutarse desde PowerShell con su ruta de instalación:



& "C:\\Users\\User\\Downloads\\netbeans\\java\\maven\\bin\\mvn.cmd" clean package





Si la compilación termina correctamente, Maven mostrará:



BUILD SUCCESS



El archivo WAR se genera en: target/SIGTAL.war



## 7. Ejecución y despliegue



Para ejecutar la aplicación desde NetBeans:



1. Abrir el proyecto `SIGTAL NETBEANS`.

2. Verificar la configuración del servidor Tomcat.

3. Confirmar que MariaDB esté iniciado.

4. Ejecutar \*\*Clean and Build Project\*\*.

5. Ejecutar \*\*Run Project\*\*.

6. Comprobar que la aplicación abra en el navegador.

7. Probar las operaciones de los módulos implementados.



También puede desplegarse el archivo target/SIGTAL.war en una instalación compatible de Apache Tomcat.



La URL de acceso dependerá del nombre del contexto configurado en el servidor.



## 8. Pruebas y validación

La validación del proyecto debe incluir, como mínimo:



- Comprobación de que la aplicación se inicia.

- Verificación de la conexión con la base de datos.

- Prueba de acceso al sistema, si el módulo de autenticación está configurado.

- Registro y consulta de clientes.

- Registro y consulta de vehículos.

- Registro y consulta de productos de inventario.

- Registro y consulta de facturas.

- Verificación de los detalles de cada factura.

- Comprobación de los reportes implementados.



Las pruebas deben ejecutarse en el entorno de destino y documentarse con sus resultados.



En la última compilación registrada durante el desarrollo se obtuvo `BUILD SUCCESS`. Maven informó que no había pruebas automatizadas para ejecutar, por lo que ese resultado confirma la compilación, pero no sustituye las pruebas funcionales.



## 9. Control de versiones



El proyecto utiliza Git para registrar los cambios del código fuente.



Repositorio remoto:



https://github.com/MauricioPolo306/SIGTAL-NETBEANS



Rama de entrega: main



Para consultar el estado del repositorio:



git status



Para consultar el último commit:



git rev-parse HEAD



Antes de publicar nuevos cambios, se recomienda revisar los archivos modificados y evitar incluir credenciales, archivos privados o artefactos innecesarios.



## 10. Archivos excluidos del repositorio



El archivo .gitignore debe excluir los artefactos de compilación, archivos privados del entorno de desarrollo, archivos temporales, registros y archivos locales que no deban versionarse.



Entre las exclusiones previstas se encuentran:



- target/

- nbproject/private/

- .env

- .env.*

- Archivos de registros y temporales



Las exclusiones deben revisarse para evitar publicar credenciales o información sensible.



## 11. Consideraciones de seguridad

- No publicar contraseñas ni credenciales reales en el repositorio.

- No utilizar cuentas sin contraseña en entornos de producción.

- Configurar usuarios con permisos mínimos necesarios para la aplicación.

- Mantener copias de seguridad de la base de datos.

- Verificar las versiones y la configuración del servidor antes de desplegar.

- Validar las entradas del usuario y el manejo de errores.



## 12. Estado del proyecto



En la verificación realizada durante el desarrollo se confirmó que el proyecto compiló correctamente mediante Maven y generó el archivo target/SIGTAL.war.



El repositorio local se encontraba sincronizado con la rama remota main.



La funcionalidad de cada módulo debe evaluarse mediante las pruebas correspondientes y no únicamente mediante la compilación.



## 13. Autoría y propósito académico



Proyecto desarrollado como parte del proceso de formación en Análisis y Desarrollo de Software.



Nombre del proyecto: **Sistema Integral de Gestión para Taller Automotriz Londoño (SIGTAL)**.

