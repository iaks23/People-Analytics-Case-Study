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





----------------------

© Akshaya Parthasarathy, 2021

For feedback, or if you just feel like saying Hi!

[![LINKEDIN](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/akshaya-parthasarathy23)
[![INSTAGRAM](https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/aks_sarathy/)
[![REDDIT](https://img.shields.io/badge/Reddit-FF4500?style=for-the-badge&logo=reddit&logoColor=white)](https://www.reddit.com/user/longstoryshort_)


