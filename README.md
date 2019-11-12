### Multiple tools for building java projects in continuous integration

# launch4j

Cross-platform Java executable wrapper
Launch4j is a cross-platform tool for wrapping Java applications distributed as jars in lightweight 
Windows native executables. The executable can be configured to search for a certain JRE version or use a bundled one, 
and it's possible to set runtime options, like the initial/max heap size. 
The wrapper also provides better user experience through an application icon, 
a native pre-JRE splash screen, and a Java download page in case the appropriate JRE cannot be found.

For more details on launch4j command, go to: [Launch4j site](http://launch4j.sourceforge.net/)

```console
docker run -v $(pwd):/app --rm keviocastro/javabuild launch4j /app/config.xml
````

## bumpversion

Version-bump your software with a single command!
See [bumpversion site](https://github.com/peritus/bumpversion)


```console
docker run -v $(pwd):/app --rm keviocastro/javabuild bumpversion --current-version minor pom.xml
````

# maven

Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
See [Maven site](https://maven.apache.org/)

```console
docker run -v $(pwd):/app --rm keviocastro/javabuild mvn clean package
````
