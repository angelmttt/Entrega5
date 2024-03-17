6.1. El primer proyecto de Maven Ejercicio 18. Responda las siguientes preguntas:

1. ¿Qué es Maven? Maven es una herramienta de gestión de proyectos de software que se utiliza principalmente para proyectos basados ​​en Java. Facilita la creación, la gestión de dependencias y la generación de informes. Maven utiliza un formato de proyecto estándar, un archivo de configuración XML (pom.xml) y proporciona un directorio predefinido para construir un proyecto.

2. ¿Cuál es el repositorio central de Maven?, ¿hasta qué punto son fiables las bibliotecas que hay en él? El Repositorio Central de Maven es un repositorio en línea que almacena bibliotecas de software y artefactos que pueden usarse como dependencias en proyectos de Maven. Este repositorio es mantenido por la comunidad Maven y contiene una amplia variedad de bibliotecas propietarias y de código abierto. En general, las bibliotecas del repositorio de Maven son bastante confiables, ya que están sujetas a ciertas políticas y procedimientos de calidad definidos por la comunidad Maven. Sin embargo, siempre es importante comprobar la reputación y la calidad de las bibliotecas antes de incluirlas en un proyecto.

3. ¿Qué es un repositorio local? Un repositorio local es un directorio en el sistema de archivos del desarrollador donde Maven almacena las dependencias descargadas localmente desde un repositorio central u otro repositorio remoto. Cuando Maven necesita una dependencia para construir un proyecto, primero verifica si está disponible en el repositorio local. Si no se encuentra, lo descarga desde el repositorio remoto y lo almacena en el repositorio local para uso futuro. Este repositorio local permite que Maven se ejecute de manera más eficiente al evitar la necesidad de descargar las mismas dependencias varias veces y también proporciona más independencia para el desarrollo cuando no hay conexión a Internet.

Ejercicio 19. Instale Maven. Por ejemplo, en OpenSuse, ejecute:sudo zypper install maven Para asegurarse de que esté instalado correctamente:mvn --version

Ejercicio 20. Complete las siguientes secciones:

1. Cree un proyecto en Maven ejecutando la siguiente instrucción1: mvn archetype:generate -DgroupId=org.pr2 -DartifactId=miPrimeraAplicacion -DarchetypeArtifactId=maven-archetype-quickstart -DarchetypeVersion=1.4 -DinteractiveMode=falsey explore el árbol de directorios generado.

2. ¿Qué es un arquetipo maven? Un arquetipo de Maven es una plantilla predefinida para crear nuevos proyectos que facilita el inicio del desarrollo con una estructura y configuración inicial.

3. Ingrese a la carpeta miPrimeraAplicacion: cdmiPrimeraAplicacion

4. Explique pom.xml: archivo Pom. xml es un archivo de configuración para Maven, un sistema de gestión de proyectos utilizado principalmente para proyectos Java. Maven usa este archivo para administrar las dependencias del proyecto, configurar los ajustes del proyecto y otras configuraciones importantes. Algunos de los elementos son: Este es el elemento raíz del archivo pom.xml y contiene todas las configuraciones del proyecto. : Indica la versión del Modelo de objetos del proyecto (POM). En este caso se utiliza la versión 4.0.0. , , : Estos elementos definen las coordenadas del proyecto. GroupId identifica el grupo u organización al que pertenece el proyecto. ArtefactId es el nombre del proyecto y versión es la versión actual del proyecto. y : Introduzca el nombre del proyecto y la URL. : Aquí se pueden definir propiedades personalizadas, que luego se pueden usar en otra parte del archivo pom.xml. En este caso, se definen la codificación del código fuente y las versiones del compilador Java. : Este elemento contiene todas las dependencias del proyecto. En este caso, la dependencia JUnit se incluye en la prueba unitaria. : Este elemento define la configuración relacionada con la construcción del proyecto. Aquí puede configurar diferentes complementos de Maven para usar al crear el proyecto. En resumen, el archivo pom.xml es una parte fundamental de cualquier proyecto Maven, ya que define la estructura, las dependencias y la configuración de compilación del proyecto. Esto permite a Maven administrar dependencias de manera eficiente y construir el proyecto de manera consistente.

5. Explore el directorio.

6. Compile el programa: mvn compile

7. Ejecute el programa: mvn exec:java -D exec.mainClass= org.pr2.App

8. Elimine los artefactos creados anteriormente, vuelva a compilar y ejecutar: mvn clean compile mvn exec:java -D exec.mainClass=org.pr2.App

9. Compile y consulte la documentación del proyecto: mvn-site

cd target/site
10. Explica en qué consisten los siguientes pasos: 
    Validación: Comprueba que el proyecto es válido y que todas las dependencias están disponibles. 
    compilar: compila el código fuente del proyecto y crea los archivos de clase en el directorio de destino. 
    prueba: ejecute las pruebas unitarias del proyecto utilizando un marco de prueba como JUnit.
    paquete: Paquetes que son códigos compilados y otros recursos en un formato específico, como JAR, WAR o EAR.
    instalar: instala el paquete en el repositorio local de Maven para que pueda usarse como una dependencia en otros proyectos. implementación: copie el paquete a un repositorio remoto para compartirlo con otros desarrolladores o sistemas de producción. clean: elimina archivos creados por el proceso de compilación, como archivos compilados y artefactos de compilación. 
    Sitio web: cree documentos del proyecto, como informes, estadísticas y otros documentos, y muéstrelos en el sitio web para referencia y colaboración.