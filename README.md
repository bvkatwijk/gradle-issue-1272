# gradle-issue-1272

Run `docker-compose up gradle`, then change the content of `./src/main/java/org/example/Example.java`

### Expected result
The running gradle build task triggers a rebuild

### Observed result
The running gradle build task does not detect the changed file


