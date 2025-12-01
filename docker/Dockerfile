FROM python:3.11-slim

RUN apt-get update && apt-get install -y \
    bash \
    wget \
    curl \
    jq \
    whiptail \
    util-linux \
    pciutils \
    lsb-release \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

WORKDIR /opt/proxmenux

RUN wget -qLO install_proxmenux.sh https://raw.githubusercontent.com/MacRimi/ProxMenux/main/install_proxmenux.sh \
    && chmod +x install_proxmenux.sh \
    && bash install_proxmenux.sh --yes

EXPOSE 8008

ENTRYPOINT ["menu"]
