Markdown
# SQL Query Examples

## Table of Contents

* [Easy Questions](#easy-questions)
  * [1. Show first name, last name, and gender of patients whose gender is 'M'](#point1)
  * 2. Show first name and last name of patients who does not have allergies. (null)
  * 3. f
  * 4. f

   
    
* [Medium Questions](#medium-questions)
* [Hard Questions](#hard-questions)

## Easy Questions

### <a name="point1">1. Show first name, last name, and gender of patients whose gender is 'M' </a>

```sql
SELECT
  first_name,
  last_name,
  gender
FROM patients
WHERE gender = 'M';
```

### 2. Show first name and last name of patients who does not have allergies. (null)

```sql
SELECT
  first_name,
  last_name
FROM patients
WHERE allergies is not null
```
