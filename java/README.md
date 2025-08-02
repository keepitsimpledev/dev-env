# java

https://ubuntu.com/tutorials/install-jre
```
$ sudo apt install default-jre
$ java --version # confirmation
```

https://vitux.com/how-to-setup-java_home-path-in-ubuntu/
```
$ update-alternatives --display java # find installation location for next step
$ export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
$ export PATH=$PATH:$JAVA_HOME/bin
$ echo $PATH # confirmation
```
