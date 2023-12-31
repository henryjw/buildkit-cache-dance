FROM amazonlinux:2023@sha256:521e488723a1ae16055067e3b78954870cf1c08c9d45421b9f8ffad82b349e1c
#RUN rm -f /etc/apt/apt.conf.d/docker-clean && \
#  echo 'Binary::apt::APT::Keep-Downloaded-Packages "true";' > /etc/apt/apt.conf.d/keep-cache
RUN \
  --mount=type=cache,target=/var/cache/apt,sharing=locked \
  --mount=type=cache,target=/var/lib/apt,sharing=locked \
  apt update && \
  apt-get --no-install-recommends install -y gcc
