# java

https://www.digitalocean.com/community/tutorials/how-to-install-java-with-apt-on-ubuntu-22-04
```
$ sudo apt update # as always
$ sudo apt install default-jdk
$ java --version # confirmation
```

if necessary, https://vitux.com/how-to-setup-java_home-path-in-ubuntu/
```
$ update-alternatives --display java # find installation location for next step
$ export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
$ export PATH=$PATH:$JAVA_HOME/bin
$ echo $PATH # confirmation
```
