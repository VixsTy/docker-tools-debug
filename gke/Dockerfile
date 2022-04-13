FROM google/cloud-sdk

RUN apt-get update \
    && apt-get upgrade -y \
    && apt-get install --no-install-recommends -y curl netcat wget dnsutils jq tcpdump traceroute watch \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

COPY ../curl-format-latencies.txt /tmp/
