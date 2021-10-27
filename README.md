[![forthebadge](https://forthebadge.com/images/badges/contains-technical-debt.svg)](https://forthebadge.com) [![forthebadge](https://forthebadge.com/images/badges/powered-by-coffee.svg)](https://forthebadge.com) [![forthebadge](https://github.com/iaks23/People-Analytics-Case-Study/blob/main/img/built-with-postgresql.svg)](https://forthebadge.com)

# 👨‍👩‍👧‍👦 People Analytics Case Study

> A HR analytics case study performed as part of the [SeriousSQL](https://www.datawithdanny.com) course by [Danny Ma](https://www.linkedin.com/in/datawithdanny/).

[![view-repo](https://img.shields.io/badge/View-Repo-blueviolet)](https://github.com/iaks23?tab=repositories)
[![view-profile](https://img.shields.io/badge/Go%20To-Profile-orange)](https://github.com/iaks23)

### 💡 Don't Forget To
 
- [ ] Star This Repo 🌟
- [x] Stay hydrated 🥤
- [x] Be awesome 💃🏻

## Table of Contents 📖
* 📂 [Exploring Datasets](#datasets)
      * 🔭[Tables](#tables)
* 🌟 [Something Else](#whatevs)






# 📁 Exploring Datasets <a name='datasets'> </a>

For the purpose of this case study, we've been provided with 6 tables, the relationship between these tables can be explained with the ERD below.

![ERD](https://github.com/iaks23/People-Analytics-Case-Study/blob/main/img/ERD.png)

> ‼️ HR Analytica has let us know that The date fields in the tables were accidentally input with incorrect year values due to a young intern accidentally messing up their data entry process! This has to be fixed before moving onto the business requirements! 

### 🔭 Closer view of the tables <a name='tables'></a>

#### `employee`

> Provides personal details of the employees that work, each identified uniquely by an employee id.

```sql
SELECT *
FROM employees.employee
LIMIT 3;
```

|id|	birth_date|	first_name|	last_name|	gender|	hire_date|
|---|---|---|---|---|---|
|10001|	1953-09-02|	Georgi|	Facello| M |1986-06-26|
|10002|	1964-06-02|	Bezalel|	Simmel|	F	|1985-11-21|
|10003|	1959-12-03|	Parto|	Bamford|	M|	1986-08-28|

> ‼️ Issue: Our young unlucky intern accidentally input the year which is 18 years behind what it should be

#### `title`

> Joins with the emmployee table on id column and provides the title held along with its duration for eac employee.

```sql
SELECT *
FROM employees.title
WHERE employee_id = 10005
ORDER BY from_date;
```
|employee_id|	title|	from_date|	to_date|
|---|---|---|---|
|10005|	Staff|	1989-09-12|	1996-09-12|
|10005|	Senior Staff|	1996-09-12|	9999-01-01|

> ‼️ Issue: Date field messed up here as well, we might need to add on our 18 years to every other single value. 

#### `salary`

> Joins with the emmployee table on id column and provides the salary earned by them for a particular time period.

```sql
SELECT *
FROM employees.salary
WHERE employee_id = 10005
ORDER BY from_date;
```
|employee_id|	amount|	from_date|	to_date|
|---|---|---|---|
|10005|	78,228|	1989-09-12|	1990-09-12|
|10005|	82,621|	1990-09-12|	1991-09-12|

> ‼️ Issue: Date field messed up here as well, we might need to add on our 18 years to every other single value. 

### `department_employee`

> Captures information for which department each employee belongs to throughout their career with our company.

```sql
SELECT *
FROM employees.department_employee
WHERE employee_id = 10029
ORDER BY from_date;
```
|employee_id| department_id|	from_date|	to_date|
|---|---|---|---|
|10029|	d004|	1991-09-18|	1999-07-08|
|10029|	d006|	1999-07-08|	9999-01-01|

> ‼️ Fix the 9999-01-01 issue, only add 18 years to the dates. 

### `department_manager`

>  Shows the `employee_id` of the manager of each department throughout time.

```sql
SELECT *
FROM employees.department_manager
WHERE department_id = 'd004'
ORDER BY from_date;
```
|employee_id| department_id|	from_date|	to_date|
|---|---|---|---|
|110303|	d004|	1985-01-01|	1988-09-09|
|110344|	d004|	1988-09-09|	1992-08-02|
|110386|	d004|	1992-08-02|	1996-08-30|
|110420|	d004|	1996-08-30|	9999-01-01|

> ‼️ Fix the 9999-01-01 issue, only add 18 years to the dates. 

### `department`

> Maps each department id, to the name. 

```sql
SELECT *
FROM employees.department
ORDER BY id
LIMIT 2;
```

|id|	dept_name|
|---|---|
|d001|	Marketing|
|d002|	Finance|












----------------------

© Akshaya Parthasarathy, 2021

For feedback, or if you just feel like saying Hi!

[![LINKEDIN](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akshaya-parthasarathy23)
[![INSTAGRAM](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/aks_sarathy/)
[![REDDIT](https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/user/longstoryshort_)


