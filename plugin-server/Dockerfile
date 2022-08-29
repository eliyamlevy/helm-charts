FROM nginx:alpine

USER root

COPY ./nginx.conf /etc/nginx/nginx.conf

RUN mkdir -p /home/plugin-server/plugin-contents
COPY ./plugin /home/plugin-server/plugin-contents

RUN find -type f /home/plugin-server/plugin-contents > /home/plugin-server/plugin-contents/files.txt

ENTRYPOINT ["nginx", "-g", "daemon off;"]

