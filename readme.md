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
