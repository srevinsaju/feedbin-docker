FROM node:alpine

ARG EXTRACT_USER
ARG EXTRACT_SECRET

WORKDIR /app

RUN apk add --no-cache \
	git

RUN git clone https://github.com/feedbin/extract.git /app && rm -rf /app/.git

RUN npm install

RUN mkdir users

RUN echo "${EXTRACT_SECRET}" > "users/${EXTRACT_USER}"

CMD ["node", "app/server.js"]
