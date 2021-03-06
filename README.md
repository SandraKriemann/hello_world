# Hello-Wercker-World
#### SpringBoot, Gradle, Docker, Wercker

This project shows the use of Springboot and Gradle. You can build the project either on your local machine with docker (Step A) or you use wercker as your CI and let them build your application for you (Step B).
You can also use the code to compare both ways.

[![wercker status](https://app.wercker.com/status/f2e4c13fd194cde02c47337ea5da6baa/m "wercker status")](https://app.wercker.com/project/bykey/f2e4c13fd194cde02c47337ea5da6baa)


## Step A: Runs with Dockerfile

        ./gradlew build buildDocker
        
       docker run -p 8080:8080 name


## Step B: Runs with wercker

        add this repository to http://app.wercker.com/
            save your docker login in the project settings/ Environment variables as DOCKER_USER and DOCKER_PASSWORD
            the rest is wercker doing for you
        pull the latest docker image with e.g.: docker pull sandra/hello_world:latest
        run the dockerfile: docker run -p 8080:8080 sandra/hello_world:latest
        
## Check the Output in your Browser

To check the Application in your Browser like that:
![Screenshot](screenshot.png?raw=true "Title")

find the IP the docker machine is currently running at with

        docker inspect 'containerID'
        
## Used Tutorials
These are the Tutorials I used and I would highly recommend:

        https://spring.io/guides/gs/gradle/
        https://spring.io/guides/gs/spring-boot-docker/
        
And don't underestimate community. The wercker community is getting bigger and bigger and they are happy to help.
