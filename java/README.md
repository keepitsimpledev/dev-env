# java

[Installing java with apt on ubuntu,](https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-22-04)
[using temurin JDK for compatibility with available github runners](https://adoptium.net/installation/linux)

```
sudo apt install -y wget apt-transport-https gpg
wget -qO - https://packages.adoptium.net/artifactory/api/gpg/key/public | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/adoptium.gpg > /dev/null
echo "deb https://packages.adoptium.net/artifactory/deb $(awk -F= '/^VERSION_CODENAME/{print$2}' /etc/os-release) main" | sudo tee /etc/apt/sources.list.d/adoptium.list
sudo apt update
sudo apt install temurin-17-jdk
java -version # confirmation
javac -version # confirmation
```

if necessary, https://vitux.com/how-to-setup-java_home-path-in-ubuntu/
```
$ update-alternatives --display java # find installation location for next step
$ export JAVA_HOME=/usr/lib/jvm/temurin-17-jdk-amd64
$ export PATH=$PATH:$JAVA_HOME/bin
$ echo $PATH # confirmation
```

## VS Code
- [Java Platform Extension](https://marketplace.visualstudio.com/items?itemName=Oracle.oracle-java)
  - Reminder: when resolving project initialization issues, confirm classpath and java runtime in Explorer > JAVA PROJECTS > More Actions...
- Consider disabling "Jdk > Java On Save: Organize Imports > Enable organize imports action on a document save". Otherwise, if auto-save is on, manually added imports will often just disappear
- Gradle: If there seem to be inexplicable IDE problems like "cannot find symbol" or "package not found", there might be an issue with [the deprecated `org.gradle.util.VersionNumber`](https://github.com/gradle/gradle/issues/34546). This deprecation happened in [version 9](https://gradle.org/releases/), so consider downgrading:
  `./gradlew wrapper --gradle-version 8.14.3`
  (followed by [Java Platform Extension](https://marketplace.visualstudio.com/items?itemName=Oracle.oracle-java)'s "Clean the Java language server", if necessary)

## other notes
- [Maven: directory structure convention](https://maven.apache.org/guides/introduction/introduction-to-the-standard-directory-layout.html)
