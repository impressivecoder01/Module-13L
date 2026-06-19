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

// class two
create table student3(
  student_id serial primary key,
  first_name varchar(50) not null,
  last_name varchar(50) not null,
  age int,
  grade char(2),
  course varchar(50),
  email varchar(100) unique,
  dob date,
  blood_group varchar(5),
  country varchar(50)
)
insert into student3 
(first_name, last_name, age, grade, course, email, dob, blood_group, country)
values
('John', 'Doe', 20, 'A', 'Computer Science', 'john1@example.com', '2004-01-15', 'O+', 'USA'),
('Jane', 'Smith', 21, 'B', 'Mathematics', 'jane2@example.com', '2003-03-22', 'A+', 'UK'),
('Ali', 'Khan', 22, 'A', 'Physics', 'ali3@example.com', '2002-07-10', 'B+', 'Pakistan'),
('Sara', 'Ahmed', 19, 'C', 'Chemistry', 'sara4@example.com', '2005-05-18', 'O-', 'Bangladesh'),
('Tom', 'Brown', 23, 'B', 'Engineering', 'tom5@example.com', '2001-11-30', 'AB+', 'Canada'),
('Emma', 'Wilson', 20, 'A', 'Biology', 'emma6@example.com', '2004-02-25', 'A-', 'Australia'),
('Liam', 'Taylor', 21, 'B', 'IT', 'liam7@example.com', '2003-08-14', 'B-', 'USA'),
('Olivia', 'Thomas', 22, 'A', 'Economics', 'olivia8@example.com', '2002-09-19', 'O+', 'UK'),
('Noah', 'White', 20, 'C', 'History', 'noah9@example.com', '2004-12-05', 'A+', 'USA'),
('Ava', 'Martin', 19, 'B', 'Philosophy', 'ava10@example.com', '2005-06-11', 'B+', 'France'),

('William', 'Clark', 23, 'A', 'Law', 'will11@example.com', '2001-04-03', 'O-', 'USA'),
('Sophia', 'Lewis', 21, 'B', 'Medicine', 'sophia12@example.com', '2003-10-27', 'AB+', 'India'),
('James', 'Walker', 22, 'A', 'Architecture', 'james13@example.com', '2002-01-08', 'A+', 'USA'),
('Mia', 'Hall', 20, 'C', 'Design', 'mia14@example.com', '2004-03-29', 'B-', 'Italy'),
('Benjamin', 'Allen', 24, 'B', 'Statistics', 'ben15@example.com', '2000-07-17', 'O+', 'Canada'),
('Charlotte', 'Young', 19, 'A', 'Arts', 'char16@example.com', '2005-09-21', 'A-', 'Germany'),
('Lucas', 'King', 21, 'B', 'Finance', 'lucas17@example.com', '2003-02-13', 'B+', 'USA'),
('Amelia', 'Wright', 22, 'A', 'Nursing', 'amelia18@example.com', '2002-05-26', 'AB-', 'UK'),
('Henry', 'Scott', 23, 'C', 'Geography', 'henry19@example.com', '2001-08-09', 'O-', 'Australia'),
('Evelyn', 'Green', 20, 'B', 'Psychology', 'eve20@example.com', '2004-11-01', 'A+', 'USA'),

('Alexander', 'Adams', 22, 'A', 'Computer Science', 'alex21@example.com', '2002-06-06', 'B+', 'USA'),
('Harper', 'Baker', 19, 'B', 'Mathematics', 'harper22@example.com', '2005-01-19', 'O+', 'Canada'),
('Daniel', 'Gonzalez', 21, 'C', 'Physics', 'daniel23@example.com', '2003-04-25', 'A-', 'Mexico'),
('Ella', 'Nelson', 20, 'A', 'Chemistry', 'ella24@example.com', '2004-07-30', 'B+', 'UK'),
('Matthew', 'Carter', 23, 'B', 'Engineering', 'matt25@example.com', '2001-03-15', 'AB+', 'USA'),
('Scarlett', 'Mitchell', 22, 'A', 'Biology', 'scarlett26@example.com', '2002-09-05', 'O-', 'Australia'),
('Joseph', 'Perez', 24, 'C', 'Economics', 'joseph27@example.com', '2000-12-12', 'A+', 'Spain'),
('Victoria', 'Roberts', 21, 'B', 'History', 'victoria28@example.com', '2003-06-28', 'B-', 'USA'),
('Samuel', 'Turner', 20, 'A', 'IT', 'samuel29@example.com', '2004-10-10', 'O+', 'UK'),
('Grace', 'Phillips', 19, 'B', 'Arts', 'grace30@example.com', '2005-02-14', 'A-', 'Ireland');
// class three
select first_name, age from  student3;
select * from student3
select first_name as "first Name" from  student3;
select first_name as "first Name", age as user_age from  student3;
select first_name, blood_group, country, age from student3 order by age desc
select first_name, blood_group, country, age from student3 order by age asc
select first_name, blood_group, country, age from student3 order by student_id asc
select first_name, blood_group, country, age from student3 order by student_id desc

// class four
select country from student3
select distinct country from student3
select distinct course from student3
select * from student3 where country = 'UK'
select first_name, age, last_name, course, grade from student3 where country = 'UK'
select first_name, age, last_name, course, grade from student3 where grade = 'A'

// class five
select blood_group, first_name, last_name, country from student3 where blood_group = 'A+'
select * from student3 where country = 'UK' or country = 'USA'
select first_name, last_name, country, course, grade from student3 where (grade = 'A' or grade = 'B') and (course = 'Mathematics' or course = 'History')
select first_name, last_name, country, grade,age from student3 where country = 'USA' and age = '20'
select first_name, last_name, country, grade, age from student3 where (country = 'UK' or country = 'USA') and age >= 20
select first_name, last_name, country, grade, age from student3 where (country = 'UK' or country = 'USA') and age >= 20 

//class six 
select * from student3 where age <= 20
select * from student3 where country != 'USA'
select * from student3 where country <> 'USA'
select * from student3 where country != 'USA' and blood_group = 'O-'
select * from student3 where age between 20 and  22
select * from student3 where age between 20 and  22 and country = 'USA'
select * from student3 where age between 20 and  22 and country = 'USA' and first_name = 'John'
select * from student3 where country = 'USA' or country = 'UK' or country = 'Pakistan'
select * from student3 where country in('USA', 'UK', 'Pakistan')
select * from student3 where course in('Law', 'History', 'Nursing')

//class seven
select * from student3 where first_name like 'J%'
select * from student3 where first_name like '%n'
select * from student3 where first_name like 'J___'
select * from student3 where email like 'j%'
select * from student3 where email like 'J%'
select * from student3 where email Ilike 'J%'

//class eight
--not
select * from student3 where country = 'Bangladesh'
select * from student3 where not country = 'Bangladesh'
select first_name,last_name,email,grade from student3 where not country = 'Bangladesh'
select first_name,last_name,email,grade from student3 where not grade = 'A'
--scaler function
select first_name from student3
select upper(first_name) from student3
select upper(first_name) as first_name_in_upper from student3
select upper(first_name), first_name, age, country from student3
select lower(first_name), first_name, age, country from student3
select concat(first_name, last_name) as "full_name", first_name, age, country from student3

//class nine
--aggregate function
select avg(age) from student3
select max(age) from student3
select min(age) from student3
select sum(age) from student3
select count(first_name) from student3
select count(*) from student3

//15 1
select true = true
select true = false
select null = null
select null <> null
insert into student3 (first_name, last_name, age, grade, course, dob, blood_group, country) values('rohan', 'rahman', 24, 'A', 'Physics', '2003-4-23', 'A+', 'Bangladesh')
select * from student3 where email <> null
select * from student3 where email is null
select * from student3 where email is not null
select coalesce(2, null)
select coalesce(null, 2)
select coalesce(null, null, 2)
select coalesce(3,null, null, 2)
select coalesce(email, 'Not provided') from student3
select first_name, last_name, coalesce(email, 'Not provided') as email2 from student3
select coalesce(email, 'Not provided') as email2 from student3

2
--limit, offset
select * from student3 limit 5
select * from student3 where country in('Bangladesh', 'Nepal', 'UK') limit 3
select * from student3 limit 5 offset 2
select * from student3 limit 5 offset 5
select * from student3 limit 5 offset 5 * 0
select * from student3 limit 5 offset 5 * 1

3
--update
select * from student3
update student3 set email = 'default@mail.com' where email is null
update student3 set email = 'default@mail.com' where email like 'r%'
update student3 set first_name = 'Rohan', age = 24 where student_id = 1
update student3 set grade= 'C' where student_id = 1 or student_id = 2 or student_id = 3;
update student3 set grade= 'A' where student_id = 1 or student_id in (1, 2)
--delete
delete from student3 where grade = 'C'
delete from student3 where grade = 'A' and blood_group = 'O-'
--group by
select country from student3 group by country
select country, avg(age) from student3 group by country
select country, count(*) from student3 group by country
select grade, count(*) from student3 group by grade
--
select course, count(*)  from student3 group by course having count(*) < 1;
select country, avg(age) from student3 group by country having avg(age)> 20

--
create table users(
  id serial primary key, 
  username varchar(50) not null
)

create table posts(
  id serial primary key, 
  title text not null, 
  user_id int references users(id)
)
INSERT INTO posts (title, user_id) VALUES
('First Post by Akash', 1),
('Batash writes about weather', 2),
('Sagor shares sea stories', 3),
('Nodi talks about rivers', 4),
('Another post by Akash', 1);
select title, username  from posts join users on posts.user_id = users.id
select *  from posts join users on posts.user_id = users.id
select posts.id, title, username  from posts join users on posts.user_id = users.id
select p.id, title, username  from posts as p join users on p.user_id = users.id

16
create table employees(
  employee_id serial primary key,
  employee_name varchar(100),
  department_id int references departments (department_id),
  salary decimal(10,2),
  hire_date date
 )

create table departments(
  department_id serial primary key,
  department_name varchar(100)
)

insert into departments (department_name) values
('Human Resources'),
('Finance'),
('Accounting'),
('Marketing'),
('Sales'),
('Information Technology'),
('Customer Support'),
('Research and Development'),
('Operations'),
('Legal')

insert into employees (employee_name, department_id, salary, hire_date) values
('Alice Johnson', 1, 55000.00, '2021-03-15'),
('Bob Smith', 2, 65000.00, '2020-07-22'),
('Charlie Brown', 3, 48000.00, '2022-01-10'),
('Diana Prince', 4, 72000.00, '2019-11-05'),
('Ethan Hunt', 5, 80000.00, '2018-06-30'),
('Fiona Gallagher', 6, 60000.00, '2021-09-18'),
('George Martin', 7, 45000.00, '2023-02-25'),
('Hannah Lee', 8, 90000.00, '2017-12-12'),
('Ian Wright', 9, 52000.00, '2022-05-08'),
('Julia Roberts', 10, 75000.00, '2020-10-14')

select * from employees inner join departments on employees.department_id = departments.department_id
select * from employees as e inner join departments as d on e.department_id = d.department_id
select * from employees inner join departments using(department_id)

select department_name, avg(salary) from employees inner join departments using(department_id) group by department_name
select department_name, round(avg(salary)) from employees inner join departments using(department_id) group by department_name
select department_name, count(*) from employees inner join departments using(department_id) group by department_name
select department_name, round(avg(salary)) as avg_salary from employees join departments using(department_id) group by  department_name order by avg_salary desc limit 1


select extract(year from hire_date) as hired_year from employees group by hired_year
select extract(year from hire_date) as hired_year, count(*) from employees group by hired_year

select max(salary) from employees2
select * from employees2 where salary = 70000
select * from employees2 where salary = (select max(salary) from employees2)
select * from employees2 where salary > (select avg(salary) from employees2)
select * from employees2 where salary = (select max(salary) from employees2 where department = 'IT')