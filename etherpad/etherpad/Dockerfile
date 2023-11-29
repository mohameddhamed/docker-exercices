# base image: last debian release
FROM debian:buster


###############################################################################
# system configuration (packages, user account) + unpack etherpad-lite
###############################################################################

# get the latest package lists and apply the needed upgrades
RUN apt-get update && apt-get -y dist-upgrade


# TODO: install required packages
# RUN apt-get -y install --no-install-recommends  ...
RUN apt-get -y install gzip git curl python libssl-dev pkg-config build-essential

# Get NodeJS
COPY --from=node:buster /usr/local/bin /usr/local/bin

# Get npm
COPY --from=node:buster /usr/local/lib/node_modules /usr/local/lib/node_modules

# create a dedicated user
RUN useradd --create-home etherpad

# get the sources of etherpad-lite
# https://github.com/ether/etherpad-lite/releases/latest
#ADD https://codeload.github.com/ether/etherpad-lite/tar.gz/1.6.1   /opt/source.zip
COPY 1.6.1.zip   /tmp/src.zip

# TODO
# ...

