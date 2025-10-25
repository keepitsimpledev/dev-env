# java

https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-22-04
```
$ sudo apt update # as always
$ sudo apt install openjdk-18-jdk-headless
$ java -version # confirmation
$ javac -version # confirmation
```

if necessary, https://vitux.com/how-to-setup-java_home-path-in-ubuntu/
```
$ update-alternatives --display java # find installation location for next step
$ export JAVA_HOME=/usr/lib/jvm/java-18-openjdk-amd64
$ export PATH=$PATH:$JAVA_HOME/bin
$ echo $PATH # confirmation
```

## VS Code
- [Java Platform Extension](https://marketplace.visualstudio.com/items?itemName=Oracle.oracle-java)
- Consider disabling "Jdk > Java On Save: Organize Imports > Enable organize imports action on a document save". Otherwise, if auto-save is on, manually added imports will often just disappear
- If there seem to be inexplicable IDE problems like "cannot find symbol" or "package not found", there might be an issue with [the deprecated `org.gradle.util.VersionNumber`](https://github.com/gradle/gradle/issues/34546). This deprecation happened in [version 9](https://gradle.org/releases/), so consider downgrading:
  `./gradlew wrapper --gradle-version 8.14.3`
  (followed by [Java Platform Extension](https://marketplace.visualstudio.com/items?itemName=Oracle.oracle-java)'s "Clean the Java language server", if necessary)
