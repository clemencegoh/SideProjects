# What are these 2? (Gradle vs Maven)

*Note:* This is here purely due to my confusion over the different compilers present in Java IntelliJ Idea

**These 2 are build automation tools**
* Gradle is newer
    * Uses Groovy (Dynamically-typed language, similar to python)
        * Alternative to Groovy is Kotlin (Statically typed)
    * Gradle was adapted by Google as the build system for **Android projects**.
    * designed to support multi-project builds that are expected to be quite huge. It also allows for incrementally adding to your build, because it knows which parts of your project are updated. Tasks that are dependent on updated parts are no longer re-executed. 
* Maven is used for project build automation using Java.
    * maps dependencies as well as mapping out how the software is built.
    * Uses XML file to describe everything: project being built, dependencies on third party modules, build order, needed plugins.
    * Maven will download libraries and plugins from the different repositories and then puts them all in a cache on your local machine. While predominantly used for Java projects, you can use it for Scala, Ruby, and C#, as well as a host of other languages.

## How are these 2 relevant?
* Could consider for future development projects since they allow for fine-tuning of scripts to run or dependencies to build upon every build.