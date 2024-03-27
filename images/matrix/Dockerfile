FROM alpine:latest
LABEL author="rado@one.sk"
LABEL description="mega supa imidz"
# ADD alpine-minirootfs-3.19.1-x86_64.tar.gz /
RUN set -o errexit \
    && sleep 1 \
    && apk add tmatrix
WORKDIR /home
USER 403
# CMD [ "/usr/bin/tmatrix", "--title=DOCKER_RULES" ]
CMD [ "/bin/sh" ]
