# Postgres-setup-staging-area
setting up a staging area in postgresql - for a toll-tax firm  

## Aim:

* Setup a  server for a data warehouse
* Create the schema to store the dataset
* Load the data into the tables
* Verify loaded data

## Tool;
* Postgresql

## Process:
* start server - start_postgres
* create db - createdb -h localhost -U postgres -p "port no" "DB name"
* create the fact and dimension tables - psql  -h localhost -U postgres -p "port no" "DB name" < star-schema.sql
* Load dimension tables - psql  -h localhost -U postgres -p "port no" "DB name" < DimCustomer.sql
* Load data into fact table - psql  -h localhost -U postgres -p "port no" "DB name" < FactBilling.sql
* verify in terminal with  verify.sql
