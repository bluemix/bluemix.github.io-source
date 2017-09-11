---
title: Heroku Ktor Deployment
date: 2017-09-12 00:16:56
lang: en
direction: ltr
tags:
  - Kotlin
  - Ktor
  - Gradle
  - Deployment
  - Running
  - Heroku
---



I'll assume you already know basic knowledge about [Ktor](http://ktor.io) and you have built and ran you server locally using Gradle. In this post, the comming text will show you how to run it under [Heroku](https://heroku.com).


### Heroku CLI
First of all you need to install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli). Please follow the instructions on how to install it at your platform.

#### Login
`heroku login`
and fill your login information.

#### Create 
`heroku create`

#### Git linking
`<APP_NAME>` is the name of your app created in the above step.
`heroku git:remote -a <APP_NAME>`


### Gradle Shadow Jar
When your code gets pushed on Heroku, it will goes throgh the building phase, by which you should provie Gradle task name to be executed. We'll use [Shadow](http://imperceptiblethoughts.com/shadow/) plug-in to build and produce an executable jar file to be run at Heroku after the build succeds. So, add the following code to your `build.gradle` file

```
  shadowJar {
      baseName = '<Project Name>'
      classifier = null
      version = null
      destinationDir = new File('server') 
  }
```
here, the produced .jar will be created at the _server_ folder.

Now, let's inform Heroku about our building task

`heroku config:set GRADLE_TASK="shadowJar"`

### Procfile
After build has finished at Heroku, it will execute a command in the file named _Procfile_ that runs your executable code. So, 

`touch Procfile` 
and add the following single line in it

`web: java -jar server/<Project NAME>.jar`


### Running locally
In order to verify your app works fine as expected, let's run your app locall
`heroku local web`

Your server should be working the same as you were expected and worked with previousely. Try to open it on a browser window to check.


### Deploy
After finishing all of the above steps, let's deploy the project 

`git push heroku master`

... and that's.

Try checking it at `https://<APP_NAME>.heroku.com`

### Resources
Links helped me a lot understanding how to deploy Ktor on Heroku
#### [Want Kotlin on the Server? Do Ktor](https://www.bignerdranch.com/blog/want-kotlin-on-the-server-do-ktor/)
#### [Deploying Kotlin on Heroku with Ktor](https://jkutner.github.io/2017/04/10/kotlin-heroku-ktor.html)


### Questions?

Please feel free to ask any question or explanation if there are missing content or not clear at some point.


