ARG TOPIO_VERSION=0.9.9.0

FROM ubuntu:16.04
ARG TOPIO_VERSION

RUN apt-get update -q \
&& apt-get install -q -y --no-install-recommends \
    wget \
    apt-transport-https \
    ca-certificates \
    xz-utils \
    libreadline-dev \
&& apt-get remove --purge -y \
&& apt-get clean -y \
&& rm -rf /var/lib/apt/lists/* \
&& wget https://github.com/telosprotocol/TOP-chain/releases/download/V${TOPIO_VERSION}/topio_V${TOPIO_VERSION}_linux64.tar.gz -O topio_V${TOPIO_VERSION}_linux64.tar.gz \
&& tar zxvf topio_V${TOPIO_VERSION}_linux64.tar.gz \
&& cp topio_${TOPIO_VERSION}/topio /usr/bin/ \
&& cp topio_${TOPIO_VERSION}/libxtopchain.so.${TOPIO_VERSION} /lib/ \
&& ln -s /lib/libxtopchain.so.${TOPIO_VERSION} /lib/libxtopchain.so \
&& rm -R topio_${TOPIO_VERSION} \
&& ls -la /lib/ \
&& topio -v

VOLUME ["/root/Topnetwork"]
ENTRYPOINT ["topio"]
