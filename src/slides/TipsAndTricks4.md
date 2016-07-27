# Tips and Tricks

Pass common easy to forget values to your tests.

```java
tasks.withType(Test) {
  systemProperty 'androidPluginVersion', androidPluginVersion
  systemProperty 'buildToolsVersion', buildToolsVersion
  systemProperty 'compileSdkVersion', compileSdkVersion
}
```

Note:
