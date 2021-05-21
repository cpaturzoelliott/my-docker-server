CONTAINERS=wireguard pihole unbound nginx-proxy

help:
	@echo "-------------------------------------"
	@echo ""
	@echo "my-docker-server Makefile arguments:"
	@echo ""
	@echo "-------------------------------------"
	@echo ""
	@echo "run \t\t- runs docker-compose up"
	@echo "detached \t- runs docker-compose up -d"
	@echo "nuke \t\t- forcefully removes all the containers and their data: $(CONTAINERS)"
	@echo "rebuild \t- runs nuke then detached"
	@echo ""
	@echo ""
	@echo "-------------------------------------"
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
	rm -rf etc-dnsmasq.d/01-pihole.conf
	sudo rm -rf etc-nginx
	sudo rm -rf etc-pihole
	sudo rm -rf etc-unbound/unbound.pid
	sudo rm -rf etc-unbound/dev
	sudo rm -rf etc-unbound/var
	rm -rf wireguard-config

rebuild:
	make nuke
	make detached
