FROM ruby:2.5
RUN apt-get update -qq && apt-get install -y build-essential libpq-dev nodejs
RUN mkdir /rails-ecs
WORKDIR /rails-ecs
COPY Gemfile ./Gemfile
COPY Gemfile.lock ./Gemfile.lock
RUN bundle install
COPY . ./rails-ecs
CMD ["bundle", "exec", "rails", "s", "-p", "3000", "-b", "0.0.0.0"]
