FROM alpine:latest
LABEL author="zwieratko"
LABEL decription="simple testing image base on Alpine"
ENV ENV="/home/rado/.profile"
RUN apk update \
    && apk add doas \
    && adduser -D rado \
    && echo 'rado:123' | chpasswd \
    && addgroup rado wheel \
    && echo 'permit :wheel as root' > /etc/doas.d/doas.conf \
    && mkdir -p /home/work \
    && chown rado:rado /home/work \
    && echo 'alias ll="ls -AlF"' > /home/rado/.profile
USER rado
WORKDIR /home/work
CMD [ "/bin/sh" ]
