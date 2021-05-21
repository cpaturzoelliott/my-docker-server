CONTAINERS=wireguard pihole unbound nginx-proxy

help:
	@echo "-------------------------------------"
	@echo ""
	@echo "my-docker-server Makefile arguments:"
	@echo ""
	@echo "-------------------------------------"
	@echo ""
	@echo "run \t- runs docker-compose up"
	@echo "detached \t- runs docker-compose up -d"
	@echo "nuke \t- forcefully removes all the containers: $(CONTAINERS)"
	@echo ""

run:
	@echo "Running docker-compose up"
	docker-compose up

detached:
	@echo "Running docker-compose up -d"
	docker-compose up -d

nuke:
	@echo "Removing all containers"
	docker container rm -f $(CONTAINERS)
