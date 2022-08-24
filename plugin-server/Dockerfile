FROM nginx:alpine

USER root

RUN mkdir -p /home/plugin-server/plugin-contents
# RUN chmod -R 777 /etc/plugin-server/plugin-contents
COPY ./plugin /home/plugin-server/plugin-contents

RUN find /home/plugin-server/plugin-contents > /home/plugin-server/plugin-contents/files.txt ! -type d

RUN rm -v /etc/nginx/nginx.conf
COPY ./nginx.conf /etc/nginx/nginx.conf

ENTRYPOINT ["nginx", "-g", "daemon off;"]

