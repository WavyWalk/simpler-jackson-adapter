# What's it?
An adapter for simpler framework's json requests parser.
# how to install
It's not on the repo engines, so just clone it in your project PARENT folder.
In your project's settings.graddle add:
```groovy
include ':simpler-jackson-adapter'  
project(':simpler-jackson-adapter').projectDir = new File(settingsDir, "simpler-jackson-adapter")
```
In build.graddle:
```groovy
compile project(':simpler-jackson-adapter')
```
# How to use with simpler
When building `SimplerDependenciesProvider`, as a value to `servletRequestParametersWrapper` argument pass:

```kotlin
ServletRequestParametersWrapper(  
        jsonParametersParser = JacksonParametersParser(ObjectMapper()) //simplified example
    )
```

That's it. It does nothing on it's own