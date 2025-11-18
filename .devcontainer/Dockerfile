FROM mcr.microsoft.com/devcontainers/base:bookworm

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    curl \
    ca-certificates \
    git \
    build-essential \
  && rm -rf /var/lib/apt/lists/*

ENV PATH="/root/.local/bin:/root/.local/share/mise/shims:${PATH}"

RUN curl https://mise.run | sh

RUN mise install node@24 && mise use -g node@24

RUN corepack enable && corepack prepare pnpm@latest --activate

WORKDIR /workspace
