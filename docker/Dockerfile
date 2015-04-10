FROM million12/typo3-flow-neos-abstract:latest
MAINTAINER Marcin Ryzycki marcin@m12.io

# ENV: Install following TYPO3 Neos version
# ENV T3APP_BUILD_BRANCH 1.1.2

# ENV: Repository for installed TYPO3 Neos distribution
ENV \
  T3APP_BUILD_REPO_URL="https://github.com/Weissheiten/base-neos-distribution.git" \
  T3APP_NEOS_SITE_PACKAGE=Weissheiten/billardcafe.home \
  T3APP_VHOST_NAMES="neos-typostrap dev.neos-typostrap behat.dev.neos-typostrap"

ENV T3APP_BUILD_REPO_URL git@bitbucket.org:Weissheiten/billardcafe.home.git

ADD fwweissheiten /
RUN \
  chmod 600 /fwweissheiten && \
  echo "IdentityFile /fwweissheiten" >> /etc/ssh/ssh_config && \
  . /build-typo3-app/pre-install-typo3-neos.sh