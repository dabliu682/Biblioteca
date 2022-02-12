### Crear backup de una base de datos en postgres
> pg_dump -O --dbname=postgresql://postgres:123@localhost:5434/SABERPRO-2011-2014 > SABERPRO-2011-2014.sql
### Crear backup de una tabla en postgres
> pg_dump -h localhost -p 5434 -U postgres -t saberpro_final -F p -b -v -f "/Temp/saberpro_final.sql" SABERPRO-2011-2014
### Buscar duplicados entre dos tablas
> select DISTINCT(id) from encontrados as f where not exists (select id from tmpterceros as d where f.id=d.id)
### Crear copia de tabla
> create table tmpdos as SELECT id from terceros
