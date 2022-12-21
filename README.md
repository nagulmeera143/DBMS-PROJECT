# DBMS-PROJECT
Here is the code of my final project of data base management system.

-- FIRST WE NEED TO CREATE TABELS, here i created 3 tables named PRODUCT, DEPOT, STOCK.

create table Product(prod varchar(50) not null primary key, pname varchar(50), price varchar(50));
create table Depot(dep varchar(50) not null primary key, addr varchar(50), volume varchar(50));
create table Stock( prod varchar(50), dep varchar(50), quantity varchar(50), foreign key(dep) references Depot(dep) on delete cascade on update cascade, foreign key(prod) references Product(prod) on delete cascade on update cascade);


-- AFTER TABLES ARE CREATED WE NEED TO INSERT THE VALUES INTO THE TABLES
-- insert is the method to which is used to insert the values into the tables.
-- the inserted values are taken from quesion bank.


-- HERE I DID INSERT VALUES INTO THE PRODUCT

insert into Product values('p1','tape','2.5');
insert into Product values('p2','tv','250');
insert into Product values('p3','vcr','80');

-- HERE I INSERTED VALUES INTO THE DEPOT

insert into Depot values('d1','New York','9000');
insert into Depot values('d2','Syracuse','6000');
insert into Depot values('d4','New York','2000');

-- HERE I INSERTED VALUES INTO THE STOCK

insert into Stock values('p1','d1','1000');
insert into Stock values('p1','d2','-100');
insert into Stock values('p1','d4','1200');
insert into Stock values('p3','d1','3000');
insert into Stock values('p3','d4','2000');
insert into Stock values('p2','d4','1500');
insert into Stock values('p2','d1','-400');
insert into Stock values('p2','d2','2000');

-- UPDATE is useful to update or manipulate the data which is already in the table, we can update the elements from one value to oters.

--THIS IS THE QUIERY LINE TO UPDATE THE ELEMENT OF 'P1' TO 'PP1' IN THE PROD COLUMN OF PRODUCT TABLE.
update product set prod = 'pp1' where prod = 'p1';

--THIS IS THE QUIERY LINE TO UPDATE THE ELEMENT OF 'd1' TO 'dd1' IN THE PROD COLUMN OF PRODUCT TABLE.
update depot set dep = 'dd1' where dep = 'd1';


-- SELECT is uselful to show the output of the the selected items

select * from product;
select * from depot;
select * from stock;
