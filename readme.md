//first class
create table employe(
  id serial,
  name varchar(100),
  age int
);
alter table employe rename to employee
alter table employee add column email varchar(50) 
alter table employee drop column email
alter table employee rename column name to username;
alter table employee alter column username type varchar(50)
alter table employee alter column email set not null
alter table employee alter column email drop not null
insert into employee (username, age,email) values ('mrzafor.', 203,'tester100@gmail.com')
alter table employee alter column email set default 'tester@gmail.com'
alter table employee add constraint unique_employee_email unique(email)
alter table employee alter column email drop default
alter table employee add constraint pk_employee_id primary key(id)
alter table employee drop constraint unique_employee_email;

