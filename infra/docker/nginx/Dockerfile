FROM nginx:1.27

WORKDIR /workspace

ENV TZ=UTC
RUN curl -fsSL https://deb.nodesource.com/setup_22.x -o nodesource_setup.sh
RUN bash nodesource_setup.sh
RUN apt-get update
RUN apt-get install -y nodejs

COPY ./infra/docker/nginx/*.conf /etc/nginx/conf.d/
