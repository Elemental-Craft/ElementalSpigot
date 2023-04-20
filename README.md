To find purpur's explanation of how to commit/add patches, please check out [here](https://github.com/PurpurMC/Purpur)

# Using in our future projects:
For future developers, if you want to depend on some of the features we've added. Please clone the repository to your local PC

* Make sure you clone it, not download the sources

After that's done, please wait for the gradle indexing and downloads process, then follow these steps:

* ./gradlew applyPatches if this is your first time running, and you have no source code
* ./gradlew publishToMavenLocal to have gradle compile a local repository for you

After that, you can depend on the jar

```gradle
repositories {
    mavenLocal()
}

dependencies {
   // Make sure not to shade this into your jar, so we use compileOnly
   compileOnly("net.elemental.server:elemental-server:1.19.4-R0.1-SNAPSHOT")
}
```