# Minimalistic java docker file
Dockerfile for study approach

'''
FROM eclipse-temurin:19-jdk-alpine

RUN echo '\
public class HelloWorld {\
    public static void main(String[] args) {\
        System.out.println("Hello, World!");\
    }\
}'\
>> HelloWorld.java

RUN javac HelloWorld.java
CMD ["java", "HelloWorld"]
'''
