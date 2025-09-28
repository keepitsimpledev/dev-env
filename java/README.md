# java

https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-22-04
```
$ sudo apt update # as always
$ sudo apt install openjdk-18-jdk-headless
$ java --version # confirmation
```

if necessary, https://vitux.com/how-to-setup-java_home-path-in-ubuntu/
```
$ update-alternatives --display java # find installation location for next step
$ export JAVA_HOME=/usr/lib/jvm/java-18-openjdk-amd64
$ export PATH=$PATH:$JAVA_HOME/bin
$ echo $PATH # confirmation
```

[extension for VS code](https://marketplace.visualstudio.com/items?itemName=Oracle.oracle-java)
