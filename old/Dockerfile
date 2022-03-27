FROM tiangolo/nginx-rtmp

# FROM ubuntu:20.04
ARG GID=0
ARG UID=0
ENV GID=${GID:-0}
ENV UID=${UID:-0}

# # 必要なものインストール
# RUN apt-get update && apt-get -y upgrade && apt-get -y install build-essential libpcre3 libpcre3-dev libssl-dev zlib1g-dev wget
# # ninxのソースコードダウンロード
# RUN wget http://nginx.org/download/nginx-1.18.0.tar.gz
# # rtmpモジュールをダウンロード
# RUN wget https://github.com/arut/nginx-rtmp-module/archive/refs/tags/v1.2.2.tar.gz
# # それぞれ解凍
# RUN tar xvzf nginx-1.18.0.tar.gz
# RUN tar xvzf v1.2.2.tar.gz
# # nginxソースコードディレクトリでビルド
# WORKDIR /nginx-1.18.0
# RUN ./configure --with-http_ssl_module --add-module=../nginx-rtmp-module-1.2.2 && make && make install
RUN mkdir -p /usr/local/nginx/html/record/hls && \
    mkdir -p /usr/local/nginx/html/live/hls && \
    chmod -R 770 /usr/local/nginx/html/record/hls /usr/local/nginx/html/live/hls
    
# CMD /usr/local/nginx/sbin/nginx -g "daemon off;"