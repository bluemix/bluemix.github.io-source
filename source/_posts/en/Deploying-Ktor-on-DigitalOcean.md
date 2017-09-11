---
title: Deploying Ktor on DigitalOcean
date: 2017-09-10 16:44:29
lang: en
direction: ltr
tags:
  - Kotlin
  - Ktor
  - Gradle
  - Deployment
  - Running
  - DigitalOcean
  - Linux
  - Fedora
---


I was using [Ktor](http://ktor.io) for about a month and I have created a personal project, and I wanted to be deployed on a [DigitalOcean](https://cloud.digitalocean.com) droplet, that has Fedora 26 installed. Here are the basic steps I've collected in order to deploy your Ktor server running.

First of all, let's install some required packages.

### Pre-requesities

#### **wget, unzip, zip**
  `$ sudo dnf install wget unzip zip`

#### **[SDKMAN!](https://github.com/sdkman/sdkman-cli)**
  `$ curl -s https://get.sdkman.io | bash`

  then, this must be run at your user directory, e.g., at `/home/<USERNANE>/` path:
  `$ source "/home/<USERNANE>/.sdkman/bin/sdkman-init.sh"`
  
    

### Java and Kotlin

After SDKMAN! has been installed, you should now install Java and Kotlin
`$ sdk install java`
`$ sdk install kotlin`

### Running Ktor...

Now, locate your Ktor project,

`$ cd your-ktor-project/`

You might want to have the Gradle script be executable,
`$ chmod +x gradlew`

then, run the Gradle script,

`$ ./gradlew run`

* You might get _**Caught an exception trying to connect to Kotlin Daemon**_, by which solved through running the above command again 🤔

Your server should be running now!
> [Well-know ports](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers), e.g., 80, requires root permission.


### Questions?

Please feel free to ask any question or explanation if there are missing content or not clear at some point.


