# Tips and Tricks

"Base" Functional Specification Cont.

```java
BuildResult runWithVersion(String gradleVersion, String... args) {
  runner(gradleVersion, args).build()
}

BuildResult run(String... args) {
  runner(null, args).build()
}
```

Note:
