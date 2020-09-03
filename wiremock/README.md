# Simple Wiremock Docker
A simple docker image based on java 8 to start a standalone [wiremock](http://wiremock.org/) container. For more information on running wiremock as a standalone process please visit [wiremock running as standalone](http://wiremock.org/docs/running-standalone/).

## Samples

### Starting a "Hello World" docker container

```sh
git clone https://github.com/Tanevski3/simple-wiremock-docker.git

cd simple-wiremock-docker

docker build -f Dockerfile \
	         -t simple-wiremock:0.1 .

docker run -it --rm \
  -p 8080:8080 \
  simple-wiremock:0.1
```