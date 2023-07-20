FROM ruby:alpine

ARG FEEDBIN_URL

WORKDIR /app

RUN apk add --no-cache \
	git \
	libidn11

RUN git clone https://github.com/feedbin/feedbin.git /app

RUN bundle install

CMD ["bundle", "exec", "foreman", "start"]
