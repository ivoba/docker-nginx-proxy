# Docker Nginx Proxy

in docker-compose.yml we set googleapis.com as ARG for the proxy_pass.  
for development run:

    docker-compose run

call f.e.

    http://localhost:8080/calendar/v3/calendars/<your-calendar>s%40group.calendar.google.com/events?key=<your-key>&timeMin=2019-04-29T00%3A00%3A00%2B02%3A00&timeMax=2019-05-06T00%3A00%3A00%2B02%3A00&singleEvents=true&maxResults=9999


## Build

We use automated builds from https://cloud.docker.com

In hooks we transfer ENV vars to build ARG.  
Set PROXY ENV var to set the proxy_pass value for nginx.

## Resources
- https://medium.com/@oliver.zampieri/self-signed-ssl-reverse-proxy-with-docker-dbfc78c05b41
- remove all headers for privacy, we dont want google to know too much
  https://stackoverflow.com/questions/44536548/how-to-remove-client-headers-in-nginx-before-passing-request-to-upstream-server
- https://docs.docker.com/docker-hub/builds/link-source/
- ARGs in cloud.docker automated builds
  https://github.com/docker/hub-feedback/issues/508

## Todo
- use http2 for proxy https://stackoverflow.com/questions/41637076/http2-with-node-js-behind-nginx-proxy
