# gradle-issue-1272
Run `docker-compose up gradle`, then change the content of `./src/main/java/org/example/Hello.java`

### Expected result
The running gradle build task triggers a rebuild

### Observed result
The running gradle build task does not detect the changed file.

However, the file did change in the docker container: run `docker-compose exec gradle cat ./src/main/java/org/example/Hello.java` to see the file content.

### Environment data
Behaviour was observed on:

Windows 10
Docker Desktop 2.0.0.3 (Engine 18.09.2, Compose 1.23.2, Machine 0.16.1)
Gradle versions: 5.2.1, 4.10.2, 4.5.1, 4.2.1