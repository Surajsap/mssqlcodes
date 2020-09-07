select EnglishEducation, EnglishOccupation, count(*) as 'Count'   ---step 6
from DimCustomer  ---step 1
where EnglishEducation in ('High School','Bachelors')  --step 2
group by EnglishEducation,EnglishOccupation   --step3
having count(*) >= 50  ---step 4
Order by EnglishEducation ---step 5



select * from DimCustomer

drop table EmpAddress

Create table EmpAddress1(
Empid int not null,
Emp_name varchar(100),
Empcity varchar(100),
Empage int
)

select * from EmpAddress

drop table empaddress

insert into EmpAddress values(1,'Suraj','Bangalore')
insert into EmpAddress values(2,'Swapna','Belagavi')
insert into EmpAddress(Empid,Emp_name) values(3,'Swapna')
---default constraints
Alter table EmpAddress ADD CONSTRAINT defaultconstraintcity DEFAULT 'BNG' FOR empcity
----check constraints
Alter table empaddress1 add constraint checkage check (Empage >16 and Empage <125) 

insert into EmpAddress1 values(1,'Suraj','Bangalore',25)
insert into EmpAddress1 values(2,'Swapna','Belagavi',19)

select * from EmpAddress1

Create table EmpAddress(
Empid int Primary key,
Emp_name varchar(100),
Empcity varchar(100),
Empage int
)

insert into EmpAddress values(1,'Suraj','Bangalore',25)
insert into EmpAddress values(2,'Swapna','Belagavi',19)
insert into EmpAddress values(3,'Swapna','Belagavi',29)
insert into EmpAddress values(4,'Sneha','Bangalore',32)

select * from EmpAddress

delete from EmpAddress where Empid =2

--to delete data in table
delete from EmpAddress

---unique key constraint

alter table empaddress add constraint Uniquevalue Unique(Empid)

---Identtity vaalue

create table identityvalue(
id int identity(1,1)not null,
firstname nvarchar(100),
Lastname varchar(100)
)

insert into identityvalue values('Suraj','Patil')
insert into identityvalue values('Swapna','Deshpande')
insert into identityvalue values('Sneha','Deshpande')

select * from identityvalue






