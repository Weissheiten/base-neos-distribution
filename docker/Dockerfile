FROM million12/typo3-flow-neos-abstract:latest
MAINTAINER Marcin Ryzycki marcin@m12.io

# ENV: Install following TYPO3 Neos version
# ENV: Repository for installed TYPO3 Neos distribution
ENV \ 
T3APP_BUILD_REPO_URL="https://github.com/Weissheiten/base-neos-distribution.git" \
T3APP_BUILD_BRANCH=2.3.8 \
T3APP_NEOS_SITE_PACKAGE=Billardcafe.Home

ADD repokeys/bitbucket-billardcafehome-key2 /

RUN \
# Configure GH repository key` \
  chown www /bitbucket-billardcafehome-key2 && chmod 600 /bitbucket-billardcafehome-key2 && \

# Pre-package Neos
  echo "IdentityFile /bitbucket-billardcafehome-key2" >> /etc/ssh/ssh_config && \
  . /build-typo3-app/pre-install-typo3-app.sh
