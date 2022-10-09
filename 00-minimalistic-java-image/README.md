# Minimalistic java docker file
Dockerfile for study approach

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

'''
docker build . -t tomascejka/java-hello-world:latest
'''

Docker image has been uploaded into docker hub, see https://hub.docker.com/repository/docker/tomascejka/java-hello-world.
