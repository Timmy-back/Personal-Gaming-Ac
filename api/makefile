.PHONY: up down restart build migrate rollback fresh logs
    make migration name=add_status_and_phone_to_users_table

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

migration:
	docker compose exec app php artisan make:migration $(name)

rollback:
	docker compose exec app php artisan migrate:rollback

fresh:
	docker compose exec app php artisan migrate:fresh --seed

logs:
	docker compose logs -f
