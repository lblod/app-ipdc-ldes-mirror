# app-ipdc-ldes-proxy
Application stack to host the IPDC LDES feed.

## Getting started

Boot the stack using

    cd app-ipdc-ldes-proxy
    docker compose up

## Discussion
### Why setting up our own IPDC LDES feed
The current IPDC LDES feed hosted by Digitaal Vlaanderen doesn't fully comply with the LDES specification. Cache headers are not set. As a consequence, when consuming the LDES feed, all pages are always refetched to check for updates. This poses a heavy load on the server and the application, making it impossible to use the consumer in a production environment.

This stack provides a temporary solution to host the IPDC LDES feed with correct cache headers.
