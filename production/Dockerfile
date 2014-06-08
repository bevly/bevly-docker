FROM phusion/baseimage:0.9.10

ENV HOME /root

RUN /etc/my_init.d/00_regen_ssh_host_keys.sh
RUN apt-get update
RUN apt-get install -y nginx-light supervisor
ADD /etc/supervisor/conf.d /etc/supervisor/conf.d/
ADD /etc/nginx/nginx.conf /etc/nginx/
ADD /etc/nginx/sites-available /etc/nginx/sites-available/
ADD dist/bevly-server /var/lib/bevly/
ADD dist/bevly-ui /var/lib/bevly/bevly-ui/

EXPOSE 80
ENTRYPOINT /usr/bin/supervisord -n -c /etc/supervisor/supervisord.conf