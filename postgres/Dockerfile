# Використовуємо офіційний образ PostgreSQL
FROM postgres:latest

# Налаштовуємо змінні середовища для бази даних
ENV POSTGRES_USER myuser
ENV POSTGRES_PASSWORD mypassword
ENV POSTGRES_DB mydb

# Переносимо SQL скрипти для ініціалізації бази даних
COPY init.sql /docker-entrypoint-initdb.d/
