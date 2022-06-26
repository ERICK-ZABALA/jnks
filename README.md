
![image](https://github.com/ERICK-ZABALA/Thousand-Eyes/blob/master/slackBot/RESULT_JK)

# JENKINS ON CLOUD HEROKU

## OVERVIEW

This example demostrate as load jenkins on cloud heroku using java. You need to download Jenkins for java
https://www.jenkins.io/download/

Then you need to create an account in Heroku.
From you Visual Studio apply this commands to upload your Jenkins on the cloud.


![image](https://github.com/ERICK-ZABALA/Thousand-Eyes/blob/master/slackBot/flowAlert.png?raw=true)


## PREREQUISITES

* Create a Heroku account at https://id.heroku.com/login.


## CONFIGURATION

cisco@PC1 MINGW64 /d/CODEX/jnks (main)
$ heroku login
 »   Warning: heroku update available from 7.53.0 to 7.60.2.
heroku: Press any key to open up the browser to login or q to exit: 
Opening browser to https://cli-auth.heroku.com/auth/cli/browser/8c7ce-4320-9280-963?requestor=SFMyNTY.g2gDbQAAAA4xOTIuMjI2LjEzNC42N24GAMCftZ6BAWIAAVGA.vr43S0if-roN5yB1_SIDU
Logging in... done
Logged in as
cisco@PC1 MINGW64 /d/CODEX/jnks (main)
$ ls
jenkins.war  

cisco@PC1 MINGW64 /d/CODEX/jnks (main)
$ heroku plugin:install java
 »   Warning: heroku update available from 7.53.0 to 7.60.2.
 »   Warning: plugin:install is not a heroku command.
Did you mean plugins:install? [y/n]: y
warning @heroku-cli/plugin-java > heroku-exec-util > uuid@3.2.1: Please upgrade  to version 7 or higher.  Older versions may use Math.random() in certain circumstances, which is known to be problematic.  See https://v8.dev/blog/math-random for details.
Installing plugin java... installed v3.1.1

cisco@PC1 MINGW64 /d/CODEX/jnks (main)
$ heroku create java-jenkins
 »   Warning: heroku update available from 7.53.0 to 7.60.2.
Creating ⬢ java-jenkins... done
https://java-jenkins.herokuapp.com/ | https://git.heroku.com/java-jenkins.git
cisco@PC1 MINGW64 /d/CODEX/jnks (main)

$ heroku deploy:war jenkins.war -a java-jenkins
 
»   Warning: heroku update available from 7.53.0 to 7.60.2.
Uploading jenkins.war
-----> Packaging application...
       - app: java-jenkins
       - including: webapp-runner.jar
       - including: jenkins.war
-----> Creating build...
       - file: slug.tgz
       - size: 107MB
-----> Uploading build...
       - success   
-----> Deploying...
remote: 
remote: -----> Building on the Heroku-20 stack
remote: -----> Using buildpack: heroku/jvm
remote: -----> heroku-deploy app detected
remote: -----> Installing OpenJDK 1.8... done
remote: -----> Discovering process types
remote:        Procfile declares types -> buildpacks, war, web
remote:
remote: -----> Compressing...
remote:        Done: 159.3M
remote: -----> Launching...
remote:        Released v3
remote:        https://java-jenkins.herokuapp.com/ deployed to Heroku
remote: 
remote: This app is using the Heroku-20 stack, however a newer stack is available.
remote: To upgrade to Heroku-22, see:
remote: https://devcenter.heroku.com/articles/upgrading-to-the-latest-stack
remote:
-----> Done
ENJOYING !!! 







