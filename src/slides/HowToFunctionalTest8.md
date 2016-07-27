# How to Functional Test

FunctionalSpec.groovy

```
@Rule TemporaryFolder dir

File getBuildFile() {
  return makeFile('build.gradle')
}

File makeFile(String path) {
  def file = file(path)
  if (!file.exists()) {
    def parts = path.split('/')
    if (parts.size() > 1) {
      dir.newFolder(*parts[0..-2])
    }
    dir.newFile(path)
  }
  return file
}

File file(String path) {
  def file = new File(dir.root, path)
  assert file.parentFile.mkdirs() || file.parentFile.exists()
  return file
}
```

Note:
Show Example of real app. Show off full build and checking for files.
"This is where you get creative"
