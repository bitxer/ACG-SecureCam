# ACG-SecureCam [![Build Status](https://travis-ci.com/Infinitide/ACG-SecureCam.svg?token=VjEYc68MUWgPSpWqgDNV&branch=master)](https://travis-ci.com/Infinitide/ACG-SecureCam)

Server and Client program to be used to retrieve information from WebCam

## Dependencies
- Apache Commons CLI
- Bouncy Castle

## Compiling the program from source

### Server
In the server directory run the following command
```
javac -cp ../lib/*;. Server.java
```

### Client
In the Client directory run the following command
```
javac -cp ../lib/*;. Client.java
```

## Prerequisites

### Server
Ensure that a keystore with the server's private certificate in the server's directory
Ensure keystore is in PKCS#12 format

### Client
Ensure that the Certificate Authority's cert is in the Client Directory

## Using the Program

### Sserver
In the client directory run the following command
```
java -cp ../lib/*;. Sserver
```

#### CLI Options

```
usage: java Server <options>
 -a,--alias <arg>                Alias for cert in keystore
 -ap,--alias-password <arg>      Alias Password for alias
 -c,--certificate <arg>          Certificate
 -h,--help                       Prints help message
 -kp,--keystore-password <arg>   Key Store Password
 -ks,--keystore <arg>            Key Store Path
 -l,--listen <arg>               Address which server listens on
 -p,--port <arg>                 Port which server listens on
 -v,--verbose                    Verbose Output
```

### Client
In the client directory run the following command
```
java -cp ../lib/*;. Client
```

#### CLI Options
```
usage: java -cp lib/*;. Client <options>
 -a,--alias <arg>                Alias for cert in keystore
 -ap,--alias-password <arg>      Alias Password for alias
 -c,--certificate <arg>          Certificate
 -g,--gui                        Starts Client GUI
 -h,--help                       Prints help message
 -kp,--keystore-password <arg>   Key Store Password
 -ks,--keystore <arg>            Key Store Path
 -o,--output <arg>               File to save image to
 -p,--port <arg>                 Port which server listens on
 -s,--server <arg>               Address which server listens on
 -v,--verbose                    Verbose Output
```