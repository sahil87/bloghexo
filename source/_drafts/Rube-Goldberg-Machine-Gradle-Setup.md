---
title: Rube Goldberg Machine - Gradle Setup
author: Sahil Ahuja
---
Just like the [Rube Goldberg Contraption](https://en.wikipedia.org/wiki/Rube_Goldberg_machine),
to learn algorithms, I started Course Era course, to test which I needed a Java Project, in which I needed to input stuff, for which I needed a testing framework, hence I tried to find the best testing framework, and found out about Spock and aldo needed a project dependency manager like Maven/Ant/Gradle, and chose Gradle as the dependency manager of choice, and learnt Groovy to be able to write Gradle DSL.

Gradle
-----
To setup Gradle Wrapper: `gradle wrapper` ([Gradle Guide](https://docs.gradle.org/current/userguide/userguide.html))

Now the executable gradlew or gradlew.bat in the current folder will install Gradle if not installed and then delegate to gradle all arguments passed originally to the gradlew command.

Gradle syntax: `gradle[w] taskName[s]`

For help/options simply type: `gradle[w]`
