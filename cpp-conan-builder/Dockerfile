FROM ubuntu:20.04 AS builder
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y python3 python3-pip build-essential cmake git
RUN mkdir -p ~/.ssh && echo "Host github.com\n\tStrictHostKeyChecking no\n" >> ~/.ssh/config
RUN pip install conan
#RUN conan remote add conanbins http://host.docker.internal:8082/artifactory/api/conan/conanbins && conan user ci -r conanbins -p Conanbins1
ENV CONAN_REVISIONS_ENABLED=1
