# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.154.2/containers/ubuntu/.devcontainer/base.Dockerfile

# [Choice] Ubuntu version: bionic, focal
ARG VARIANT="focal"
FROM mcr.microsoft.com/vscode/devcontainers/base:0-${VARIANT}

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    npm \
    python3 \
    python3-pip

ARG PROSELINT_VERSION="0.10.2"
ARG PYCODESTYLE_VERSION="2.6.0"
ARG PYLINT_VERSION="2.7.2"
RUN python3 -m pip install \
    proselint==${PROSELINT_VERSION} \
    pylint==${PYLINT_VERSION} \
    pycodestyle==${PYCODESTYLE_VERSION}

ARG MARKDOWN_LINK_CHECK_VERSION="3.8.6"
ARG MARKDOWN_SPELLCHECK_VERSION="1.3.1"
RUN npm install -g \
    markdown-link-check@${MARKDOWN_LINK_CHECK_VERSION} \
    markdown-spellcheck@${MARKDOWN_SPELLCHECK_VERSION}
