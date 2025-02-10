# Solutions to Hive Tasks

This file contains solutions to the given Hive-related tasks.

## Q-1: Create Hive Database and Load `Wine.csv` into `wine` Table

```sql
CREATE DATABASE hive_odev;
USE hive_odev;

CREATE TABLE wine (
  Alcohol DOUBLE,
  Malic_Acid DOUBLE,
  Ash DOUBLE,
  Alcalinity_of_Ash DOUBLE,
  Magnesium INT,
  Total_Phenols DOUBLE,
  Flavanoids DOUBLE,
  Nonflavanoid_Phenols DOUBLE,
  Proanthocyanins DOUBLE,
  Color_Intensity DOUBLE,
  Hue DOUBLE,
  OD280_OD315_of_Diluted_Wines DOUBLE,
  Proline INT
)
ROW FORMAT DELIMITED 
FIELDS TERMINATED BY ',' 
STORED AS TEXTFILE;

LOAD DATA INPATH '/user/hive/warehouse/hive_odev/Wine.csv' 
INTO TABLE wine;
```

## Q-2: Filter `Alcohol > 13.00` and Insert into `wine_alc_gt_13` Table

```sql
CREATE TABLE wine_alc_gt_13 AS 
SELECT * FROM wine WHERE Alcohol > 13.00;
```

## Q-3: Drop `hive_odev` Database Including All Tables

```sql
DROP DATABASE hive_odev CASCADE;
```

## Q-4: Load `employee.txt` into `employee` Table in `company` Database

```sql
CREATE DATABASE IF NOT EXISTS company;
USE company;

CREATE TABLE employee (
  name STRING,
  age INT,
  department STRING,
  python_skill INT,
  java_skill INT
)
ROW FORMAT DELIMITED 
FIELDS TERMINATED BY ',' 
STORED AS TEXTFILE;

LOAD DATA INPATH '/user/hive/warehouse/company/employee.txt' 
INTO TABLE employee;
```

## Q-5: Query Employees with `Python Skill > 70`

```sql
SELECT name, age, department, python_skill 
FROM employee 
WHERE python_skill > 70;
```
