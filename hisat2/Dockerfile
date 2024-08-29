FROM alpine:3.19

RUN apk add --no-cache wget zip python3 perl

WORKDIR /app

RUN wget https://github.com/DaehwanKimLab/hisat2/archive/refs/tags/v2.2.1.zip && \
    unzip v2.2.1.zip

ENTRYPOINT [ "/app/hisat2-2.2.1" ]
