#FROM circleci/python:2.7
#RUN sudo apt-get update && sudo apt-get install ruby-sass

FROM debian:stretch

RUN apt-get update \
    && apt-get install --no-install-recommends -y \
      apt-transport-https \
      curl \
      ruby-sass \
      python-dev \
      python-pip \
      gnupg

RUN echo "deb https://packages.cloud.google.com/apt cloud-sdk-stretch main" > /etc/apt/sources.list.d/google-cloud-sdk.list
RUN curl https://packages.cloud.google.com/apt/doc/apt-key.gpg | apt-key add -
RUN apt-get update \
    && apt-get install --no-install-recommends -y \
      google-cloud-sdk \
      google-cloud-sdk-app-engine-python

ENV PYTHONPATH="/usr/lib/google-cloud-sdk/platform/google_appengine:${PYTHONPATH}"
