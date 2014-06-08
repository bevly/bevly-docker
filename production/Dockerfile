FROM phusion/baseimage:0.9.10

ENV HOME /root

RUN /etc/my_init.d/00_regen_ssh_host_keys.sh
RUN apt-get update
RUN apt-get install -y nginx-light
ADD /etc/service /etc/service/
ADD /etc/nginx/nginx.conf /etc/nginx/
ADD /etc/nginx/sites-available /etc/nginx/sites-available/
ADD dist/bevly-server /var/lib/bevly/
ADD dist/bevly-ui /var/lib/bevly/bevly-ui/

EXPOSE 80
ENTRYPOINT ["/sbin/my_init"]