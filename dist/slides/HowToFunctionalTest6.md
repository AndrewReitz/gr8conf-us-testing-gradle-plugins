# How to Functional Test

```java
abstract class FunctionalSpec extends Specification {
  File getLocalRepo() {
    return new File('build/localrepo')
  }
}
```

Note:
