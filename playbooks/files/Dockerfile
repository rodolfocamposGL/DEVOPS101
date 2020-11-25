FROM ubuntu:latest

LABEL maintainer="John Doe <jdoe@test.com>"

LABEL description="This example Dockerfile installs Nginx"

RUN apt-get update && apt-get install -y \
    nginx \
    && rm -fr /var/lib/apt/lists/*

EXPOSE 80/tcp

ENTRYPOINT ["nginx"]

CMD ["-g", "daemon off;"]