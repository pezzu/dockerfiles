FROM node:10-stretch

RUN \
    apt-get update && \
    apt-get install -y libdbus-glib-1-2 libgtk-3-0 && \
    cd /opt && \
    wget --quiet https://ftp.mozilla.org/pub/firefox/releases/59.0.3/linux-x86_64/en-US/firefox-59.0.3.tar.bz2 && \
    tar xvjf firefox-59.0.3.tar.bz2 && \
    ln -st /usr/local/bin /opt/firefox/firefox && \
    rm -f firefox-59.0.3.tar.bz2 && \
    wget --quiet https://github.com/laurentj/slimerjs/releases/download/1.0.0/slimerjs-1.0.0.tar.bz2 && \
    tar xvjf slimerjs-1.0.0.tar.bz2 && \
    ln -st /usr/local/bin /opt/slimerjs-1.0.0/slimerjs && \
    rm -f slimerjs-1.0.0.tar.bz2