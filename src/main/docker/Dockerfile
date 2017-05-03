FROM openjdk

ARG fileName
ENV IMG_VERSION ${fileName}

VOLUME /tmp
ADD maven/$IMG_VERSION.jar $IMG_VERSION.jar
RUN sh -c 'touch /$IMG_VERSION.jar'
ENTRYPOINT java -Djava.security.egd=file:/dev/./urandom -jar "/$IMG_VERSION.jar"
