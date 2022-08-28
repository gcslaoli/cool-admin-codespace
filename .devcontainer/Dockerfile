# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.238.1/containers/codespaces-linux/.devcontainer/base.Dockerfile

FROM mcr.microsoft.com/vscode/devcontainers/universal:2-focal
COPY first-run-notice.txt /usr/local/etc/vscode-dev-containers/first-run-notice.txt


# ** [Optional] Uncomment this section to install additional packages. **
USER root

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends tzdata
# 时区配置
RUN echo "Asia/Shanghai" > /etc/timezone
RUN rm -f /etc/localtime    
RUN dpkg-reconfigure -f noninteractive tzdata

USER codespace
