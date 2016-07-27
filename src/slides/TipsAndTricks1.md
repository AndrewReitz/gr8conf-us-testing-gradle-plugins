# Tips and Tricks

Have a "Base" Functional Specification.

```java
GradleRunner runner(String gradleVersion, String... args) {
    return GradleRunner.create()
        .withProjectDir(dir.root)
        .forwardOutput() // forward ouput to System.out
        .withArguments(args.toList())
        .withGradleVersion(gradleVersion?:GradleVersion.current().version)
  }
```

Note:
Gradle Runner With arguments passed in ready to go. Custom version
to pass in since I need to change versions in places.
Cont on next screen.
