FROM nginx

RUN echo '<h1>hello Docker~</h1>' > '/usr/share/nginx/html/index.html'

COPY sources.list /etc/apt/sources.list

RUN apt-get update && apt-get install -y curl && rm -rf /var/lib/apt/lists/*
HEALTHCHECK --interval=5s --timeout=3s \
  CMD curl -fs http://localhost/ || exit 1

