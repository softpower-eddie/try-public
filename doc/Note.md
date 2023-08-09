# Note

- [Kotlin](#kotlin)
  - [Install](#install)
  - [Hello World](#hello-world)
  - [REPL](#repl)
  -

## Kotlin

### Install

### Hello World

```bash
kotlinc-jvm -version
# info: kotlinc-jvm 1.9.0 (JRE 17.0.8+7-LTS)

kotlinc-jvm Hello.kt -d Hello.jar
# info: compiling: Hello.kt

java -classpath Hello.jar HelloKt
# Hello, world!

java -jar Hello.jar
# Hello, world!

find / -iname kotlin-stdlib.jar 2>&1 | grep -v "Permission denied"
# /usr/local/sdkman/candidates/kotlin/1.9.0/lib/kotlin-stdlib.jar

java -classpath Hello.jar:/usr/local/sdkman/candidates/kotlin/1.9.0/lib/kotlin-stdlib.jar HelloKt
# Hello, world!

kotlin -classpath Hello.jar HelloKt
# Hello, world!
```

### REPL

```bash
kotlinc-jvm
# Welcome to Kotlin version 1.9.0 (JRE 17.0.8+7-LTS).

>>> :load Hello.kt
>>> main()
# Hello, world!

```

### Kotlin Script

```bash
kotlinc-jvm -script listktsfiles.kts
# ./listktsfiles.kts

chmod +x greet.kts
./greet.kts

find / -iname kotlinc-jvm 2>&1 | grep -v "Permission denied"
# /usr/local/sdkman/candidates/kotlin/1.9.0/bin/kotlinc-jvm

sudo chown root:root greet.kts
sudo ./greet.kts

echo $USER
sudo usermod -aG root $USER
```