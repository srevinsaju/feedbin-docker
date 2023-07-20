FROM ruby:alpine

WORKDIR /app

RUN apk add --no-cache \
	git

RUN git clone https://github.com/feedbin/image.git /app

RUN bundle install

CMD ["bundle", "exec", "foreman", "start"]
