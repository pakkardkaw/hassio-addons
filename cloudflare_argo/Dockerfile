ARG BUILD_FROM
FROM $BUILD_FROM

ARG BUILD_ARCH
RUN \
    && sudo wget -O /usr/local/bin/cloudflared https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-arm && chmod +x /usr/local/bin/cloudflared
RUN cloudflared -v

COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
