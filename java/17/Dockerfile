FROM        eclipse-temurin:17

RUN			apt-get -y update
RUN         apt-get -y install ca-certificates curl fontconfig git bash openssl sqlite tar tzdata openjfx \
			    && adduser --disabled-password --home /home/container container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh
CMD         [ "/bin/bash", "/entrypoint.sh" ]
