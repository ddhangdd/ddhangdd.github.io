---
layout: default
title: Portfolio
---

# Portfolio

---

## Learning Purpose 

* Using iloc, loc to select rows and columns in Pandas DataFrames
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1iv6JsO0EYHJA8MJErj1iYTGR_87XlmGA)
This colab covers how to use iloc and loc with Pandas. Inspired by  [Lynn](https://www.shanelynn.ie/select-pandas-dataframe-rows-and-columns-using-iloc-loc-and-ix/#comments)
	

---
	
## Technical Project

- [Edugression](https://ddhangdd.github.io/Edugression/)
- [Stock Market Prediction](https://ddhangdd.github.io/Stock%20Market%20Prediction/)
- [Neural Networks and CSPs](https://ddhangdd.github.io/portfolio/SQL)
- [Project 4 Title](http://example.com/)
- [Project 5 Title](http://example.com/)

---

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
