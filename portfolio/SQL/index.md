---
layout: default
title: SQL
---

# SQL!



```sql
CREATE TABLE student (   
    student_id INT PRIMARY KEY,
    name VARCHAR(20),
    major VARCHAR(20)
);

DESCRIBE student;

DROP TABLE student;


ALTER TABLE student ADD GPA DECIMAL(3,2); #total digit, 2 after .

ALTER TABLE student DROP COLUMN GPA;

SELECT * FROM student;



INSERT INTO student VALUES(1,'Jack', 'Biology');
INSERT INTO student VALUES(2,'Kate', 'Sociology');
INSERT INTO student(student_id, name) VALUES(10,'Claire');
INSERT INTO student VALUES(4,'Jack', 'Biology');
INSERT INTO student VALUES(5,'Mike', 'CS');


#start over

--schema is like a framework, then you insert data
CREATE TABLE student (   
    student_id INT PRIMARY KEY,
    name VARCHAR(20) ,
    major VARCHAR(20) DEFAULT 'undecided' #constraint
);

CREATE TABLE student (   
    student_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(20) ,
    major VARCHAR(20) DEFAULT 'undecided'
);

INSERT INTO student(name, major) VALUES('Claire', 'CS');
INSERT INTO student(name, major) VALUES('Claire', 'CS');
INSERT INTO student(name, major) VALUES('Claire', 'CS');




##----update and delete
SELECT * FROM student;

INSERT INTO student VALUES(1,'Jack', 'Biology');
INSERT INTO student VALUES(2,'Kate', 'Sociology');
INSERT INTO student VALUES(3,'Claire', 'CS');
INSERT INTO student VALUES(4,'Jack', 'Biology');
INSERT INTO student VALUES(5,'Mike', 'CS');


UPDATE student 
SET major = "Bio"
WHERE major = "Biology";


UPDATE student 
SET major = "Random major"
WHERE student_id = "4";

UPDATE student 
SET major = "Biochemistry"
WHERE major = "Biology" OR major = "CS";

UPDATE student 
SET name = "Tom", major = "Biochemistry"
WHERE student_id = "4";

UPDATE student 
SET major = "Undecided"; #apply to all data


#------delete

DELETE FROM student; #delete all row

DELETE FROM student  #delete specific row
WHERE student_id = 5;

DELETE FROM student  #delete specific row
WHERE major = 'undecided' AND name = "Tom";


#---- basic queries e.g. select 


```
---
