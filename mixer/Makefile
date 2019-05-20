TAG := 1.0.0
IMG ?= vasylk/logviewer-mixer

all: push

build:
	CGO_ENABLED=0 go build .
	docker build -t $(IMG):$(TAG) .
	@echo Built $(IMG):$(TAG)

run: 
	docker run -p 17655:17655 --network=host $(IMG):$(TAG)

push: build
	docker push $(IMG):$(TAG)
@echo Pushed $(IMG):$(TAG)
