# Minimalistic java docker file
Dockerfile for study approach. Docker image has been uploaded into docker hub, see https://hub.docker.com/repository/docker/tomascejka/java-hello-world.

## Build image
```
docker build . -t tomascejka/java-hello-world:latest
```

## Run
```
docker run --rm --name java-hello tomascejka/java-hello-world:latest
```

## Others
Build from given Dockerfile
<pre>
FROM eclipse-temurin:19-jdk-alpine

RUN echo '\
public class HelloWorld {\
    public static void main(String[] args) {\
        System.out.println("Hello, World!");\
    }\
}'\
&gt;&gt; HelloWorld.java

RUN javac HelloWorld.java
CMD ["java", "HelloWorld"]
</pre>

## Sources
+ https://hub.docker.com/_/eclipse-temurin/
