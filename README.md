My custom Paper Fork ![GitHub Workflow Status (branch)](https://img.shields.io/jenkins/build?jobUrl=https%3A%2F%2Fwww.redserv.net%2Fjenkins%2Fjob%2FCustom%2520Paper%2F)
===========

High performance Spigot fork that aims to fix gameplay and mechanics inconsistencies.


**Support and Project Discussion:**
 - [IRC](https://webchat.esper.net/?channels=paper) or [Discord](https://discord.gg/papermc)

Custom Features
------
* Faster turtle egg hatch time
* Maxed book level for villagers
* Cheapest books for villagers
* Faster water/snow cauldrons, but mainly snow
* Instant-minable deepslate (No sound for the client though :\)
* Better trident spawn rate
* Instant-minable basalt (No sound for the client though :\)
* Faster Goat Attacks
* More slime spawns

How To (Server Admins)
------
Download Paper [here](https://www.redserv.net/jenkins/job/Custom%20Paper/lastSuccessfulBuild/artifact/Paper-Server/build/libs/Paper-Server-reobf.jar) or from the [Jenkins page](https://www.redserv.net/jenkins/job/Custom%20Paper/lastSuccessfulBuild).



How To (Plugin Developers) (Same as normal paper)
------
 * See our API patches [here](patches/api)
 * See upcoming, pending, and recently added API [here](https://github.com/PaperMC/Paper/projects/6)
 * Paper API javadocs here: [papermc.io/javadocs](https://papermc.io/javadocs/)
 * Maven Repo (for paper-api):
```xml
<repository>
    <id>papermc</id>
    <url>https://papermc.io/repo/repository/maven-public/</url>
</repository>
```
 * Artifact Information:
```xml
<dependency>
    <groupId>io.papermc.paper</groupId>
    <artifactId>paper-api</artifactId>
    <version>1.17.1-R0.1-SNAPSHOT</version>
    <scope>provided</scope>
</dependency>
 ```

**Or alternatively, with Gradle:**

 * Repository:
```kotlin
repositories {
    maven {
        url = uri("https://papermc.io/repo/repository/maven-public/")
    }
}

dependencies {
    compileOnly("io.papermc.paper:paper-api:1.17.1-R0.1-SNAPSHOT")
}

java {
    toolchain.languageVersion.set(JavaLanguageVersion.of(16))
}
```

How To (Compiling Jar From Source)
------
To compile Paper, you need JDK 16 and an internet connection.

Clone this repo, run `./gradlew applyPatches`, then `./gradlew reobfJar` from your terminal. You can find the compiled jar in the `Paper-Server/build/libs` directory.

To get a full list of tasks, run `./gradlew tasks`.

How To (Pull Request)
------
See [Contributing](CONTRIBUTING.md)

Support Us (Original Paper)
------
First of all, thank you for considering helping out, we really appreciate that!  

PaperMC has various recurring expenses, mostly related to infrastructure. Paper uses [Open Collective](https://opencollective.com/) via the [Open Source Collective fiscal host](https://opencollective.com/opensource) to manage expenses. Open Collective allows us to be extremely transparent, so you can always see how your donations are used. You can read more about finanically supporting PaperMC [on our website](https://papermc.io/sponsors).  

You can find our collective [here](https://opencollective.com/papermc), or you can donate via GitHub Sponsors [here](https://github.com/sponsors/PaperMC), which will also go towards the collective.

Special Thanks To:
-------------

[![YourKit-Logo](https://www.yourkit.com/images/yklogo.png)](https://www.yourkit.com/)

[YourKit](https://www.yourkit.com/), makers of the outstanding java profiler, support open source projects of all kinds with their full featured [Java](https://www.yourkit.com/java/profiler) and [.NET](https://www.yourkit.com/.net/profiler) application profilers. We thank them for granting Paper an OSS license so that we can make our software the best it can be.

[<img src="https://user-images.githubusercontent.com/21148213/121807008-8ffc6700-cc52-11eb-96a7-2f6f260f8fda.png" alt="" width="150">](https://www.jetbrains.com)

[JetBrains](https://www.jetbrains.com/), creators of the IntelliJ IDEA, supports Paper with one of their [Open Source Licenses](https://www.jetbrains.com/opensource/). IntelliJ IDEA is the recommended IDE for working with Paper, and most of the Paper team uses it.

All our sponsors!  
[![Sponsor Image](https://raw.githubusercontent.com/PaperMC/papermc.io/data/sponsors.png)](https://papermc.io/sponsors)
