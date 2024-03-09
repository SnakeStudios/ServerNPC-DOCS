---
description: >-
  ServerNPC have one single repository where you can get the official builds for
  the API.
---

# Repositories

For optimal performance, I recommend using the latest version of the plugin. The API is designed to be compatible with the corresponding version of the plugin.

#### For gradle

```gradle
maven {
    url "https://nexus.snake.rip/repository/snake"
}
```

```gradle
implementation("com.isnakebuzz:ServerNPC-API:1.16.3-RELEASE")
```

#### For maven

```xml
<repository>
    <id>snake-repo</id>
    <url>https://nexus.snake.rip/repository/snake/</url>
</repository>
```

```xml
<dependency>
  <groupId>com.isnakebuzz</groupId>
  <artifactId>ServerNPC-API</artifactId>
  <version>1.16.3-RELEASE</version>
</dependency>
```
