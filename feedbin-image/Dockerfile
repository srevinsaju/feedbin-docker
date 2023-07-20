FROM ruby:latest

WORKDIR /app

RUN apt-get update
RUN apt-get install \
	git

RUN git clone https://github.com/feedbin/image.git /app

RUN bundle install

CMD ["bundle", "exec", "foreman", "start"]
