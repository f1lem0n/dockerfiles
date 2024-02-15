FROM alpine:3.19

ENV PATH=/app/USalign:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin

RUN apk add --no-cache git make g++ bash gawk
RUN git clone https://github.com/pylelab/USalign.git
RUN cd USalign && make

WORKDIR /app