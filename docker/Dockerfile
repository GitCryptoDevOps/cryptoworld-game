FROM ruby:slim

RUN apt-get update

RUN apt-get install -y \
      bundler \
      fonts-linuxlibertine \
      inotify-tools \
      libcairo2-dev \
      libpango1.0-dev \
      pdftk \
      poppler-utils

WORKDIR /home/app
ADD app/ /home/app
COPY Gemfile /home/app
#ADD . /app
RUN bundle install
