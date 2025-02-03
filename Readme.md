# Tarea12SXE - Pedro Piñeiro Ordax

## Apartado 1

Entramos en el pgAdmin y nos conectamos a la base de datos de odoo, una vez dentro vamos a crear las tablas de forma manual, vamos a Tablas y creamos una, insertando los datos solicitados
![ej1](imgs/ej1.png)

## Apartado 2

Para insertar 5 registros ponemos esta query
![ej2](imgs/ej2.png)

Para comprobarlo le damos a ver todas las tablas en EmpresasFCT
![ej2-2](imgs/ej2-2.png)

## Apartado 3

En el apartado de query escribimos esto
```sql
select * from "EmpresasFCT" order by "fechaContacto" desc;
```
![ej3](imgs/ej3.png)

## Apartado 4

```sql
select "name", "city", "commercial_company_name" 
from public.res_partner 
where "city" = 'Tracy'
order by "name";
```
![ej4](imgs/ej4.png)

## Apartado 5

```sql
SELECT DISTINCT ON ("invoice_partner_display_name") 
    "invoice_partner_display_name", 
    "name", 
    "invoice_date", 
    "amount_untaxed"
FROM public.account_move
WHERE "move_type" = 'out_refund'
ORDER BY "invoice_partner_display_name", "invoice_date" DESC;
```
![ej4](imgs/ej5.png)