# ecommerce-infra

Ecommerce infrastructure: Eureka discovery server, API gateway, and local Docker services.

## Local PostgreSQL

From this directory:

```bash
docker compose up -d
```

- **Default DB:** `products` (matches `product-service` `application.properties`)
- **User / password:** `ecommerce` / `ecommerce`
- **Extra DBs** (created on first init): `orders`, `inventory` — edit `postgres/init/02-additional-databases.sql` to add more

Add databases by extending that SQL file, then recreate the volume (`docker compose down -v`) if you need scripts to re-run.
