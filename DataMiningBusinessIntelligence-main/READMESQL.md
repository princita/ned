# SQL Basics
used for 

1-storing and 
2-managing data
RDBMS

It not case sensitive.

# Types of SQL Commands
• There are five types of SQL commands: DDL, DML,
DCL, TCL, and DQL.
![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/f0a99f73-3001-46fd-9eb0-50d91e9edbaa)

  <table>
    <thead>
      <tr>
        <th>Index</th>
        <th>View</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>create Unique index index_name on table_name</td>
            <td>create View Detail view as select name,address from stu_detail</td>
        </tr>
        <tr>
            <td>Drop index index_name</td>
            <td>Drop view view_Name</td>
        </tr>

    </tbody>
  </table>
  
  # sub-query 
outer query ->main query 
inner query ->sub query 
unique/not exist/ exist/not in/some/all

insert into Employfrom`ee_BMP
select * from Employee
where ID IN (select ID from Employee)

# SQL Clause
![image](https://github.com/princit/DataMiningBusinessIntelligence/assets/29123911/07970c59-7753-4e7f-badc-9c6a16be64a9)

# Join


  <table>
    <thead>
      <tr>
        <th>Inner Join</th>
        <th>Left Join</th>
        <th>Right Join</th>
        <th>Full Join</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>matching Value in both table</td>
            <td>return All value from left table only matching value in right table </td>
            <td>return All value from right table only matching value in left table </td>
            <td>return combination of right and left outer join ,Put null where match not found</td>
        </tr>
    </tbody>
  </table>
 
  # Operation
  <table>
    <thead>
      <tr>
        <th>Union</th>
        <th>Intersection</th>
        <th>Minus</th>
        <th>Except</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>Eliminate duplicate row</td>
            <td>common row form both </td>
            <td>Present first but absent in second </td>
            <td>return combination of right and left outer join ,Put null where match not found</td>
        </tr>
        <tr>
            <td>select * from first union select * from second</td>
            <td>select * from first intersection select * from second</td>
            <td>select * from first minus select * from second</td>
            <td>select * from first except select * from second</td>
        </tr>
    </tbody>
  </table>


mysql -u yourdbuser -p Yourdbbase

  # Cartisean Product
  <table>
    <thead>
      <tr>
        <th>Where</th>
        <th>Join</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>select * from instructor,teacher where instructor.ID = teacher.ID</td>
            <td>select * from Epmployee inner join project on project.Emp_ID = Employee.Emp_ID </td>
        </tr>
    </tbody>
  </table>

select name from instructor where salary between 90 and 100

  # Tuple Comparision

  select name,course_id from intructor,teacher where (instructor.ID,dept_name) = (Teacher.ID,"Bilogy")

  insert into table1 select * from table1

  # Updates with Scalar Subqueries
  <table>
    <thead>
      <tr>
        <th>Where</th>
        <th>Join</th>
      </tr>
    </thead>
    <tbody>
        <tr>
            <td>update instructor set salary = case when salary <= 100 then salary*1.05 else salary*103 end</td>
            <td>update student s set tot_cred = (select sum(credits) from takes,course where take.cource_id=cource.course _id and s.ID = take.ID and take.grade<'F' and takes.grade is not null) </td>
        </tr>
    </tbody>
  </table>

  # Assignment
  CREATE TABLE students(
   student_id   INT              NOT NULL,
   name VARCHAR (20)     NOT NULL,
   age  INT              NOT NULL,
   grade  CHAR (25) ,    
   PRIMARY KEY (student_id)
);

UPDATE students
SET age = 777
WHERE student_id = 2;

UPDATE students SET grade = 'APlus' WHERE age > 85;

DELETE FROM `students` WHERE student_id = 3

DELETE FROM `students` WHERE grade <'C';

CREATE TABLE courses(
   course_id INT              NOT NULL,
   course_name VARCHAR (20)     NOT NULL,
   instructor CHAR (25) ,    
   PRIMARY KEY (course_id)
);

CREATE TABLE enrollments (
   enrollment_id INT          NOT NULL,
   student_id INT         NOT NULL,
   course_id INT      NOT NULL,
   PRIMARY KEY (enrollment_id),
 FOREIGN KEY (  course_id) REFERENCES courses(course_id)
);

ALTER TABLE enrollments ADD semester varchar(255);

ALTER TABLE enrollments ADD CONSTRAINT fk_student_enrollment FOREIGN KEY (student_id) REFERENCES students (student_id);

GRANT SELECT, UPDATE, INSERT,DELETE ON students TO root;

REVOKE DELETE ON students FROM root;

SELECT AVG(age) FROM `students` WHERE 1;

SELECT COUNT(*) FROM `students` WHERE grade != 'F';

# •	Write a query to retrieve all students who have enrolled in a specific course.
SELECT students.student_id, students.name FROM students JOIN enrollments ON students.student_id = enrollments.student_id JOIN courses ON enrollments.course_id = courses.course_id;

Perform joins:
# •	Write a query to retrieve a list of students along with the courses they are enrolled in.
SELECT students.student_id, students.name, courses.course_id, courses.course_name FROM students JOIN enrollments ON students.student_id = enrollments.student_id JOIN courses ON enrollments.course_id = courses.course_id;

# •	Write a query to retrieve a list of courses along with the names of the students enrolled in each course.
SELECT courses.course_id, courses.course_name, students.student_id, students.name FROM courses JOIN enrollments ON courses.course_id = enrollments.course_id JOIN students ON enrollments.student_id = students.student_id;

# Normailization

# 1NF (First Normal Form) Rules
Each table cell should contain a single value.
Each record needs to be unique.

# 2. Second Normal Form (2NF)
For a table to be in the Second Normal Form,

It should be in the First Normal form.

And, it should not have Partial Dependency.(primary key depandant on other cloumn)

# 3. Third Normal Form (3NF)
A table is said to be in the Third Normal Form when,

It satisfies the First Normal Form and the Second Normal form.

And, it doesn't have Transitive Dependency.(Any column depandant on other cloumn)

# For a table to be in BCNF, the following conditions must be satisfied:

R must be in the 3rd Normal Form

and, for each functional dependency ( X → Y ), X should be a Super Key.
# 5. Fourth Normal Form (4NF)
A table is said to be in the Fourth Normal Form when,

It is in the Boyce-Codd Normal Form.

And, it doesn't have Multi-Valued Dependency.

# 5. Fifth Normal Form (5NF)
The fifth normal form is also called the PJNF - Project-Join Normal Form

It is the most advanced level of Database Normalization.

Using Fifth Normal Form you can fix Join dependency and reduce data redundancy.

It also helps in fixing Update anomalies in DBMS design.
