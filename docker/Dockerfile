FROM azul/zulu-openjdk-alpine:8u162

ENV VERSION=1.0.1

EXPOSE 9999

RUN apk --no-cache upgrade -a && \
    apk --no-cache add wget

RUN wget https://github.com/bennypi/jenkins-maven-docker-test/releases/download/${VERSION}/jenkins-maven-docker-test-${VERSION}.jar

ENTRYPOINT java -jar jenkins-maven-docker-test-${VERSION}.jar