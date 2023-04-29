# Maven Repository

## Overview

We offer a public Maven repository for Lunar Client artifacts, hosted at `https://repo.lunarclient.dev`. Please note the TLD, `.dev`, which is used for all of our developer-facing documentation.

## Adding the Repository

Maven:

```xml filename="pom.xml"
<repositories>
    <repository>
        <id>lunarclient</id>
        <url>https://repo.lunarclient.dev</url>
    </repository>
</repositories>
```

Gradle:

```groovy filename="build.gradle"
repositories {
    maven {
        name = "lunarclient"
        url = "https://repo.lunarclient.dev"
    }
}
```

## Adding Apollo as a dependency

Maven:

```xml filename="pom.xml"
<dependencies>
    <dependency>
        <groupId>com.lunarclient</groupId>
        <artifactId>apollo-api</artifactId>
        <version>0.1.0-SNAPSHOT</version>
        <scope>provided</scope>
    </dependency>
</dependencies>
```

Gradle:

```groovy filename="build.gradle"
dependencies {
    compileOnly("com.lunarclient:apollo-api:0.1.0-SNAPSHOT")
}
```

## Other artifacts

### Apollo dependencies

Artifacts required to build Apollo.

- `com.lunarclient:apollo-protos` (source available on Buf Schema Registry, at https://buf.build/lunarclient/apollo)
- `com.lunarclient:apollo-common` (source available in main Apollo repo, at https://github.com/LunarClient/Apollo)

### Legacy API

API / sample implementations for our _legacy_ Lunar Client API. These are only available for backwards compatibility; all new development should use Apollo, our next-gen API platform.

- `com.lunarclient:BukkitImpl` (source available at https://github.com/LunarClient/BukkitImpl)
- `com.lunarclient:bukkitapi` (source available at https://github.com/LunarClient/BukkitAPI)
- `com.lunarclient:bukkitapi-nethandler` (source available at https://github.com/LunarClient/BukkitAPI-NetHandler)

### Lunar Client forks

Forks of various open source libraries we use and publish.

- `org.cadixdev:mercury` (source available at https://github.com/LunarClient/Mercury)
- `org.cadixdev:mercurymixin` (source available at https://github.com/LunarClient/MercuryMixin)
- `org.spongepowered:mixin` (source available at https://github.com/LunarClient/Mixin)
- `com.eliotlash.molang:particleman` (source available at https://github.com/LunarClient/particleman)
- `software.bernie.geckolib3:core` (source available at https://github.com/LunarClient/geckolib-core)
