build:
	docker compose \
		-f data_lakehouse/docker-compose.yaml build dremio minio nessie

up:
	docker compose \
		-f data_lakehouse/docker-compose.yaml up dremio minio nessie -d

down:
	docker compose \
		-f data_lakehouse/docker-compose.yaml down dremio minio nessie
