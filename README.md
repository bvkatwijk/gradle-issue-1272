# gradle-issue-1272
This repository provides a quick setup showcasing [Gradle Issue 1272](https://github.com/gradle/gradle/issues/1272)

Clone the repo, run `docker-compose up gradle`, then change the content of `./src/main/java/org/example/Hello.java`.

## Expected result
The running gradle build task triggers a rebuild

## Observed result (Windows 10 Pro 1803)
The running gradle build task does not detect the changed file.

However, the file did change in the docker container: run `docker-compose exec gradle cat ./src/main/java/org/example/Hello.java` to see the file content.

## Observed Result (Mac OS Mojave 10.14.3)
A rebuild was triggered when the file was altered.

## Environment data
Behaviour was observed on:

Docker Desktop 2.0.0.3 (Engine 18.09.2, Compose 1.23.2, Machine 0.16.1)
Gradle versions: 5.2.1
