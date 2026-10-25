FROM mcr.microsoft.com/devcontainers/base:debian

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
  && apt-get install -y --no-install-recommends \
    ca-certificates \
    git \
    python3 \
    python3-venv \
  && rm -rf /var/lib/apt/lists/*

RUN python3 -m venv /opt/apm \
  && /opt/apm/bin/pip install --no-cache-dir apm-cli==0.34.0 \
  && ln -s /opt/apm/bin/apm /usr/local/bin/apm
