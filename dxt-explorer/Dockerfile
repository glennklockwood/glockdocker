# docker build -t dxtexplorer .
# docker run -it --rm dxtexplorer

FROM ubuntu:20.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt -y update && \
    apt -y install --no-install-recommends r-base python3 python3-pip git && \
    rm -rf /var/cache/yum

WORKDIR /work

RUN git clone https://gitlab.com/jeanbez/dxt-explorer.git && \
    cd dxt-explorer && \
    pip install -r requirements.txt
