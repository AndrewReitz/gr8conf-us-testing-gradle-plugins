# Testing Your Plugin with Unit Tests

For classes that depend on Gradle you want to use ProjectBuilder.

```java
@Rule TemporaryFolder dir

Project project

def setup() {
  project = ProjectBuilder.builder().withProjectDir(dir.root).build()
  project.pluginManager.apply(AppPlugin) // com.android.build.gradle.AppPlugin
  project.pluginManager.apply(GroovyAndroidPlugin) // my plugin
}
```

Note:
For example if you want to test an extension or other Gradle dependent files.
This allows you to test in a siloed environment and allows you check each small
piece of code.
