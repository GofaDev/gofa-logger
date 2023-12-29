# Gofa logger for android

## Installation

Add it in your root build.gradle at the end of repositories:

- Groovy DSL

```groovy
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```

- Kotlin DSL

```kotlin
allprojects {
    repositories {
        ...
        maven(url = "https://jitpack.io")
    }
}
```

Add the dependency

- Groovy DSL

```groovy
dependencies {
    implementation 'com.github.gofa-software:gofa-logger:1.0.1'
}
```

- Kotlin DSL

```kotlin
dependencies {
    implementation("com.github.gofa-software:gofa-logger:1.0.1")
}
```

## Usages
```kotlin
data class Car(val name: String, val model: String)

val car = Car("BMW", "X5")
val ca2 = Car("BMW", "X5")

GofaLogger.log("Car =", car)

GofaLogger.log("Car =", car, "Car2 =", car2)

GofaLogger.group("%cCar", "color: red; font-size: 20px; font-weight: bold;")
GofaLogger.log("Car =", car)
GofaLogger.log("Car2 =", car2)
GofaLogger.groupEnd()

```
