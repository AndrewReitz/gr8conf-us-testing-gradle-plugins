# How to Functional Test

build.gradle

```
apply plugin: 'maven'
apply from: "$rootDir/gradle/projectLocalRepo.gradle"

...

tasks.withType(Test) {
  dependsOn install
}
```

Note:
