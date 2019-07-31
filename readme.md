# Nginx Proxy for https://www.googleapis.com

for development run:

    docker-compose run

call f.e.

    https://localhost/calendar/v3/calendars/<your-calendar>s%40group.calendar.google.com/events?key=<your-key>&timeMin=2019-04-29T00%3A00%3A00%2B02%3A00&timeMax=2019-05-06T00%3A00%3A00%2B02%3A00&singleEvents=true&maxResults=9999


## Build



## Resources
- https://medium.com/@oliver.zampieri/self-signed-ssl-reverse-proxy-with-docker-dbfc78c05b41
- remove all headers for privacy, we dont want google to know too much
  https://stackoverflow.com/questions/44536548/how-to-remove-client-headers-in-nginx-before-passing-request-to-upstream-server
- https://docs.docker.com/docker-hub/builds/link-source/

## Todo
- use http2 for proxy https://stackoverflow.com/questions/41637076/http2-with-node-js-behind-nginx-proxy
