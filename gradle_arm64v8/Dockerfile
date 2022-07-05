ARG VERSION=7.4.2-jdk17-jammy
FROM arm64v8/gradle:${VERSION}

RUN set -o errexit -o nounset \
    && apt-get update \
    && apt-get install --yes --no-install-recommends \
        net-tools \
        iputils-ping \
        iproute2 \
        telnet \
        unzip \
        wget \
        binutils \
        fakeroot

WORKDIR /home/gradle/project

CMD ["gradle"]