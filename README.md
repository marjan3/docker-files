# Dockerfiles
**Dockerfiles** is a collection of useful docker files that can be reused. 

```
$ docker build -t .
$ docker run -it --rm -p 8080:8080 service:0.1
```

or

```
$ docker compose up -d .
```

## Prerequisites
* Bash

## Guide

### `wiremock`

A simple docker image based on java 8 to start a standalone [wiremock](http://wiremock.org/) container. For more information on running wiremock as a standalone process please visit [wiremock running as standalone](http://wiremock.org/docs/running-standalone/).

### `grafana-prometheus-loki` 

Change `prometheus/prometheus.yml` to point to the metrics endpoint

```
    ...
  - job_name: 'service-example'
    static_configs:
      - targets:
          - 'localhost:8080'
    ...
```


## Contact

For contact, you can reach me at [marjantanevski@outlook.com](marjantanevski@outlook.com).

## License

MIT © [Marjan Tanevski](marjantanevski@outlook.com)
