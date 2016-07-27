# How to Functional Test

Let's get creative.

`projectLocalRepo.gradle`

```java
plugins.withType(MavenPlugin) {
  ext.localRepoUrl = new File(rootProject.buildDir, 'localrepo').toURI()

  install {
    repositories {
      mavenDeployer {
        repository(url: localRepoUrl)
      }
    }
  }
}
```

Note:
