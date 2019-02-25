SHELL := /bin/bash
VERSION_TAG=$(shell git rev-parse --short HEAD)

.PHONY: help
help: ## This help message
  @echo -e "$$(grep -hE '^\S+:.*##' $(MAKEFILE_LIST) | sed -e 's/:.*##\s*/:/' -e 's/^\(.\+\):\(.*\)/\\x1b[36m\1\\x1b[m:\2/' | column -c2 -t -s :)"

.PHONY: build
build: ## Build the Docker images
  docker-compose build
