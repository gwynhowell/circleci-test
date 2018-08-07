FROM circleci/python:2.7

RUN sudo apt-get update \
    && sudo apt-get install --no-install-recommends -y \
      ruby-sass

ENV CLOUD_SDK_URL="https://dl.google.com/dl/cloudsdk/channels/rapid/downloads/google-cloud-sdk-210.0.0-linux-x86_64.tar.gz"
RUN curl $CLOUD_SDK_URL | tar -xz -C ~/
RUN sh ~/google-cloud-sdk/install.sh --quiet --path-update true
RUN ~/google-cloud-sdk/bin/gcloud --quiet components install app-engine-python
