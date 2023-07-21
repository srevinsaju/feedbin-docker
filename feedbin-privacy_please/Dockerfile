FROM ruby:alpine

ARG CAMO_KEY

WORKDIR /app

RUN apk add --no-cache \
	build-base \
	git

RUN git clone https://github.com/feedbin/privacy-please.git /app && rm -rf /app/.git

RUN bundle install

ENV PRIVACY_KEY=$CAMO_KEY

CMD ["bundle", "exec", "foreman", "start"]
