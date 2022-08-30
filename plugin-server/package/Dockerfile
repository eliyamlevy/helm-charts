FROM nginx:alpine

USER root

# COPY ./nginx.conf /etc/nginx/nginx.conf

RUN mkdir -p /home/plugin-server/plugin-contents
COPY ../plugin /home/plugin-server/plugin-contents

RUN find /home/plugin-server/plugin-contents > /home/plugin-server/plugin-contents/files.txt -type f

ENTRYPOINT ["nginx", "-g", "daemon off;"]

