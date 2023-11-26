# base image: last debian release
FROM debian:buster

# install the latest upgrades
RUN apt-get update && apt-get -y dist-upgrade

# TODO install nginx
RUN apt install -y nginx

# TODO set the default container command command (CMD) to run the nginx daemon
CMD ["nginx", "-g", "daemon off;"]

