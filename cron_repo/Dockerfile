FROM ruby:2.4.0
ENV API_KEY 123456
RUN gem install activeresource --no-ri --no-rdoc
# 設定済みreposman.rbをコピー
COPY ./reposman.rb /opt
# 起動用シェルをコピー
COPY ./run_reposman.sh /opt
COPY ./run_cron.sh /opt
RUN apt-get -y update && apt-get -y upgrade && apt-get install -y cron git
RUN chmod +x /opt/run_reposman.sh && chmod +x /opt/run_cron.sh
# 5分おきに実行
RUN echo '*/5 * * * * root /bin/sh /opt/run_reposman.sh' >> /etc/crontab
CMD ["/opt/run_cron.sh"]

