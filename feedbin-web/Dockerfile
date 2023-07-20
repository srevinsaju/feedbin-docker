FROM ruby:latest

ARG FEEDBIN_URL

WORKDIR /app

RUN apt-get update
RUN apt-get install \
	git \
	libidn11-dev

RUN git clone https://github.com/feedbin/feedbin.git /app

RUN bundle install

CMD ["bundle", "exec", "foreman", "start"]
