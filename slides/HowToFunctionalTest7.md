# How to Functional Test

```java
buildFile << """
  buildscript {
    repositories {
      maven { url "${localRepo.toURI()}" }
      jcenter()
    }
    ...
  }

  apply plugin: 'com.your.coolplugin'
  ...
"""
```

Note:
