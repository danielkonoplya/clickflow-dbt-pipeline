
# clickflow-dbt-pipeline

## Описание

**`clickflow-dbt-pipeline`** — это простой, но гибкий проект для построения ETL/ELT-процессов с использованием Apache Airflow, ClickHouse, PostgreSQL и dbt.

Проект подойдёт для:

- быстрого запуска прототипов пайплайнов  
- аналитики и построения витрин данных  
- тренировок и демонстрации инженерных подходов  

Он объединяет проверенные инструменты для оркестрации, хранения и трансформации данных, упакованные в контейнеры через Docker Compose.

## Состав

- **Apache Airflow** — управление задачами и расписаниями  
- **ClickHouse** — высокопроизводительное аналитическое хранилище  
- **PostgreSQL** — база данных для Airflow и staging  
- **dbt-postgres** — SQL-трансформации через dbt  

## Запуск

```bash
docker-compose up --build
```

После запуска:

- **Airflow:** http://localhost:8080  
- **ClickHouse:** http://localhost:8123  
- **PostgreSQL:** `localhost:5433`

## Структура проекта

- `dags/` — DAG-файлы для Airflow  
- `dbt/` — проект для dbt (если используется)  
- `Dockerfile` — расширяет Airflow, добавляя dbt  
- `docker-compose.yml` — конфигурация всех сервисов  
