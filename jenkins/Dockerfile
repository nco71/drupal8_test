FROM jenkins:alpine

USER root
COPY sudoers /etc/
RUN  apk add --update sudo && \
     addgroup jenkins wheel && \
     rm -rf /var/cache/apk/*
RUN  echo "jenkins ALL=NOPASSWD: ALL" >> /etc/sudoers
USER jenkins
