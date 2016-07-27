# Tips and Tricks

Use your plugin in your project!

```java
sourceSets {
  main {
    groovy.srcDirs = ['src/main/groovy', '../groovy-android-gradle-plugin/src/main/groovy']
    resources.srcDirs = ['src/main/resources', '../groovy-android-gradle-plugin/src/main/resources']
  }
}
```

Note:
Thanks John Engleman!
