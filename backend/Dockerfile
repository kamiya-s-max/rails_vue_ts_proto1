FROM ruby:2.6.4

RUN apt-get update -qq && apt-get install -y build-essential libpq-dev postgresql-client nodejs

ENV APP_DIR /app/backend

WORKDIR $APP_DIR
COPY Gemfile $APP_DIR
COPY Gemfile.lock $APP_DIR
RUN bundle install
COPY . $APP_DIR