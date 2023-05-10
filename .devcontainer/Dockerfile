# FROM ghcr.io/osgeo/gdal:alpine-small-3.7.0
FROM mcr.microsoft.com/devcontainers/base:ubuntu

USER root

# Install the xz-utils package
RUN apt-get update && apt-get install -y xz-utils python3-pip gdal-bin libgdal-dev && \
    apt-get clean -y

# Update C env vars so compiler can find gdal
ENV CPLUS_INCLUDE_PATH=/vscode/include/gdal
ENV C_INCLUDE_PATH=/vscode/include/gdal

USER vscode

# Install Python packages
# RUN pip3 install --requirement requirements.txt