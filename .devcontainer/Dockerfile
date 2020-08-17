FROM ruby:2.7.1-buster

RUN apt update && apt install -y zsh less graphviz groff-base bsdmainutils
RUN gem update --system

ENV BUNDLE_APP_CONFIG=""
ENV BUNDLE_SILENCE_ROOT_WARNING=""
RUN useradd --create-home --user-group --uid 1000 app
RUN mkdir -p /app /original
RUN chown -R app /app /original /usr/local/bundle

WORKDIR /app

USER app

ENV SHELL=/bin/zsh
