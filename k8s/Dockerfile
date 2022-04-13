FROM ubuntu:22.04

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install --no-install-recommends -y apt-transport-https watch \
    netcat dnsutils tcpdump traceroute \
    curl wget jq \
    openssh-client git \
    ca-certificates \
    gzip tar \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN mkdir /.kube && chmod g+rwX /.kube

RUN curl -LO https://storage.googleapis.com/kubernetes-release/release/$(curl -s https://storage.googleapis.com/kubernetes-release/release/stable.txt)/bin/linux/amd64/kubectl \
    && chmod +x ./kubectl \
    && mv ./kubectl /usr/local/bin/kubectl

COPY ../curl-format-latencies.txt /tmp/


