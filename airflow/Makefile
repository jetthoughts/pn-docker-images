NAME := pubnative/airflow
COMMIT := $$(git log -1 --pretty=%h)
VERSIONED := ${NAME}:${COMMIT}
LATEST := ${NAME}:latest
 
all: build push

.PHONY: build
build:
	docker build --rm . -t ${VERSIONED}
	docker tag ${VERSIONED} ${LATEST}

.PHONY: push
push:
	docker push ${VERSIONED}
	docker push ${LATEST}
