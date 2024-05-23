# https://registry.hub.docker.com/_/nginx/
FROM nginx:1.26

# 設定ファイルをコピー
COPY conf/nginx.conf /etc/nginx/nginx.conf

# HTMLファイルをコピー
COPY index.html /usr/share/nginx/html
