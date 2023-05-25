FROM eed3si9n/sbt:latest as mobiliquest

USER root

RUN apk update && apk add bash git sudo npm

RUN npm install npm@9.3.1
RUN npm install -g n
RUN n 19.4.0

RUN node --version

#DEV
#COPY mobiliquest/DEV /var/mobiliquest/mobiliquest

RUN mkdir -p /var/mobiliquest
RUN adduser mobiliquest -g "" -D -h /var/mobiliquest/

#DEV
#RUN chown mobiliquest -R /var/mobiliquest/mobiliquest/

COPY mobiliquest/run.sh /var/mobiliquest/run.sh
COPY mobiliquest/compile.sh /var/mobiliquest/compile.sh
RUN chmod +x /var/mobiliquest/run.sh
RUN chmod +x /var/mobiliquest/compile.sh

<<<<<<< Updated upstream
#EXPOSE 8080:8081
=======
EXPOSE 80
>>>>>>> Stashed changes
USER mobiliquest


#PROD
RUN cd /var/mobiliquest && \
    git config --global http.sslVerify "false" && \
    git clone https://github.com/Geographie-cites/mobiliquest.git && \
    cd mobiliquest && \
    git checkout master

RUN bash /var/mobiliquest/compile.sh

ENTRYPOINT bash /var/mobiliquest/run.sh

