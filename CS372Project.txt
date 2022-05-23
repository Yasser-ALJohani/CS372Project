/*
create database clothing_go

use clothing_go

create table Account(birth_data date not null ,Email varchar(20) not null primary key , password varchar(30) not null ,
country varchar(20) , city varchar(20) , dist varchar(20))

create table user_account(UserEmail varchar(20) not null foreign key (UserEmail) references Account(Email) on update cascade ,
UserID varchar(30) not null 
primary key(UserEmail ,UserID))

create table user_table(userID varchar(30) not null  , user_password int not null , user_Email varchar(30) not null ,
primary key (userID,user_Email))

create table Payment( pay_invoice varchar (255) Not null primary key  , pay_method varchar(20) Not null, DT Datetime )


create table order_table(item_price money not null , order_ID int not null primary key , 
item_type varchar(30) not null , item_name varchar(30) not null  , item_size varchar(3) not null)

create table Product (product_name varchar (250) Not null , product_description varchar(250) Not null , 
product_type varchar(50) Not null   
primary key ( product_name, product_description,product_type))

INSERT INTO Account VALUES ('1995-10-01','abcd@gmail.com',1234,'K','riyadh','alia');
INSERT INTO Account VALUES ('1997/11/08', 'efgh@gmail.com', 5678 , 'KSA' ,'makhaa' ,'awali');
INSERT INTO Account VALUES ('1985/12/01', 'ijkl@gmail.com', 0910 , 'UEA' ,'dubi' ,'sharg');
INSERT INTO Account VALUES ('1983/10/05', 'mnop@gmail.com', 1112 , 'UEA' ,'ajmaan' ,'darb');
INSERT INTO Account VALUES ('1993/09/09', 'qrst@gmail.com', 1314 , 'USA' ,'LA' ,'west');
-------------------------------------------------------------------------------------------
insert into order_table values(44 , 7159 , 'T-shirt' , 'NSTYLE' , 'M')
insert into order_table values(259.45 , 1458 , 'Shoes' , 'NIKERT' , '40')
insert into order_table values(144.55 , 8954 , 'Pants' , 'ADIDATRIO' , '38')
insert into order_table values(850 , 9458 , 'Jacket' , 'LAGRECA' , '48')
insert into order_table values(87.50 , 2546 , 'Belt' , 'LeatherBelt' , '34')
-------------------------------------------------------------------------------------------

Insert into Product values ('Button-Down Collar Shirt', 'Shirt Light Blue' ,'Shirt')
Insert into Product values ('Checkered Overshirt Grey', 'Grey Shirt ' ,'Shirt')
Insert into Product values ('Bravada Core', 'Sneakers Black/White' ,'Shoes')
Insert into Product values ('PUMA sport', ' Style Core Court Pure Black/White' ,'Shoes')
Insert into Product values ('Essential Cargo Pants', 'Tommy Hilfiger' ,'Pants')
-------------------------------------------------------------------------------------------
Insert into Payment Values ('Price = 105','credit card','2021-5-7  10:50:30')
Insert into Payment Values ('Price = 850','Apple Pay','2021-5-7  11:52:40')
Insert into Payment Values ('Price = 360','VISA ','2021-5-7  12:30:42')
Insert into Payment Values ('Price = 1500','Apple Pay','2021-5-7  10:20:58')
Insert into Payment Values ('Price = 4200','VISA','2021-5-7  10:33:22')

select * from order_table 
select * from Product
select * from Payment

select sum (item_price) as 'Sum of Prices' from order_table 
select avg (item_price) as 'Average Price' from order_table 
select max (item_price) as 'Max Price'  from order_table
select min (item_price) as 'Min Price' from order_table
select count (item_price) as 'Number of Values' from order_table 

select item_price as 'Price' , order_id as 'ID' , item_type as 'Type' , item_name 'Name'
 , item_size 'Size' from order_table 

select sum (item_price) as 'Sum of Prices' from order_table 
select avg (item_price) as 'Average Price' from order_table 
select max (item_price) as 'Max Price'  from order_table
select min (item_price) as 'Min Price' from order_table
select count (item_price) as 'Number of Values' from order_table 
*/