PHONY: start

start:
	docker build -t ansible . && \
		docker run --name ansible -d ansible sleep infinity


PHONY: first

first:
	docker exec ansible ansible-playbook file_change.yml


PHONY: second

second:
	docker exec ansible ansible-playbook caddy_deploy.yml


