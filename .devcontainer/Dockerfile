FROM mcr.microsoft.com/vscode/devcontainers/python:3.6

USER vscode
RUN curl -sSL "https://get.sdkman.io" | bash

# https://github.com/awslabs/python-deequ/tree/v0.1.8#setup-java
ARG JAVA_VERSION="8.0.292.hs-adpt"
ARG SPARK_VERSION="3.1.2"
RUN /bin/bash -c \
  'source /home/vscode/.sdkman/bin/sdkman-init.sh && sdk install java "${JAVA_VERSION}" && sdk install spark "${SPARK_VERSION}"'

ENV POETRY_VERSION=1.1.7
RUN curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
