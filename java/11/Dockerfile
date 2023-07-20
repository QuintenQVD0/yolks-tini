FROM        --platform=$TARGETOS/$TARGETARCH eclipse-temurin:11.0.13_8-jdk-focal

LABEL       author="Michael Parker" maintainer="parker@pterodactyl.io"

LABEL       org.opencontainers.image.source="https://github.com/pterodactyl/yolks"
LABEL       org.opencontainers.image.licenses=MIT

RUN         apt update -y \
						&& apt install -y curl lsof ca-certificates openssl git tar sqlite3 fontconfig tzdata iproute2 libfreetype6 tini \
						&& useradd -d /home/container -m container

USER        container
ENV         USER=container HOME=/home/container
WORKDIR     /home/container

COPY        --chown=container:container ./../entrypoint.sh /entrypoint.sh
RUN         chmod +x /entrypoint.sh
ENTRYPOINT    ["/usr/bin/tini", "-g", "--"]
CMD         ["/entrypoint.sh"]