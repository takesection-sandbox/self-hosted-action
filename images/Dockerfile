FROM ghcr.io/actions/actions-runner:2.312.0

USER root

RUN apt update && apt install -y curl && \
    curl -fLo /tmp/sbt.tgz https://github.com/sbt/sbt/releases/download/v1.9.8/sbt-1.9.8.tgz && \
    tar zxf /tmp/sbt.tgz -C /usr/share && ln -s /usr/share/sbt/bin/sbt /usr/bin/sbt && rm -f /tmp/sbt.tgz

WORKDIR /home/runner
USER runner
