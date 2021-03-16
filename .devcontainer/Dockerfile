# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.154.2/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version: bionic, focal
ARG VARIANT="focal"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

# Following versions must be Debian Policy compliant.
# See https://www.debian.org/doc/debian-policy/ch-controlfields.html#version
ARG NPM_VERSION="6.14.4+ds-1ubuntu2"
ARG PYTHON3_VERSION="3.8.2-0ubuntu2"
ARG PYTHON3_PIP_VERSION="20.0.2-5ubuntu1.1"

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    npm=${NPM_VERSION} \
    python3=${PYTHON3_VERSION} \
    python3-pip=${PYTHON3_PIP_VERSION} \
    && rm -rf /var/lib/apt/lists/*

ARG PROSELINT_VERSION="0.10.2"
ARG PYCODESTYLE_VERSION="2.6.0"
ARG PYLINT_VERSION="2.7.2"
RUN python3 -m pip install --no-cache-dir \
    proselint==${PROSELINT_VERSION} \
    pylint==${PYLINT_VERSION} \
    pycodestyle==${PYCODESTYLE_VERSION}

ARG MARKDOWN_LINK_CHECK_VERSION="3.8.6"
ARG MARKDOWN_SPELLCHECK_VERSION="1.3.1"
RUN npm install -g \
    markdown-link-check@${MARKDOWN_LINK_CHECK_VERSION} \
    markdown-spellcheck@${MARKDOWN_SPELLCHECK_VERSION}
