FROM openjdk:11

ENV GOTTY_TAG_VER v1.0.1

RUN apt-get -y update && \
    apt-get install -y curl && \
    curl -sLk https://github.com/yudai/gotty/releases/download/${GOTTY_TAG_VER}/gotty_linux_amd64.tar.gz \
    | tar xzC /usr/local/bin && \
    apt-get purge --auto-remove -y curl && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists*

COPY /gotty_config/gotty /gotty