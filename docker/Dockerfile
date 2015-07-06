FROM million12/typo3-flow-neos-abstract:latest
MAINTAINER Marcin Ryzycki marcin@m12.io

# ENV: Install following TYPO3 Neos version
ENV T3APP_BUILD_BRANCH 1.2.9

# ENV: Repository for installed TYPO3 Neos distribution
ENV T3APP_BUILD_REPO_URL https://github.com/Weissheiten/base-neos-distribution.git

ADD repokeys/bitbucket-billardcafehome-key2 /
RUN \
  chmod 600 /bitbucket-billardcafehome-key2 && \
  echo "IdentityFile /bitbucket-billardcafehome-key2" >> /etc/ssh/ssh_config && \
  . /build-typo3-app/pre-install-typo3-app.sh
