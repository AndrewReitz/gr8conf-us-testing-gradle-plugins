## Testing Your Plugin with Unit Tests

Testing small pieces of classes.

```java
def "should set options on groovy compile"() {
  given:
  def groovyTask = project.tasks.create('Test Groovy Compile', GroovyCompile)

  project.androidGroovy {
    options { // must be explicit here as spock does not resolve like gradle
      project.configure(groovyTask.groovyOptions) {
        encoding = 'UTF-8'
        forkOptions.jvmArgs = ['-noverify']
      }
      sourceCompatibility = JavaVersion.VERSION_1_7
      targetCompatibility = '1.7'
    }
  }

  when:
  project.extensions.getByType(GroovyAndroidExtension).configure(groovyTask)

  then:
  groovyTask.sourceCompatibility == '1.7'
  groovyTask.targetCompatibility == '1.7'
  groovyTask.groovyOptions.encoding == 'UTF-8'
  groovyTask.groovyOptions.forkOptions.jvmArgs == ['-noverify']
}
```

Note:
Scroll Down
Talk about gradle lifecycle
Show Other Examples
