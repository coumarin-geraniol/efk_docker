FROM fluent/fluentd:v1.14.1
RUN apk add --update --virtual .build-deps \
    sudo build-base ruby-dev \
    && sudo gem install \
    fluent-plugin-elasticsearch \
    && sudo gem sources --clear-all \
    && apk del .build-deps \
    && rm -rf /var/cache/apk/* \
    /home/fluent/.gem/ruby/2.6.0/cache/*.gem