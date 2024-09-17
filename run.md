export DB_URL=postgres://ecommerce:ecommerce@localhost:5432/users_db?sslmode=disable
goose -dir ./sql/schema/ postgres $DB_URL up 


goose -dir ./sql/schema/ postgres "postgres://ecommerce:ecommerce@localhost:5432/users_db?sslmode=disable" up 

docker run -p 8001:8080 --env-file .env-dev ecommerce_user
