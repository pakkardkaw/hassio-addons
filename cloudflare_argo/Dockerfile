ARG BUILD_FROM
FROM $BUILD_FROM

ARG BUILD_ARCH
RUN sudo curl -L https://github.com/cloudflare/cloudflared/releases/latest/download/cloudflared-linux-arm /usr/local/bin/cloudflared
RUN sudo chmod +x /usr/local/bin/cloudflared
RUN cloudflared -v

COPY run.sh /
RUN chmod a+x /run.sh

CMD [ "/run.sh" ]
