FROM alpine:latest

RUN apk add --no-cache zip wget python3 perl bash make g++ tar zlib-dev

WORKDIR /app

RUN wget https://github.com/DaehwanKimLab/hisat2/archive/refs/tags/v2.2.1.zip && \
    unzip v2.2.1.zip && cd hisat2-2.2.1 && make

WORKDIR /app

RUN wget https://github.com/samtools/samtools/releases/download/1.20/samtools-1.20.tar.bz2 && \
    tar xvf samtools-1.20.tar.bz2 && cd samtools-1.20 && \
    ./configure --without-curses --disable-bz2 --disable-lzma && make

ENV PATH="$PATH:/app/hisat2-2.2.1:/app/samtools-1.20"
