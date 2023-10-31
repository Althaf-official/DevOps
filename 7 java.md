# What is full form of JDK?

Java Development Kit

# Which java version is installed on host01 server?

![image](https://github.com/Althaf-official/DevOps/assets/105126131/6ba8334e-5f47-48c1-9c2d-d15f64e904bf)

# Which tool is used for documenting your app with JDK?

javadoc

# Which tool is used for compiling your app with JDK?

javac

# debugging

jdb

# Which component was not part of JDK before version 9 of Java but became part of it from version 9 onwards?

jre


# Help us install java 20 inside /opt directory on app01 server.

ssh app01 to login to app01 server and run below command to download

`sudo curl https://download.java.net/java/GA/jdk20/bdc68b4b9cbc4ebcb30745c85038d91d/36/GPL/openjdk-20_linux-x64_bin.tar.gz --output /opt/openjdk-20_linux-x64_bin.tar.gz`

To uncompress run `sudo tar -xf /opt/openjdk-20_linux-x64_bin.tar.gz -C /opt/`

To verify run `/opt/jdk-20/bin/java -version` on app01 and confirm correct version is installed

![image](https://github.com/Althaf-official/DevOps/assets/105126131/0f6b597b-fbc1-4ed5-b48b-002edc600b50)



# We need to set java binary path in environment PATH variable to use java binaries. So that you can simply run java instead of the full path.


Once done, verify that you can invoke java simply by running java command.

![image](https://github.com/Althaf-official/DevOps/assets/105126131/445ba52c-d5a2-4bfe-952f-a543fc2ccdb1)

Set path variable with the command `export PATH=$PATH:/opt/jdk-20/bin`



