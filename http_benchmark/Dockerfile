FROM debian:10-slim
RUN apt update -y &&\
    apt install -y build-essential libssl-dev git &&\
    git clone https://github.com/wg/wrk.git wrk &&\
    make -C wrk
FROM debian:10-slim
RUN apt update -y &&\
    apt install -y nghttp2-client
COPY --from=0 /wrk/wrk /usr/local/bin

