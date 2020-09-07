# mssqlcodes

select EnglishEducation, EnglishOccupation, count(*) as 'Count'   ---step 6
from DimCustomer  ---step 1
where EnglishEducation in ('High School','Bachelors')  --step 2
group by EnglishEducation,EnglishOccupation   --step3
having count(*) >= 50  ---step 4
Order by EnglishEducation ---step 5



select * from DimCustomer

drop table EmpAddress

Create table EmpAddress(
Empid int not null,
Emp_name varchar(100),
Empcity varchar(100)
)

select * from EmpAddress

insert into EmpAddress values(1,'Suraj','Bangalore')
insert into EmpAddress values(2,'Swapna','Belagavi')
insert into EmpAddress(Empid,Emp_name) values(3,'Swapna')

Alter table EmpAddress ADD CONSTRAINT defaultconstraintcity DEFAULT 'BNG' FOR empcity

