StatsD + Graphite + Grafana 4
---------------------------------------------

This image contains a sensible default configuration of StatsD, Graphite and Grafana.


### Using the Docker Index ###

All you need as a prerequisite is having `docker` installed on your machine. The container exposes the following ports:

- `80`: the Grafana web interface.
- `81`: the Graphite web port
- `8125`: the StatsD port.
- `8126`: the StatsD administrative port.

To start a container with this image you just need to run the following command:

```bash
$ docker run -d --restart=always -p 127.0.0.1:8080:80 -p 127.0.0.1:8081:81 -p 127.0.0.1:8125:8125/udp -p 127.0.0.1:8126:8126 --name=grafana4-statd uanetexception/grafana4-statsd:latest
```

