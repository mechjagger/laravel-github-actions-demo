
FROM php:7.3-cli-alpine

LABEL "com.github.actions.name"="Laravel PHP Insights Action"
LABEL "com.github.actions.description"="Run PHP Insights"
LABEL "com.github.actions.icon"="bar-chart-2"
LABEL "com.github.actions.color"="blue"

# fix work iconv library with alphine
# https://github.com/nunomaduro/phpinsights/issues/43#issuecomment-498108857
RUN apk add --no-cache --repository http://dl-cdn.alpinelinux.org/alpine/edge/community/ --allow-untrusted gnu-libiconv
ENV LD_PRELOAD /usr/lib/preloadable_libiconv.so php

COPY entrypoint.sh /usr/local/bin/entrypoint.sh

ENTRYPOINT ["/usr/local/bin/entrypoint.sh"]
