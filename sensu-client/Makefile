.PHONY: build test
newtag ?= latest
registryUrl ?= registry.service.dsd.io
image = ${registryUrl}/opguk/sensu-client

build:
	docker build -t "${image}:latest" .
	docker tag "${image}:latest" "${image}:${newtag}"

clean:
	@eval `docker-machine env default` ||:
	@docker kill `docker ps -a -q` ||:
	@docker rm -f -v `docker ps -a -q` ||:
	@docker rmi -f `docker images -q` ||:
	
test:
	env NAME=$(image) VERSION=$(newtag) ./test