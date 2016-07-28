# How to Functional Test

```java
buildFile << """
  buildscript {
    repositories {
      maven { url "${localRepo.toURI()}" }
      jcenter()
    }
    dependencies {
      classpath 'com.your.coolplugin:plugin:+'
    }
    ...
  }

  apply plugin: 'com.your.coolplugin'
  ...
"""
```

Note:
