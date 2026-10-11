.PHONY: up down restart build migrate rollback fresh logs

up:
	docker compose up -d

down:
	docker compose down

restart:
	docker compose down
	docker compose up -d

build:
	docker compose up -d --build

migrate:
	docker compose exec app php artisan migrate

rollback:
	docker compose exec app php artisan migrate:rollback

fresh:
	docker compose exec app php artisan migrate:fresh --seed

logs:
	docker compose logs -f
