run:
	docker run \
	-it --rm \
	--network mongodb \
	--name rest-server \
	-p 8000:8000 \
	-e e04d2ff2bc92cd5cfc920566ebba00b5335f8d6a35b0a1f7c664970f01ebbb7a=mongodb://mongodb:27017/notes \
	node-docker
.PHONY: run