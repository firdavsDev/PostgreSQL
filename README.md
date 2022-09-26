## PSQL short commands
```
\l   -   list of databases
\du  -   list of roles (users)
\c {database_name}   -   change or connect to database
\d   -   list of tables with indexes
\dt  -   list of tables withous indexes
\d {table_name} - details of table
```
#
## Date types
```
text: 
	varchar() - Limit bo'lganda ishlatiladi
	text - Limit bo'lmaganda ishlatiladi
	char() - varchardan farqi kiritilgan son nechi bo'lsa o'shancha simbol saqlanadi. Agar kiritilgan so'z kichik bo'lsa yoniga space qo'shib saqlaydi.
```
```	
integer:
	INT - (-2.147.483.648) dan (2.147.483.647) gacha 
	SMALLINT - (-32.768) dan (32.767) gacha
	BIGINT - (-9223372036854775808) dan (9223372036854775807) gacha bo'lgan butun sonlarni saqlash.
```
```	
numeric:
	NUMERIC(5,2) - umumiy sonlar 5 ta, nuqtadan so'ng 2 ta son (123.45 yoki 456.98)
	NUMERIC(5) - umumiy sonlar 5 ta, nuqtadan so'n 0 ta son 
	NUMERIC - xoxlagan qiymatni saqlash uchun.
```
```	
floating numbers:
	REAL, DOUBLE PRECISION - real 4 bytes, double precision 8 bytes
	Hisob kitob muhim bo'lganda numeric ishlatish maslahat beriladi.
```
```
datetimes:
	DATE - sanalar uchun: 2021-10-12
	TIME - vaqt uchun: 10:25:40
	TIMESTAMP - ham sana ham vaqt uchun : 2021-10-12 10:25:40
```
```
others:
	SERIAL, SMALLSERIAL, BIGSERIAL - auto_increment uchun (table_id SERIAL PRIMARY KEY).
	BOOLEAN - True or False
```		
#		
## Alter table

#### Example:
```
ALTER TABLE book ADD COLUMN id SERIAL PRIMARY KEY;
```
```
ALTER TABLE book RENAME TO my_book;
```
```
ALTER TABLE book RANAME {column_name} TO {new_column_name}; -- change name of column
```
```
ALTER TABLE book ALTER COLUMN {column_name} TYPE VARCHAR(90); -- change type of column
```
```
ALTER TABLE book ALTER COLUMN amount SET NOT NULL; -- change nullable of column
```
```
ALTER TABLE book DROP COLUMN {column_name}; -- delete column
```
